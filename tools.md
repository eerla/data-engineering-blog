---
layout: default
title: "Data Engineering Tools"
---

<div class="page-header">
  <h1 class="page-title">Comprehensive Data Engineering Tools</h1>
  <p class="page-subtitle">Find right tools for your data engineering needs - cloud providers, comparisons, and decision guides</p>
</div>

<div class="container">
  <!-- Filter Section -->
  <section class="tools-filters">
    <h2>Filter Tools</h2>
    <div class="filter-controls">
      <select id="layer-filter" class="filter-select">
        <option value="all">All Layers</option>
        <option value="data-ingestion">Data Ingestion</option>
        <option value="data-processing">Data Processing</option>
        <option value="data-storage">Data Storage</option>
        <option value="data-consumption">Data Consumption</option>
      </select>
      
      <select id="type-filter" class="filter-select">
        <option value="all">All Types</option>
        <option value="batch">Batch</option>
        <option value="streaming">Streaming</option>
        <option value="bi">Business Intelligence</option>
        <option value="cloud-service">Cloud Service</option>
      </select>
      
      <select id="cloud-filter" class="filter-select">
        <option value="all">All Clouds</option>
        <option value="aws">Amazon Web Services</option>
        <option value="gcp">Google Cloud Platform</option>
        <option value="azure">Microsoft Azure</option>
        <option value="multi-cloud">Multi-Cloud</option>
        <option value="open-source">Open Source</option>
      </select>
    </div>
  </section>

  <!-- Cloud-based Tools Grid -->
  <section class="cloud-tools">
    <h2>Tools by Cloud Provider</h2>
    
    <!-- AWS Section -->
    <div class="cloud-section">
      <div class="cloud-header" onclick="toggleCloud('aws')">
        <h3>☁️ Amazon Web Services (AWS)</h3>
        <span class="tool-count">{{ site.data.tools | where: "cloud", "AWS" | size }} tools</span>
        <span class="toggle-icon">▼</span>
      </div>
      
      <div id="aws-tools" class="cloud-content">
        {% assign aws_tools = site.data.tools | where: "cloud", "AWS" %}
        <div class="tools-grid">
          {% for tool in aws_tools %}
          <div class="tool-card">
            <h4>{{ tool.name }}</h4>
            <div class="tool-meta">
              <span class="type-badge">{{ tool.type }}</span>
              <span class="layer-badge">{{ tool.layer }}</span>
            </div>
            <p><strong>Use case:</strong> {{ tool.use_case }}</p>
          </div>
          {% endfor %}
        </div>
      </div>
    </div>

    <!-- GCP Section -->
    <div class="cloud-section">
      <div class="cloud-header" onclick="toggleCloud('gcp')">
        <h3>🔵 Google Cloud Platform (GCP)</h3>
        <span class="tool-count">{{ site.data.tools | where: "cloud", "GCP" | size }} tools</span>
        <span class="toggle-icon">▼</span>
      </div>
      
      <div id="gcp-tools" class="cloud-content">
        {% assign gcp_tools = site.data.tools | where: "cloud", "GCP" %}
        <div class="tools-grid">
          {% for tool in gcp_tools %}
          <div class="tool-card">
            <h4>{{ tool.name }}</h4>
            <div class="tool-meta">
              <span class="type-badge">{{ tool.type }}</span>
              <span class="layer-badge">{{ tool.layer }}</span>
            </div>
            <p><strong>Use case:</strong> {{ tool.use_case }}</p>
          </div>
          {% endfor %}
        </div>
      </div>
    </div>

    <!-- Azure Section -->
    <div class="cloud-section">
      <div class="cloud-header" onclick="toggleCloud('azure')">
        <h3>🔷 Microsoft Azure</h3>
        <span class="tool-count">{{ site.data.tools | where: "cloud", "Azure" | size }} tools</span>
        <span class="toggle-icon">▼</span>
      </div>
      
      <div id="azure-tools" class="cloud-content">
        {% assign azure_tools = site.data.tools | where: "cloud", "Azure" %}
        <div class="tools-grid">
          {% for tool in azure_tools %}
          <div class="tool-card">
            <h4>{{ tool.name }}</h4>
            <div class="tool-meta">
              <span class="type-badge">{{ tool.type }}</span>
              <span class="layer-badge">{{ tool.layer }}</span>
            </div>
            <p><strong>Use case:</strong> {{ tool.use_case }}</p>
          </div>
          {% endfor %}
        </div>
      </div>
    </div>

    <!-- Multi-Cloud Section -->
    <div class="cloud-section">
      <div class="cloud-header" onclick="toggleCloud('multi-cloud')">
        <h3>🌐 Multi-Cloud & Cloud Agnostic</h3>
        <span class="tool-count">{{ site.data.tools | where: "cloud", "Multi-Cloud" | size }} tools</span>
        <span class="toggle-icon">▼</span>
      </div>
      
      <div id="multi-cloud-tools" class="cloud-content">
        {% assign multi_cloud_tools = site.data.tools | where: "cloud", "Multi-Cloud" %}
        <div class="tools-grid">
          {% for tool in multi_cloud_tools %}
          <div class="tool-card">
            <h4>{{ tool.name }}</h4>
            <div class="tool-meta">
              <span class="type-badge">{{ tool.type }}</span>
              <span class="layer-badge">{{ tool.layer }}</span>
            </div>
            <p><strong>Use case:</strong> {{ tool.use_case }}</p>
          </div>
          {% endfor %}
        </div>
      </div>
    </div>

    <!-- Open Source Section -->
    <div class="cloud-section">
      <div class="cloud-header" onclick="toggleCloud('open-source')">
        <h3>🔓 Open Source & Self-Hosted</h3>
        <span class="tool-count">{{ site.data.tools | where: "cloud", "Open Source" | size }} tools</span>
        <span class="toggle-icon">▼</span>
      </div>
      
      <div id="open-source-tools" class="cloud-content">
        {% assign open_source_tools = site.data.tools | where: "cloud", "Open Source" %}
        <div class="tools-grid">
          {% for tool in open_source_tools %}
          <div class="tool-card">
            <h4>{{ tool.name }}</h4>
            <div class="tool-meta">
              <span class="type-badge">{{ tool.type }}</span>
              <span class="layer-badge">{{ tool.layer }}</span>
            </div>
            <p><strong>Use case:</strong> {{ tool.use_case }}</p>
          </div>
          {% endfor %}
        </div>
      </div>
    </div>
  </section>

  <!-- Tool Comparisons Section -->
  <section class="comparisons-section">
    <h2>🔄 Tool Comparisons</h2>
    
    <!-- Orchestration Comparison -->
    <div class="comparison-section">
      <h3>Workflow Orchestration</h3>
      <div class="comparison-table">
        <div class="table-header">
          <div class="tool-col">Tool</div>
          <div class="feature-col">Best For</div>
          <div class="feature-col">Key Feature</div>
          <div class="feature-col">Learning Curve</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Airflow</strong>
            <span class="badge mature">Mature</span>
          </div>
          <div class="feature-col">Batch ETL, established teams</div>
          <div class="feature-col">Large community, extensive integrations</div>
          <div class="feature-col">Medium</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Prefect</strong>
            <span class="badge modern">Modern</span>
          </div>
          <div class="feature-col">Python-native workflows</div>
          <div class="feature-col">Dynamic scaling, modern UI</div>
          <div class="feature-col">Low-Medium</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Dagster</strong>
            <span class="badge data-aware">Data-aware</span>
          </div>
          <div class="feature-col">Asset governance, lineage</div>
          <div class="feature-col">Data assets, software-defined assets</div>
          <div class="feature-col">Medium-High</div>
        </div>
      </div>
      
      <div class="recommendation">
        <h4>Quick Recommendation:</h4>
        <ul>
          <li><strong>Choose Airflow</strong> for established ETL workflows and large teams</li>
          <li><strong>Choose Prefect</strong> for Python-first development and modern workflows</li>
          <li><strong>Choose Dagster</strong> for complex data pipelines needing governance</li>
        </ul>
      </div>
    </div>

    <!-- Data Warehouse Comparison -->
    <div class="comparison-section">
      <h3>📊 Data Warehouses</h3>
      <div class="comparison-table">
        <div class="table-header">
          <div class="tool-col">Tool</div>
          <div class="feature-col">Best For</div>
          <div class="feature-col">Key Feature</div>
          <div class="feature-col">Cost Model</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Snowflake</strong>
            <span class="badge multi-cloud">Multi-cloud</span>
          </div>
          <div class="feature-col">Enterprise analytics, multi-cloud</div>
          <div class="feature-col">Automatic scaling, data sharing</div>
          <div class="feature-col">Pay-per-use (credits)</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>BigQuery</strong>
            <span class="badge serverless">Serverless</span>
          </div>
          <div class="feature-col">Large-scale analytics, ML</div>
          <div class="feature-col">Serverless, ML integration</div>
          <div class="feature-col">Pay-per-query + storage</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Redshift</strong>
            <span class="badge aws">AWS Native</span>
          </div>
          <div class="feature-col">AWS ecosystem, petabyte-scale</div>
          <div class="feature-col">AWS integration, concurrency scaling</div>
          <div class="feature-col">Node-based + on-demand</div>
        </div>
      </div>
      
      <div class="recommendation">
        <h4>Quick Recommendation:</h4>
        <ul>
          <li><strong>Choose Snowflake</strong> for multi-cloud strategy and enterprise features</li>
          <li><strong>Choose BigQuery</strong> for serverless operations and Google ecosystem</li>
          <li><strong>Choose Redshift</strong> for AWS-native workloads and cost control</li>
        </ul>
      </div>
    </div>

    <!-- Streaming Comparison -->
    <div class="comparison-section">
      <h3>⚡ Streaming Platforms</h3>
      <div class="comparison-table">
        <div class="table-header">
          <div class="tool-col">Tool</div>
          <div class="feature-col">Best For</div>
          <div class="feature-col">Key Feature</div>
          <div class="feature-col">Complexity</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Kafka</strong>
            <span class="badge standard">Industry Standard</span>
          </div>
          <div class="feature-col">High-throughput event streaming</div>
          <div class="feature-col">Distributed log, durability</div>
          <div class="feature-col">High</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Kinesis</strong>
            <span class="badge aws">AWS Managed</span>
          </div>
          <div class="feature-col">AWS ecosystem, managed service</div>
          <div class="feature-col">Fully managed, AWS integration</div>
          <div class="feature-col">Medium</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Pulsar</strong>
            <span class="badge flexible">Flexible</span>
          </div>
          <div class="feature-col">Multi-tenancy, geo-replication</div>
          <div class="feature-col">Tiered storage, unified messaging</div>
          <div class="feature-col">High</div>
        </div>
      </div>
      
      <div class="recommendation">
        <h4>Quick Recommendation:</h4>
        <ul>
          <li><strong>Choose Kafka</strong> for maximum control and ecosystem compatibility</li>
          <li><strong>Choose Kinesis</strong> for AWS-native managed streaming</li>
          <li><strong>Choose Pulsar</strong> for advanced features and multi-tenancy</li>
        </ul>
      </div>
    </div>

    <!-- BI Tools Comparison -->
    <div class="comparison-section">
      <h3>📈 Business Intelligence Tools</h3>
      <div class="comparison-table">
        <div class="table-header">
          <div class="tool-col">Tool</div>
          <div class="feature-col">Best For</div>
          <div class="feature-col">Key Feature</div>
          <div class="feature-col">Cost</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Tableau</strong>
            <span class="badge enterprise">Enterprise</span>
          </div>
          <div class="feature-col">Visual analytics, enterprise</div>
          <div class="feature-col">Advanced visualizations</div>
          <div class="feature-col">High</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Power BI</strong>
            <span class="badge microsoft">Microsoft</span>
          </div>
          <div class="feature-col">Microsoft ecosystem, enterprise</div>
          <div class="feature-col">Office 365 integration</div>
          <div class="feature-col">Medium-High</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Looker</strong>
            <span class="badge embedded">Embedded</span>
          </div>
          <div class="feature-col">Embedded analytics, modeling</div>
          <div class="feature-col">LookML modeling layer</div>
          <div class="feature-col">High</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Metabase</strong>
            <span class="badge open-source">Open Source</span>
          </div>
          <div class="feature-col">Self-service, simplicity</div>
          <div class="feature-col">Easy setup, SQL interface</div>
          <div class="feature-col">Low-Medium</div>
        </div>
      </div>
      
      <div class="recommendation">
        <h4>Quick Recommendation:</h4>
        <ul>
          <li><strong>Choose Tableau</strong> for advanced visual analytics and enterprise needs</li>
          <li><strong>Choose Power BI</strong> for Microsoft ecosystem integration</li>
          <li><strong>Choose Looker</strong> for embedded analytics and data modeling</li>
          <li><strong>Choose Metabase</strong> for cost-effective self-service analytics</li>
        </ul>
      </div>
    </div>

    <!-- Storage Formats Comparison -->
    <div class="comparison-section">
      <h3>🏞️ Lakehouse Formats</h3>
      <div class="comparison-table">
        <div class="table-header">
          <div class="tool-col">Format</div>
          <div class="feature-col">Best For</div>
          <div class="feature-col">Key Feature</div>
          <div class="feature-col">Ecosystem</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Delta Lake</strong>
            <span class="badge databricks">Databricks</span>
          </div>
          <div class="feature-col">ACID transactions, reliability</div>
          <div class="feature-col">Time travel, optimized writes</div>
          <div class="feature-col">Databricks, Spark</div>
        </div>
        
        <div class="table-row">
          <div class="tool-col">
            <strong>Iceberg</strong>
            <span class="badge open">Open</span>
          </div>
          <div class="feature-col">Schema evolution, multi-engine</div>
          <div class="feature-col">Engine-agnostic, partitioning</div>
          <div class="feature-col">Spark, Flink, Trino</div>
        </div>
      </div>
      
      <div class="recommendation">
        <h4>Quick Recommendation:</h4>
        <ul>
          <li><strong>Choose Delta Lake</strong> for Databricks ecosystem and ACID guarantees</li>
          <li><strong>Choose Iceberg</strong> for multi-engine support and schema evolution</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- Cloud-to-Cloud Cheat Sheet -->
  <section class="cloud-cheatsheet-section">
    <h2>☁️ Cloud-to-Cloud Data Engineering Cheat Sheet</h2>
    <p class="section-intro">Quick reference for equivalent services across AWS, GCP, and Azure. Perfect for multi-cloud migrations and architecture planning.</p>
    
    <!-- Distributed Compute -->
    <div class="cheatsheet-category">
      <h3>🔥 1. Distributed Compute (Spark / Hadoop)</h3>
      <div class="cheatsheet-table">
        <div class="cheatsheet-header">
          <div>Use Case</div>
          <div>GCP</div>
          <div>AWS</div>
          <div>Azure</div>
        </div>
        <div class="cheatsheet-row">
          <div>Managed Spark/Hadoop clusters</div>
          <div>Dataproc</div>
          <div>EMR</div>
          <div>Azure Databricks</div>
        </div>
        <div class="cheatsheet-row">
          <div>Serverless Spark</div>
          <div>Dataproc Serverless</div>
          <div>EMR Serverless</div>
          <div>Synapse Serverless Spark</div>
        </div>
        <div class="cheatsheet-row">
          <div>Notebook development</div>
          <div>Vertex AI Workbench / Dataproc Hub</div>
          <div>EMR Notebooks / SageMaker</div>
          <div>Databricks Notebooks</div>
        </div>
      </div>
      <div class="cheatsheet-when">
        <strong>When to use:</strong> scalable ETL, ML feature engineering, batch pipelines, heavy Spark jobs.
      </div>
    </div>

    <!-- Batch ETL / ELT -->
    <div class="cheatsheet-category">
      <h3>⚙️ 2. Batch ETL / ELT</h3>
      <div class="cheatsheet-table">
        <div class="cheatsheet-header">
          <div>Use Case</div>
          <div>GCP</div>
          <div>AWS</div>
          <div>Azure</div>
        </div>
        <div class="cheatsheet-row">
          <div>Serverless ETL</div>
          <div>Dataflow (Batch)</div>
          <div>AWS Glue ETL</div>
          <div>ADF Mapping Data Flows</div>
        </div>
        <div class="cheatsheet-row">
          <div>Pipeline orchestration</div>
          <div>Cloud Composer (Airflow)</div>
          <div>Step Functions / MWAA</div>
          <div>Azure Data Factory Pipelines</div>
        </div>
        <div class="cheatsheet-row">
          <div>SQL ELT</div>
          <div>BigQuery SQL</div>
          <div>Redshift SQL</div>
          <div>Synapse SQL</div>
        </div>
      </div>
      <div class="cheatsheet-when">
        <strong>When to use:</strong> scheduled transformations, ELT workflows, Airflow-based orchestration.
      </div>
    </div>

    <!-- Real-Time Streaming -->
    <div class="cheatsheet-category">
      <h3>⚡ 3. Real-Time Streaming</h3>
      <div class="cheatsheet-table">
        <div class="cheatsheet-header">
          <div>Use Case</div>
          <div>GCP</div>
          <div>AWS</div>
          <div>Azure</div>
        </div>
        <div class="cheatsheet-row">
          <div>Stream ingestion</div>
          <div>Pub/Sub</div>
          <div>Kinesis Data Streams</div>
          <div>Event Hubs</div>
        </div>
        <div class="cheatsheet-row">
          <div>Stream processing</div>
          <div>Dataflow (Streaming)</div>
          <div>Kinesis Data Analytics (Flink)</div>
          <div>Azure Stream Analytics</div>
        </div>
        <div class="cheatsheet-row">
          <div>CDC ingestion</div>
          <div>Datastream</div>
          <div>DMS + MSK Connect</div>
          <div>ADF CDC / Event Grid</div>
        </div>
      </div>
      <div class="cheatsheet-when">
        <strong>When to use:</strong> event-driven pipelines, real-time analytics, CDC replication.
      </div>
    </div>

    <!-- Storage -->
    <div class="cheatsheet-category">
      <h3>🗄️ 4. Storage (Lake, Warehouse, Lakehouse)</h3>
      <div class="cheatsheet-table">
        <div class="cheatsheet-header">
          <div>Use Case</div>
          <div>GCP</div>
          <div>AWS</div>
          <div>Azure</div>
        </div>
        <div class="cheatsheet-row">
          <div>Object storage (data lake)</div>
          <div>Cloud Storage</div>
          <div>S3</div>
          <div>ADLS Gen2</div>
        </div>
        <div class="cheatsheet-row">
          <div>Data warehouse</div>
          <div>BigQuery</div>
          <div>Redshift</div>
          <div>Synapse Dedicated SQL Pool</div>
        </div>
        <div class="cheatsheet-row">
          <div>Lakehouse</div>
          <div>BigQuery + Dataplex</div>
          <div>S3 + Athena + Glue Catalog</div>
          <div>Synapse + OneLake + Fabric</div>
        </div>
      </div>
      <div class="cheatsheet-when">
        <strong>When to use:</strong> central data lake, analytics warehouse, unified lakehouse architecture.
      </div>
    </div>

    <!-- Metadata, Governance, Catalog -->
    <div class="cheatsheet-category">
      <h3>🧭 5. Metadata, Governance, Catalog</h3>
      <div class="cheatsheet-table">
        <div class="cheatsheet-header">
          <div>Use Case</div>
          <div>GCP</div>
          <div>AWS</div>
          <div>Azure</div>
        </div>
        <div class="cheatsheet-row">
          <div>Data catalog</div>
          <div>Data Catalog</div>
          <div>Glue Data Catalog</div>
          <div>Purview Data Catalog</div>
        </div>
        <div class="cheatsheet-row">
          <div>Governance & lineage</div>
          <div>Dataplex</div>
          <div>Lake Formation</div>
          <div>Microsoft Purview</div>
        </div>
      </div>
      <div class="cheatsheet-when">
        <strong>When to use:</strong> schema management, lineage, access control, governance.
      </div>
    </div>

    <!-- Data Quality & Observability -->
    <div class="cheatsheet-category">
      <h3>🧪 6. Data Quality & Observability</h3>
      <div class="cheatsheet-table">
        <div class="cheatsheet-header">
          <div>Use Case</div>
          <div>GCP</div>
          <div>AWS</div>
          <div>Azure</div>
        </div>
        <div class="cheatsheet-row">
          <div>Data quality rules</div>
          <div>Dataplex DQ</div>
          <div>Glue Data Quality</div>
          <div>Purview Data Quality</div>
        </div>
        <div class="cheatsheet-row">
          <div>Pipeline monitoring</div>
          <div>Cloud Monitoring</div>
          <div>CloudWatch</div>
          <div>Azure Monitor</div>
        </div>
      </div>
      <div class="cheatsheet-when">
        <strong>When to use:</strong> validating datasets, monitoring pipelines, enforcing SLAs.
      </div>
    </div>

    <!-- BI & Analytics -->
    <div class="cheatsheet-category">
      <h3>📊 7. BI & Analytics</h3>
      <div class="cheatsheet-table">
        <div class="cheatsheet-header">
          <div>Use Case</div>
          <div>GCP</div>
          <div>AWS</div>
          <div>Azure</div>
        </div>
        <div class="cheatsheet-row">
          <div>BI dashboards</div>
          <div>Looker / Looker Studio</div>
          <div>QuickSight</div>
          <div>Power BI</div>
        </div>
        <div class="cheatsheet-row">
          <div>SQL on data lake</div>
          <div>BigQuery Omni / BigLake</div>
          <div>Athena</div>
          <div>Synapse Serverless SQL</div>
        </div>
      </div>
      <div class="cheatsheet-when">
        <strong>When to use:</strong> dashboards, ad-hoc analytics, federated SQL.
      </div>
    </div>

    <!-- ML / Feature Engineering -->
    <div class="cheatsheet-category">
      <h3>🤖 8. ML / Feature Engineering (Adjacent to DE)</h3>
      <div class="cheatsheet-table">
        <div class="cheatsheet-header">
          <div>Use Case</div>
          <div>GCP</div>
          <div>AWS</div>
          <div>Azure</div>
        </div>
        <div class="cheatsheet-row">
          <div>ML platform</div>
          <div>Vertex AI</div>
          <div>SageMaker</div>
          <div>Azure ML</div>
        </div>
        <div class="cheatsheet-row">
          <div>Feature store</div>
          <div>Vertex AI Feature Store</div>
          <div>SageMaker Feature Store</div>
          <div>Azure Feature Store (Fabric)</div>
        </div>
      </div>
    </div>

    <!-- Quick Summary -->
    <div class="quick-summary">
      <h3>🧩 One-Page Summary</h3>
      <div class="summary-grid">
        <div class="summary-card">
          <h4>If you want Spark →</h4>
          <div class="cloud-options">
            <strong>GCP:</strong> Dataproc<br>
            <strong>AWS:</strong> EMR<br>
            <strong>Azure:</strong> Databricks
          </div>
        </div>
        
        <div class="summary-card">
          <h4>If you want Serverless ETL →</h4>
          <div class="cloud-options">
            <strong>GCP:</strong> Dataflow<br>
            <strong>AWS:</strong> Glue<br>
            <strong>Azure:</strong> ADF Data Flows
          </div>
        </div>
        
        <div class="summary-card">
          <h4>If you want Streaming →</h4>
          <div class="cloud-options">
            <strong>GCP:</strong> Pub/Sub + Dataflow<br>
            <strong>AWS:</strong> Kinesis + KDA<br>
            <strong>Azure:</strong> Event Hubs + Stream Analytics
          </div>
        </div>
        
        <div class="summary-card">
          <h4>If you want a Lakehouse →</h4>
          <div class="cloud-options">
            <strong>GCP:</strong> BigQuery + Dataplex<br>
            <strong>AWS:</strong> S3 + Athena + Glue Catalog<br>
            <strong>Azure:</strong> Synapse + OneLake + Fabric
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Quick Decision Guide -->
  <section class="decision-guide">
    <h2>🎯 Quick Decision Guide</h2>
    
    <div class="decision-grid">
      <div class="decision-card">
        <h3>Startups/Small Teams</h3>
        <ul>
          <li><strong>Orchestration:</strong> Prefect or Airflow</li>
          <li><strong>Storage:</strong> BigQuery or Redshift</li>
          <li><strong>BI:</strong> Metabase or Power BI</li>
          <li><strong>Streaming:</strong> Kinesis (if AWS)</li>
        </ul>
      </div>
      
      <div class="decision-card">
        <h3>Enterprise Teams</h3>
        <ul>
          <li><strong>Orchestration:</strong> Airflow or Dagster</li>
          <li><strong>Storage:</strong> Snowflake</li>
          <li><strong>BI:</strong> Tableau or Looker</li>
          <li><strong>Streaming:</strong> Kafka or Pulsar</li>
        </ul>
      </div>
      
      <div class="decision-card">
        <h3>Cost-Conscious</h3>
        <ul>
          <li><strong>Orchestration:</strong> Open-source Airflow</li>
          <li><strong>Storage:</strong> BigQuery (pay-per-query)</li>
          <li><strong>BI:</strong> Metabase (open-source)</li>
          <li><strong>Streaming:</strong> Managed Kinesis</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- Tool Comparisons and Layer Summary Side by Side -->
  <div class="tools-layout">
    <!-- Tool Comparisons -->
    <section class="comparison-section">
      <h2>Tool Comparisons</h2>
      <div class="comparison-grid">
        <div class="comparison-card">
          <h3>🔄 ETL Tools</h3>
          <div class="tools-compared">
            <div class="tool-compare-item">
              <strong>Airflow:</strong> Complex workflows, battle-tested
            </div>
            <div class="tool-compare-item">
              <strong>Prefect:</strong> Python-native, modern
            </div>
            <div class="tool-compare-item">
              <strong>Dagster:</strong> Asset governance, lineage
            </div>
          </div>
        </div>
        
        <div class="comparison-card">
          <h3>⚡ Streaming</h3>
          <div class="tools-compared">
            <div class="tool-compare-item">
              <strong>Kafka:</strong> High throughput, distributed
            </div>
            <div class="tool-compare-item">
              <strong>Pub/Sub:</strong> Google Cloud native
            </div>
            <div class="tool-compare-item">
              <strong>Kinesis:</strong> AWS integrated, scalable
            </div>
          </div>
        </div>
        
        <div class="comparison-card">
          <h3>📈 BI Tools</h3>
          <div class="tools-compared">
            <div class="tool-compare-item">
              <strong>Tableau:</strong> Enterprise, visual analytics
            </div>
            <div class="tool-compare-item">
              <strong>Power BI:</strong> Microsoft ecosystem
            </div>
            <div class="tool-compare-item">
              <strong>Looker:</strong> Embedded analytics, modeling
            </div>
            <div class="tool-compare-item">
              <strong>Metabase:</strong> Open-source, simple
            </div>
          </div>
        </div>
        
        <div class="comparison-card">
          <h3>🏞️ Storage Formats</h3>
          <div class="tools-compared">
            <div class="tool-compare-item">
              <strong>S3:</strong> Object storage standard
            </div>
            <div class="tool-compare-item">
              <strong>Delta Lake:</strong> ACID transactions, reliability
            </div>
            <div class="tool-compare-item">
              <strong>Iceberg:</strong> Schema evolution, multi-engine
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Layer Summary -->
    <section class="layer-summary">
      <h2>Tools by Layer</h2>
      
      {% assign ingestion_tools = tools | where: "layer", "Data Ingestion" %}
      {% assign processing_tools = tools | where: "layer", "Data Processing" %}
      {% assign storage_tools = tools | where: "layer", "Data Storage" %}
      {% assign consumption_tools = tools | where: "layer", "Data Consumption" %}
      
      <div class="summary-grid">
        <div class="summary-card">
          <h3>Data Ingestion</h3>
          <p>Moving data from sources to systems</p>
          <div class="tool-count">{{ ingestion_tools.size }} tools</div>
          <a href="{{ site.baseurl }}/layers/data-ingestion/" class="explore-link">Explore Layer</a>
        </div>
        
        <div class="summary-card">
          <h3>Data Processing</h3>
          <p>Transforming data into insights</p>
          <div class="tool-count">{{ processing_tools.size }} tools</div>
          <a href="{{ site.baseurl }}/layers/data-processing/" class="explore-link">Explore Layer</a>
        </div>
        
        <div class="summary-card">
          <h3>Data Storage</h3>
          <p>Storing and organizing data</p>
          <div class="tool-count">{{ storage_tools.size }} tools</div>
          <a href="{{ site.baseurl }}/layers/data-storage/" class="explore-link">Explore Layer</a>
        </div>
        
        <div class="summary-card">
          <h3>Data Consumption</h3>
          <p>Making data accessible and useful</p>
          <div class="tool-count">{{ consumption_tools.size }} tools</div>
          <a href="{{ site.baseurl }}/layers/data-consumption/" class="explore-link">Explore Layer</a>
        </div>
      </div>
    </section>
  </div>
