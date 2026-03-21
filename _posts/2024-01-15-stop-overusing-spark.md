---
layout: post
title: "Spark on GCP is Overkill - Use BigQuery Instead"
date: 2024-01-15
categories: data-engineering
tags: [spark, performance, optimization, system-design, BigQuery, GCP]
---

<!-- PASTE YOUR MEDIUM CONTENT HERE -->


---


If you're running a persistent Spark footprint on GCP for analytics and ELT, you should at least ask whether you still need it. In my experience as a lead data/platform engineer, for the majority of analytics-heavy workloads BigQuery is faster to operate, cheaper to run (once tuned), and dramatically simpler to own than self-managed Spark clusters. Treat Spark as an occasional specialist tool - not the default.


Teams I work with have historically reached for Spark for everything: joins, aggregations, windowing, even ML. That made sense when your data warehouse couldn't scale compute or when local transformations needed complex state.
But GCP's serverless BigQuery has closed a lot of gaps: near-infinite auto-scaling, integrated storage/compute, SQL-first tooling (stored procedures, BQML), and tighter Vertex AI integration. For ad-hoc BI, ELT, and most model training workflows, the operational burden of Dataproc + Spark often outweighs the benefits.

## What changes if you move to BigQuery
Here are the real engineering trade-offs I evaluate:
#### Operational overhead
- Spark: you manage clusters, autoscaling policies, image/version drift, YARN or Kubernetes configs, job failures due to executor OOMs and shuffle errors.
- BigQuery: serverless, no cluster ops, auto-scaling, built-in durability. You pay for queries and storage, not nodes.
#### Developer velocity
- SQL-first teams ship faster. Converting ETL to ELT SQL + stored procs shortens feedback loops and reduces QA surface area vs long-running Spark jobs.
#### Performance model
- Spark tuning is CPU/memory/shuffle focused (executors, partitions, caching).
- BigQuery tuning is about reducing scanned bytes (partitioning, clustering, denormalization, materialized views).
#### Cost predictability
- Spark costs are predictable only if you tightly pack clusters. BigQuery's on-demand billing can spike; but you control it with table design, materialized views, and flat-rate reservations.
#### Stateful streaming & complex transforms
- Use Dataflow for stateful streaming ETL; BigQuery can be the destination/warehouse. Keep Spark for niche stateful algorithms or legacy pipelines that are prohibitively expensive to re-architect.

### Example PySpark (simplified):
```python
from pyspark.sql import SparkSession 

spark = SparkSession.builder.appName("daily_agg").getOrCreate() 

events = spark.read.parquet("gs://bucket/events/") 
users = spark.read.parquet("gs://bucket/users/") 
res = events.join(users, "user_id").groupBy("day", "country").agg(…) 
res.repartition("day").write.partitionBy("day").parquet("gs://bucket/out/")
```

### After (BigQuery ELT approach):
Ingest raw events to a partitioned BigQuery table (or use BigQuery Storage API).
Run a scheduled SQL stored procedure that does the joins/aggregations in-place and writes to partitioned tables / materialized views.
No cluster ops, fewer moving parts, faster iteration.

### Example BigQuery SQL (simplified):
```sql
CREATE OR REPLACE TABLE dataset.daily_agg 
PARTITION BY DATE(event_date) AS 
SELECT 
  DATE(event_timestamp) AS event_date, 
  country, 
  COUNT(*) AS events, 
  SUM(value) AS total_value 
FROM dataset.events_raw 
WHERE event_timestamp >= DATE_SUB(CURRENT_DATE(), INTERVAL 7 DAY) 
GROUP BY event_date, country;
```

### Key techniques to make BigQuery economical and fast
If you switch, you must learn to think differently. Spark tuning = executors & shuffle; BigQuery tuning = schema and bytes.

#### Partitioning + clustering
Partition by ingestion timestamp or event date to limit scanned data.
Cluster by high-cardinality selective columns used in WHERE (user_id, event_type).

```sql
CREATE TABLE dataset.events 
PARTITION BY DATE(event_timestamp) 
CLUSTER BY user_id, event_type AS 
SELECT * FROM dataset.events_raw_import;
```

#### Denormalize where it reduces joins
For analytics, denormalized tables or pre-joined materialized views reduce repeated work.
Use repeated RECORD fields for nested data instead of explode + join patterns.

#### Materialized views and scheduled refresh
Push frequently used aggregates into materialized views to serve BI queries cheaply and quickly.

```sql
CREATE MATERIALIZED VIEW dataset.mv_user_spend AS 
SELECT 
  user_id, 
  SUM(amount) AS total_spend 
FROM dataset.transactions 
GROUP BY user_id;
```