</div>

<script>
// Cloud section toggle functionality
function toggleCloud(cloudId) {
  const content = document.getElementById(cloudId + '-tools');
  const icon = event.currentTarget.querySelector('.toggle-icon');
  
  if (content.style.display === 'none' || content.style.display === '') {
    content.style.display = 'block';
    icon.textContent = '▼';
  } else {
    content.style.display = 'none';
    icon.textContent = '▶';
  }
}

// Initialize with all sections collapsed
document.addEventListener('DOMContentLoaded', function() {
  const cloudContents = document.querySelectorAll('.cloud-content');
  cloudContents.forEach(content => {
    content.style.display = 'none';
  });
  
  const icons = document.querySelectorAll('.toggle-icon');
  icons.forEach(icon => {
    icon.textContent = '▶';
  });
});

// Enhanced filtering functionality with cloud provider support
document.getElementById('layer-filter').addEventListener('change', filterTools);
document.getElementById('type-filter').addEventListener('change', filterTools);
document.getElementById('cloud-filter').addEventListener('change', filterTools);

function filterTools() {
  const layerFilter = document.getElementById('layer-filter').value;
  const typeFilter = document.getElementById('type-filter').value;
  const cloudFilter = document.getElementById('cloud-filter').value;
  const toolCards = document.querySelectorAll('.tool-card');
  
  toolCards.forEach(card => {
    const layer = card.querySelector('.layer-badge').textContent;
    const type = card.querySelector('.type-badge').textContent;
    
    // Get cloud provider from parent section
    const cloudSection = card.closest('.cloud-section');
    const cloudSectionId = cloudSection ? cloudSection.id : '';
    let cloudProvider = '';
    if (cloudSectionId.includes('aws-tools')) cloudProvider = 'aws';
    else if (cloudSectionId.includes('gcp-tools')) cloudProvider = 'gcp';
    else if (cloudSectionId.includes('azure-tools')) cloudProvider = 'azure';
    else if (cloudSectionId.includes('multi-cloud-tools')) cloudProvider = 'multi-cloud';
    else if (cloudSectionId.includes('open-source-tools')) cloudProvider = 'open-source';
    
    const layerMatch = layerFilter === 'all' || layer.includes(layerFilter);
    const typeMatch = typeFilter === 'all' || type.includes(typeFilter);
    const cloudMatch = cloudFilter === 'all' || cloudProvider === cloudFilter;
    
    // Show/hide cloud sections based on cloud filter
    if (cloudFilter === 'all') {
      cloudSection.style.display = 'block';
    } else if (cloudSectionId.includes(cloudFilter + '-tools')) {
      cloudSection.style.display = 'block';
    } else {
      cloudSection.style.display = 'none';
    }
    
    // Filter individual tool cards within visible sections
    if (cloudMatch && layerMatch && typeMatch) {
      card.style.display = 'block';
    } else {
      card.style.display = 'none';
    }
  });
}
</script>

<style>
.cloud-section {
  margin-bottom: 1.5rem;
  border: 1px solid var(--border-color);
  border-radius: 8px;
  overflow: hidden;
}

.cloud-header {
  background: var(--background-secondary);
  padding: 1rem 1.5rem;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: background-color 0.2s ease;
}

.cloud-header:hover {
  background: var(--background-tertiary);
}

.cloud-header h3 {
  margin: 0;
  color: var(--primary-color);
}

.tool-count {
  background: var(--primary-color);
  color: white;
  padding: 0.25rem 0.75rem;
  border-radius: 20px;
  font-size: 0.875rem;
  font-weight: 600;
}

.toggle-icon {
  font-size: 1.2rem;
  color: var(--primary-color);
  transition: transform 0.2s ease;
}

.cloud-content {
  padding: 1.5rem;
  background: white;
  border-top: 1px solid var(--border-color);
}

.tools-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1rem;
}

.tool-card {
  padding: 1rem;
  border: 1px solid var(--border-color);
  border-radius: 6px;
  background: var(--background-secondary);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.tool-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.tool-card h4 {
  margin: 0 0 0.5rem 0;
  color: var(--text-primary);
}

.tool-meta {
  display: flex;
  gap: 0.5rem;
  margin-bottom: 0.75rem;
}

.type-badge, .layer-badge {
  padding: 0.25rem 0.5rem;
  border-radius: 4px;
  font-size: 0.75rem;
  font-weight: 600;
  color: white;
}

.type-badge {
  background: var(--secondary-color);
}

.layer-badge {
  background: var(--primary-color);
}

.tool-card p {
  margin: 0;
  font-size: 0.875rem;
  color: var(--text-secondary);
}

.cloud-tools {
  margin-bottom: 3rem;
}
</style>