#### Parameterize queries + use prepared statements
Prevent query sprawl (hundreds of slightly different queries) by using parameterized stored procedures and templates.

#### Cost controls
Use flat-rate reservations for predictable workloads (BI dashboards).
Enforce quotas, labels, and billing export to BigQuery for monitoring.
Implement query policies: require table scans under X bytes for interactive queries, or force preview modes.

#### Monitor query sprawl
Export audit logs and INFORMATION_SCHEMA queries into a dataset. Alert on new ad-hoc queries above byte thresholds.

#### Complex transformations / streaming - pragmatic hybrid
Streaming ETL with state? Use Dataflow (Apache Beam) to handle low latency, stateful computations and write results into BigQuery.
Complex iterative ML or GPU-bound workloads? Use Vertex AI or Dataproc selectively - not as daily defaults.

When Spark is useful: specialized custom libraries, heavy iterative algorithms that require RAM-based caching across iterations, or legacy batch processes that are costly to rewrite.

#### BigQuery ML & Vertex AI - move ML left into the warehouse
Train many baseline models (logistic, kmeans, boosted trees) directly in BigQuery using BQML.

```sql
CREATE OR REPLACE MODEL dataset.churn_model 
OPTIONS(model_type='logistic_reg') AS 
SELECT features…, label 
FROM dataset.features_table;
```
For heavier model training, use BigQuery export via Storage API or BigLake to Vertex AI. This reduces ETL friction and the need to export to Spark.

#### Interoperability - don't burn bridges
Use BigQuery Storage API for fast reads into Spark/Beam when you do need multi-engine workflows.
Export Parquet/Avro for downstream systems.
BigLake lets you maintain a single table surface across object storage and BigQuery compute.

#### Performance mindset shift (what we tune now)
Minimize bytes scanned: add PARTITION filters, use SELECT * judiciously.
Cluster for selective predicates rather than tuning shuffle.
Denormalize/flatten where it reduces join cardinality.
Use APPROX_* functions for large-scale approximations.
Materialized views for hot BI queries.

#### Operational controls & cost predictability
Flat-rate reservations: buy slots for BI-heavy workloads (redash/Looker) to avoid per-query surprises.
Budget alerts + programmatic job gating: block queries over X bytes without a tag or approval.
Centralize production pipelines under a service account with enforced labels for chargeback.

#### When to keep Spark?
Legacy pipelines costly to rewrite immediately.
GPU-heavy or highly iterative algorithms with state that don't map cleanly to SQL/BigQuery or Vertex AI.
Real-time stream processing with complex event-time state that requires Beam/Dataproc-level control - though Dataflow often covers these cases.

### Practical migration playbook
Inventory: identify all Spark jobs and classify by type: ad-hoc, scheduled ELT, streaming, ML training.
Prioritize: replace analytics + ELT first (biggest ROI). Leave complex streaming/ML last.
Convert ETL -> ELT: reimplement transformations as BigQuery SQL + stored procedures. Use staging partitioned tables.
Apply cost design: partition/cluster, create materialized views, add quotas.
Replace streaming sinks with Dataflow -> BigQuery for stateful processing.
Measure: compare latency, cost, failure rates, and developer velocity.
Decommission Dataproc clusters gradually; keep a small sandbox for ad-hoc Spark jobs using BigQuery Storage API where needed.

#### Engineering lessons (from real projects)
SQL-first reduces the feedback loop. Analysts and engineers can iterate faster when transformations live in the warehouse.
You only get BigQuery's economics after you redesign tables and queries for it. Naively copying Spark patterns into BigQuery wastes money.
Treat cost-control as a product: visibility + automated gates prevent surprise bills.
Interoperability is key. Don't pretend BigQuery replaces every tool - use Spark selectively via Storage API for niche needs.

BigQuery is not a silver bullet, but for GCP-hosted analytics and ELT it should be your default. It reduces operational overhead, accelerates delivery, and - with disciplined table design - keeps costs predictable. Keep Spark for specialized workloads, but move the majority of your analytics into BigQuery, adopt SQL-first engineering, and use Dataflow + Vertex AI for the parts BigQuery wasn't designed to own.

---

If you're building data platforms, exploring analytics, or just love thinking about how data actually tells a story, feel free to follow or leave a clap 👏. It's a small signal, but it helps me keep writing honest, example-driven content about data modeling, fact tables, dimensions, and the patterns that make analytics work.
Thanks for reading and for keeping curiosity alive ❤️.