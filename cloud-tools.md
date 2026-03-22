---
layout: default
title: "Cloud Data Engineering Tools"
---

<div class="page-header">
  <h1 class="page-title">Cloud Data Engineering Tools</h1>
  <p class="page-subtitle">Compare and choose the right tools across major cloud providers</p>
</div>

<div class="container">
  <section class="cloud-intro">
    <p class="intro-text">Navigate cloud data engineering tools by provider or category. Find native services, multi-cloud solutions, and independent tools for your data stack.</p>
    
    <div class="decision-tree">
      <h3>🎯 Quick Decision Guide</h3>
      <div class="decision-grid">
        <div class="decision-item">
          <h4>Single Cloud Strategy?</h4>
          <p>Start with native tools for simplicity and performance</p>
        </div>
        <div class="decision-item">
          <h4>Multi-Cloud Approach?</h4>
          <p>Use independent tools for flexibility and vendor diversity</p>
        </div>
        <div class="decision-item">
          <h4>Hybrid Architecture?</h4>
          <p>Combine native and independent tools for optimal results</p>
        </div>
      </div>
    </div>
  </section>

  <section class="aws-section">
    <div class="cloud-header" onclick="toggleCloud('aws')">
      <h2 class="cloud-title">🟠 Amazon Web Services (AWS)</h2>
      <span class="tool-count">50+ tools</span>
      <span class="toggle-icon">▶</span>
    </div>
    <p class="cloud-description">Comprehensive cloud platform with strong data engineering ecosystem</p>
    
    <div id="aws-tools" class="cloud-content" style="display: none;">
    
    <div class="tool-categories">
      <div class="category-section">
        <h3>1️⃣ Ingestion (Batch + Streaming)</h3>
        <div class="sub-category">
          <h4>Batch Ingestion</h4>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>AWS Glue Data Catalog Crawlers</h4>
              <p>Discover and ingest schema from various data sources automatically</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Data Discovery</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Schema discovery, automated metadata extraction, data catalog population
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>AWS Glue ETL Jobs</h4>
              <p>Batch ingestion and transformation with visual ETL interface</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">ETL Platform</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Visual ETL development, scheduled batch processing, data transformation
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>AWS DataSync</h4>
              <p>On-premises to S3 transfers with automated scheduling and delta sync</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">On-Prem Transfer</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> On-prem to cloud migration, continuous file sync, hybrid data architecture
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>AWS Transfer Family</h4>
              <p>SFTP/FTPS/FTP ingestion for secure file transfers to S3</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">File Transfer</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Secure file ingestion, partner data feeds, legacy system integration
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>AWS Snowball / Snowmobile</h4>
              <p>Petabyte-scale physical data ingestion via offline transfer devices</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Physical Transfer</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Large-scale data migration, network-limited transfers, initial data lake seeding
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4><a href="{{ site.baseurl }}/tools/#aws-lambda">AWS Lambda</a></h4>
              <p>Event-driven serverless functions for lightweight data ingestion and processing</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Serverless</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Event-driven ingestion, API-based data collection, lightweight transformations
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>AWS Step Functions</h4>
              <p>Orchestrated ingestion flows with complex state machines and error handling</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Orchestration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Complex ingestion workflows, state machine patterns, multi-step data pipelines
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Streaming Ingestion</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#amazon-kinesis">Amazon Kinesis Data Streams</a></h4>
                <p>Real-time event streaming with at-least-once delivery and scaling</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Streaming</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Real-time analytics, IoT data ingestion, event-driven architectures
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Kinesis Data Firehose</h4>
                <p>Streaming data delivery to S3, Redshift, and OpenSearch with automatic batching</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Streaming</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> High-volume streaming data, automated data lake ingestion, real-time analytics
              </div>
            </div>
              
              <div class="cloud-tool">
                <h4>Amazon MSK (Managed Kafka)</h4>
                <p>Fully managed Apache Kafka service for high-throughput event streaming</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Streaming</span>
                </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Kafka workloads, event streaming, microservices communication
              </div>
            </div>
              
              <div class="cloud-tool">
                <h4>IoT Core</h4>
                <p>IoT device data ingestion with device management and data routing</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">IoT</span>
                </div>
              <div class="when-to-use">
                <strong>When to use:</strong> IoT data collection, device management, sensor data processing
              </div>
            </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>2️⃣ CDC & Database Migration</h3>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>AWS DMS (Database Migration Service)</h4>
              <p>CDC from MySQL/Postgres/Oracle/etc. to AWS targets with schema conversion</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Database Migration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Database migration, ongoing replication, lift-and-shift projects
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>AWS SCT (Schema Conversion Tool)</h4>
              <p>Schema migration and conversion tool for heterogeneous database migrations</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Schema Migration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Schema conversion, database migration planning, heterogeneous database support
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>3️⃣ Storage (Lake + Warehouse)</h3>
          <div class="sub-category">
            <h4>Object Storage (Data Lake)</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#amazon-s3">Amazon S3</a></h4>
                <p>Industry-standard object storage for unlimited scalable data storage</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Data Lake</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data lake storage, backup and archiving, static content delivery
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Data Warehouse</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#amazon-redshift">Amazon Redshift</a></h4>
                <p>Petabyte-scale data warehouse optimized for complex analytical queries</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Data Warehouse</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Enterprise analytics, business intelligence, large-scale data warehousing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Redshift Serverless</h4>
                <p>Serverless data warehouse with automatic scaling and pay-per-query pricing</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Data Warehouse</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Variable workloads, cost optimization, serverless analytics
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Lakehouse Table Formats</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Apache Iceberg</h4>
                <p>Open table format for massive analytic datasets with schema evolution</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Table Format</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Large-scale analytics, data lake queries, multi-engine data processing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Apache Hudi</h4>
                <p>Transactional data lake platform with ACID transactions and incremental processing</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Table Format</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data lake transactions, incremental updates, CDC workloads
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Delta Lake</h4>
                <p>Storage format bringing ACID transactions and time travel to data lakes</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Table Format</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Reliable data lakes, streaming analytics, machine learning pipelines
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Parquet / ORC / Avro</h4>
                <p>Columnar file formats optimized for analytical queries and compression</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">File Format</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Analytical storage, compression optimization, schema evolution
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Catalog / Metadata</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>AWS Glue Data Catalog</h4>
                <p>Centralized metadata repository for data assets and schema management</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Data Catalog</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Metadata management, data discovery, schema governance
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Lake Formation</h4>
                <p>Data lake governance with fine-grained permissions and automated workflows</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Governance</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data lake governance, permission management, automated workflows
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>4️⃣ Processing (Batch + Streaming)</h3>
          <div class="sub-category">
            <h4>Batch Processing</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>AWS Glue (Spark-based)</h4>
                <p>Serverless Spark service for large-scale data transformations and ETL</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Distributed Computing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Big data transformations, ETL workflows, serverless processing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#apache-spark">Amazon EMR</a></h4>
                <p>Managed Hadoop/Spark cluster for big data processing workloads</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Distributed Computing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Big data transformations, machine learning pipelines, large-scale data processing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Amazon Redshift SQL</h4>
                <p>SQL interface for Redshift with advanced analytics and window functions</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">SQL Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data warehouse analytics, complex queries, SQL-based transformations
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Athena (Presto/Trino)</h4>
                <p>Serverless SQL query engine for analyzing data directly in S3</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">SQL Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Direct S3 queries, ad-hoc analytics, cost-effective data exploration
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>AWS Batch</h4>
                <p>Batch computing service for large-scale job processing and HPC workloads</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Batch Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Large-scale batch jobs, HPC workloads, cost-effective compute
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#aws-lambda">Lambda</a></h4>
                <p>Serverless compute for lightweight data transformations and enrichment</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Serverless</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Lightweight transformations, event-driven processing, cost-effective compute
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Streaming Processing</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Kinesis Data Analytics (Flink)</h4>
                <p>Managed Apache Flink for real-time analytics with SQL and Java APIs</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Stream Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Real-time analytics, windowed aggregations, complex stream processing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Kinesis Data Analytics SQL</h4>
                <p>SQL interface for real-time stream processing with standard SQL syntax</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Stream Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> SQL-based stream processing, real-time analytics, familiar query language
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Amazon MSK + Kafka Streams</h4>
                <p>Managed Kafka integration with AWS-native streaming analytics</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Stream Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Kafka workloads, stream processing, microservices communication
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>EMR Spark Structured Streaming</h4>
                <p>Managed Spark clusters with structured streaming capabilities and windowing</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Stream Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Complex streaming logic, Spark ecosystem, advanced stream processing
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>5️⃣ Orchestration & Workflow Management</h3>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>AWS Step Functions</h4>
              <p>Serverless orchestration for complex workflows with state machines and error handling</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Orchestration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Complex workflows, state machine patterns, multi-step data pipelines
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Amazon MWAA (Managed Airflow)</h4>
              <p>Managed Apache Airflow for workflow orchestration with AWS integration</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Orchestration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Airflow workflows, AWS-native orchestration, managed DAG execution
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>AWS Glue Workflows</h4>
              <p>Visual workflow orchestration with drag-and-drop interface and AWS service integration</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Orchestration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Visual workflow building, AWS service integration, simplified orchestration
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>EventBridge</h4>
              <p>Event-driven orchestration for cloud service integration and automated responses</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Event Orchestration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Event-driven architectures, cloud service integration, automated responses
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>CloudWatch Events</h4>
              <p>Cron-based job scheduling and event-driven automation for AWS services</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Job Scheduling</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Cron jobs, scheduled tasks, periodic data processing
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>6️⃣ Data Modeling & Transformation</h3>
          <div class="sub-category">
            <h4>Modeling</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>dbt Core on AWS</h4>
                <p>SQL-based transformation tool with AWS Redshift and Athena adapters</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data warehouse transformations, analytics engineering, SQL-based pipelines
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>dbt Cloud</h4>
                <p>Managed dbt service with CI/CD, scheduling, and team collaboration</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Team collaboration, managed transformations, automated testing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Amazon Redshift SQL</h4>
                <p>Advanced SQL with window functions, arrays, and analytics capabilities</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">SQL Modeling</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data warehouse analytics, complex queries, advanced SQL features
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Athena SQL</h4>
                <p>SQL interface for S3 data with Presto/Trino engine and standard SQL syntax</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">SQL Modeling</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Direct S3 queries, ad-hoc analytics, SQL-based data exploration
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Transformation Engines</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Glue (Spark)</h4>
                <p>Serverless Spark service for large-scale data transformations</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Big data transformations, ETL workflows, serverless processing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#apache-spark">EMR (Spark)</a></h4>
                <p>Managed Hadoop/Spark cluster with ecosystem libraries and SQL interfaces</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Big data transformations, ML pipelines, Spark ecosystem
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Amazon Redshift SQL</h4>
                <p>Advanced SQL engine with analytics functions and stored procedures</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data warehouse transformations, complex analytics, SQL-based processing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Athena SQL</h4>
                <p>SQL engine for S3 data with standard SQL and analytical functions</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Direct S3 queries, ad-hoc analytics, SQL-based transformations
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>7️⃣ Data Quality, Lineage & Observability</h3>
          <div class="sub-category">
            <h4>Data Quality</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>AWS Glue Data Quality</h4>
                <p>Comprehensive data quality framework with rules, monitoring, and validation</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Data Quality</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data quality monitoring, automated validation, quality rules enforcement
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Deequ (Amazon OSS)</h4>
                <p>Open-source data quality library for data validation and testing</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Data Quality</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Custom data quality testing, validation automation, quality assurance
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>dbt tests</h4>
                <p>SQL-based data testing framework for data validation and quality checks</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Data Quality</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data testing, validation automation, quality assurance
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Lineage</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>AWS Glue Lineage</h4>
                <p>Automated data lineage tracking and visualization for data dependencies</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Data Lineage</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Impact analysis, data governance, compliance reporting, dependency tracking
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Lake Formation permissions lineage</h4>
                <p>Permission tracking and access control lineage for data lake governance</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Data Lineage</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Access control tracking, compliance auditing, permission management
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Monitoring & Observability</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>CloudWatch Logs</h4>
                <p>Centralized logging service for applications and infrastructure monitoring</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Logging</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Log aggregation, troubleshooting, audit trails, application monitoring
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>CloudWatch Metrics</h4>
                <p>Comprehensive metrics collection and monitoring for AWS services and custom applications</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Monitoring</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Infrastructure monitoring, performance tracking, alerting, custom metrics
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>X-Ray</h4>
                <p>Distributed tracing for microservices and application performance analysis</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Tracing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Performance optimization, microservices debugging, latency analysis, distributed tracing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>OpenSearch Dashboards</h4>
                <p>Real-time dashboards and visualization for operational monitoring</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Monitoring</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Real-time monitoring, operational dashboards, log visualization
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>8️⃣ Metadata, Catalog, Governance</h3>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>AWS Glue Data Catalog</h4>
              <p>Centralized metadata repository for data assets and schema management</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Data Catalog</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Metadata management, data discovery, schema governance
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>AWS Lake Formation</h4>
              <p>Data lake governance with permissions, workflows, and automated management</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Governance</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Data lake governance, permission management, automated workflows
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>IAM</h4>
              <p>Identity and access management for fine-grained permissions and security</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Access Control</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Access control, security management, compliance, fine-grained permissions
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Macie</h4>
              <p>AI-powered sensitive data detection, classification, and protection</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Data Protection</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Sensitive data detection, PII protection, compliance, automated classification
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>KMS</h4>
              <p>Key management service for encryption and secure key storage</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Security</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Data encryption, key management, security compliance
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>CloudTrail</h4>
              <p>Audit logging and API activity tracking for security and compliance</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Audit</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Security auditing, compliance monitoring, API activity tracking
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>9️⃣ Serving & Consumption</h3>
          <div class="sub-category">
            <h4>BI & Analytics</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Amazon QuickSight</h4>
                <p>Business intelligence platform with interactive dashboards and ML insights</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Business Intelligence</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Business intelligence, interactive dashboards, ML-powered analytics
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Redshift Query Editor</h4>
                <p>Web-based SQL editor for Redshift with query optimization and visualization</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">SQL Editor</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Redshift query development, ad-hoc analysis, SQL optimization
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Athena</h4>
                <p>Interactive query service for S3 data with ad-hoc analysis and visualization</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">SQL Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Ad-hoc data analysis, interactive queries, S3 data exploration
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Reverse ETL / Operational Analytics</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Hightouch</h4>
                <p>Sync warehouse data back to SaaS tools for operational analytics and activation</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Reverse ETL</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Sales team enablement, operational dashboards, data activation
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Census</h4>
                <p>Operational analytics platform for warehouse-to-app data sync and activation</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Reverse ETL</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Customer success analytics, marketing automation, sales team insights
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>🔟 ML / Feature Serving</h3>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>SageMaker</h4>
              <p>Comprehensive ML platform for training, deployment, and managing models at scale</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">ML Platform</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Machine learning pipelines, model training, MLOps, deployment
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>SageMaker Feature Store</h4>
              <p>Centralized feature management for ML workflows with low-latency serving</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">Feature Store</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Feature engineering, ML workflows, feature reuse, low-latency serving
                </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Redshift ML</h4>
              <p>In-database machine learning for predictive analytics and model deployment</p>
              <div class="tool-details">
                <span class="cloud-badge">AWS Native</span>
                <span class="type-badge">ML Platform</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> In-database ML, predictive analytics, SQL-based machine learning
                </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>1️⃣1️⃣ DevOps, CI/CD, Infrastructure for Data Engineering</h3>
          <div class="sub-category">
            <h4>Infrastructure</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>CloudFormation</h4>
                <p>Infrastructure as code service for managing AWS resources declaratively</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Infrastructure as Code</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Infrastructure automation, version control, reproducible environments
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Terraform on AWS</h4>
                <p>Multi-cloud infrastructure as code tool with AWS provider support</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Infrastructure as Code</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Multi-cloud infrastructure, version control, provider-agnostic deployments
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>AWS CDK</h4>
                <p>Software-defined infrastructure using familiar programming languages</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Infrastructure as Code</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Infrastructure as code, programmatic deployments, type-safe resource management
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>CI/CD</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>CodePipeline</h4>
                <p>Continuous integration and delivery service for automated build and deployment</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">CI/CD</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Automated deployments, CI/CD pipelines, release management
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>CodeBuild</h4>
                <p>Fully managed build service for compiling, testing, and packaging code</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">CI/CD</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Automated builds, testing, artifact creation, build automation
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>CodeCommit</h4>
                <p>Managed Git service for source code control and collaboration</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Version Control</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Source code management, team collaboration, CI/CD integration
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Compute Runtimes</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>ECS / Fargate</h4>
                <p>Container orchestration with serverless compute and automatic scaling</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Container Platform</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Containerized applications, serverless compute, microservices
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>EKS (Kubernetes)</h4>
                <p>Managed Kubernetes cluster for container orchestration and scaling</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Container Orchestration</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Complex applications, microservices, container orchestration
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#aws-lambda">Lambda</a></h4>
                <p>Serverless compute for event-driven functions and lightweight processing</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Serverless</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Event-driven processing, lightweight functions, serverless architecture
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>EC2</h4>
                <p>Virtual machines for custom data processing workloads and full control</p>
                <div class="tool-details">
                  <span class="cloud-badge">AWS Native</span>
                  <span class="type-badge">Virtual Machines</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Custom software, specialized workloads, full control, HPC applications
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>🧭 End-to-End AWS Data Engineering Pipeline (Ordered)</h3>
          <div class="pipeline-summary">
            <table class="pipeline-table">
              <thead>
                <tr>
                  <th>Stage</th>
                  <th>AWS Tools</th>
                  <th>Description</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td><strong>Ingest</strong></td>
                  <td>Kinesis, Firehose, DMS, DataSync, Glue</td>
                  <td>Event streaming, CDC, ETL, batch transfers</td>
                </tr>
                <tr>
                  <td><strong>Land</strong></td>
                  <td>S3</td>
                  <td>Data lake with raw, bronze, silver, gold layers</td>
                </tr>
                <tr>
                  <td><strong>Process</strong></td>
                  <td>Glue, EMR, Athena, Redshift</td>
                  <td>Spark processing, SQL queries, big data analytics</td>
                </tr>
                <tr>
                  <td><strong>Model</strong></td>
                  <td>dbt, Redshift SQL, Athena SQL</td>
                  <td>Analytics engineering, SQL modeling, query optimization</td>
                </tr>
                <tr>
                  <td><strong>Orchestrate</strong></td>
                  <td>Step Functions, MWAA</td>
                  <td>Serverless orchestration, managed Airflow</td>
                </tr>
                <tr>
                  <td><strong>Validate</strong></td>
                  <td>Glue Data Quality, Deequ</td>
                  <td>Data quality monitoring, automated validation</td>
                </tr>
                <tr>
                  <td><strong>Catalog</strong></td>
                  <td>Glue Catalog, Lake Formation</td>
                  <td>Metadata management, data lake governance</td>
                </tr>
                <tr>
                  <td><strong>Serve</strong></td>
                  <td>QuickSight, SageMaker</td>
                  <td>Business intelligence, machine learning serving</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  </div> <!-- Close AWS section div -->


  <section class="gcp-section">
    <div class="cloud-header" onclick="toggleCloud('gcp')">
      <h2 class="cloud-title">☁️ Google Cloud Platform (GCP)</h2>
      <span class="tool-count">40+ tools</span>
      <span class="toggle-icon">▶</span>
    </div>
    <p class="cloud-description">Comprehensive cloud platform with serverless-first approach and strong ML integration</p>
    
    <div id="gcp-tools" class="cloud-content" style="display: none;">
    
    <div class="tool-categories">
      <div class="category-section">
        <h3>1️⃣ Ingestion (Batch + Streaming)</h3>
        <div class="sub-category">
          <h4>Batch Ingestion</h4>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>Cloud Storage Transfer Service</h4>
              <p>Move data from AWS/S3, HTTP, on-prem to GCP with automated scheduling</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Batch Transfer</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Migrating data from other clouds, scheduled batch transfers, on-prem to cloud migration
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Storage Transfer Service for On-Prem</h4>
              <p>Agent-based ingestion for on-premises data sources to Cloud Storage</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">On-Prem Transfer</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Large on-prem data migration, continuous sync from on-prem to cloud
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Cloud Data Fusion</h4>
              <p>Low-code ETL platform with 200+ pre-built connectors for data integration</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">ETL Platform</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Rapid ETL development, connecting SaaS applications, visual data pipeline building
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Cloud Functions</h4>
              <p>Event-driven serverless functions for lightweight data ingestion and processing</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Serverless</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Event-driven data ingestion, API-based data collection, lightweight transformations
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Cloud Run</h4>
              <p>Containerized ingestion microservices with automatic scaling and load balancing</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Container Platform</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Custom ingestion services, container-based data processing, HTTP-based data collection
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Streaming Ingestion</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#google-pub-sub">Pub/Sub</a></h4>
                <p>Fully managed event ingestion service with at-least-once delivery guarantees</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Streaming</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Real-time event streaming, microservices communication, event-driven architectures
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Pub/Sub Lite</h4>
                <p>Cheaper Kafka-like alternative for high-throughput event streaming</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Streaming</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Cost-effective event streaming, Kafka workloads, high-throughput messaging
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>2️⃣ CDC & Database Migration</h3>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>Database Migration Service (DMS)</h4>
              <p>Managed service for MySQL/Postgres/SQL Server → Cloud SQL/BigQuery migration</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Database Migration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Database migration, ongoing replication, lift-and-shift projects
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Datastream</h4>
              <p>CDC service for MySQL/Postgres/Oracle → BigQuery with schema evolution</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">CDC</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Real-time database replication, change data capture, streaming database updates
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>3️⃣ Storage (Lake + Warehouse)</h3>
          <div class="sub-category">
            <h4>Object Storage (Data Lake)</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#google-cloud-storage">Cloud Storage (GCS)</a></h4>
                <p>Unified object storage for raw, bronze, silver, and gold data layers</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Data Lake</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data lake implementation, medallion architecture, cost-effective storage
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Data Warehouse</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#google-bigquery">BigQuery</a></h4>
                <p>Serverless warehouse with lakehouse engine, ML, and geospatial analytics</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Data Warehouse</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Large-scale analytics, real-time dashboards, cost-effective warehousing
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Lakehouse Table Formats</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>BigLake Tables</h4>
                <p>Native BigQuery support for lakehouse table formats with ACID transactions</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Table Format</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Lakehouse architecture, ACID transactions on data lake, schema evolution
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Iceberg Support</h4>
                <p>Apache Iceberg table format support via BigLake connectors</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Table Format</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Large analytic tables, time travel queries, schema evolution
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Delta Lake Support</h4>
                <p>Read/write Delta Lake tables via BigLake connectors</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Table Format</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Delta Lake workloads, ACID transactions, merge operations
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>4️⃣ Processing (Batch + Streaming)</h3>
          <div class="sub-category">
            <h4>Batch Processing</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#google-bigquery">BigQuery SQL</a></h4>
                <p>Serverless SQL engine for large-scale data transformations and analytics</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">SQL Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Large-scale transformations, analytical queries, ELT workflows
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#dataproc">Dataproc</a></h4>
                <p>Managed Hadoop/Spark cluster for big data processing workloads</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Distributed Computing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Big data analytics, machine learning pipelines, distributed processing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#google-dataflow">Dataflow</a></h4>
                <p>Managed Apache Beam service for batch and stream processing</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Stream Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Real-time analytics, event processing, large-scale data transformations
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Cloud Composer-Triggered Jobs</h4>
                <p>Orchestrate batch processing jobs with Airflow workflows</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Orchestration</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Complex workflow orchestration, scheduled batch jobs, dependency management
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Cloud Run / Cloud Functions for Lightweight Transforms</h4>
                <p>Serverless compute for small-scale data transformations and enrichment</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Serverless</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Lightweight transformations, event-driven processing, cost-effective compute
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Streaming Processing</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Dataflow (Beam Streaming)</h4>
                <p>Apache Beam streaming for real-time data processing with windowing</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Stream Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Real-time analytics, windowed aggregations, stream processing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Dataproc + Spark Structured Streaming</h4>
                <p>Managed Spark clusters with structured streaming capabilities</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Stream Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Complex streaming logic, Spark ecosystem, advanced stream processing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>BigQuery Streaming Inserts</h4>
                <p>Real-time data insertion into BigQuery tables via streaming API</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Streaming</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Real-time analytics, dashboard updates, low-latency data availability
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Pub/Sub → BigQuery Direct Write</h4>
                <p>Direct streaming from Pub/Sub to BigQuery without intermediate processing</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Streaming</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Simple event-to-table pipelines, real-time dashboards, minimal processing needs
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>5️⃣ Orchestration & Workflow Management</h3>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>Cloud Composer</h4>
              <p>Managed Apache Airflow for complex workflow orchestration and DAG management</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Orchestration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Complex workflows, Airflow DAGs, dependency management, scheduled jobs
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Workflows</h4>
              <p>Serverless orchestration for event-driven workflows and microservices</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Orchestration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Event-driven orchestration, microservices coordination, serverless workflows
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Cloud Scheduler</h4>
              <p>Cron-based job scheduling for periodic data processing tasks</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Job Scheduling</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Cron jobs, scheduled tasks, periodic data processing
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Eventarc</h4>
              <p>Event-driven orchestration for cloud service integrations</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Event Orchestration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Event-driven architectures, cloud service integration, automated responses
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>6️⃣ Data Modeling & Transformation</h3>
          <div class="sub-category">
            <h4>Modeling</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#google-bigquery">BigQuery SQL</a></h4>
                <p>Advanced SQL with window functions, arrays, and machine learning integration</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">SQL Modeling</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data modeling, analytical queries, complex transformations
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>dbt Core on GCP</h4>
                <p>SQL-based transformation tool with GCP BigQuery adapter</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data warehouse transformations, analytics engineering, SQL-based pipelines
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>dbt Cloud</h4>
                <p>Managed dbt service with CI/CD, scheduling, and collaboration</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Team collaboration, managed transformations, automated testing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>LookML (Looker)</h4>
                <p>Data modeling language for Looker with version control and testing</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Modeling</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Business intelligence modeling, governed data access, Looker integration
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Transformation Engines</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#google-dataflow">Dataflow (Beam)</a></h4>
                <p>Apache Beam unified model for batch and stream processing</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Unified batch/stream processing, portable pipelines, complex transformations
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#dataproc">Dataproc (Spark)</a></h4>
                <p>Apache Spark ecosystem with ML libraries and SQL interfaces</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Big data transformations, ML pipelines, Spark ecosystem
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>BigQuery SQL / BigQuery ML</h4>
                <p>SQL with built-in machine learning functions for predictive analytics</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">ML Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> In-database ML, predictive analytics, SQL-based ML
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>7️⃣ Data Quality, Lineage & Observability</h3>
          <div class="sub-category">
            <h4>Data Quality</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Dataplex Data Quality</h4>
                <p>Comprehensive data quality framework with rules and monitoring</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Data Quality</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data quality monitoring, automated validation, quality rules
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>BigQuery Data Quality (via Dataplex)</h4>
                <p>Native BigQuery data quality checks and monitoring</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Data Quality</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Warehouse quality monitoring, automated quality checks
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>dbt Tests</h4>
                <p>SQL-based data testing framework for data validation</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Data Quality</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data testing, validation automation, quality assurance
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Lineage</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Dataplex Lineage</h4>
                <p>Automated data lineage tracking and visualization</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Data Lineage</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Impact analysis, data governance, compliance reporting
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>BigQuery Built-in Lineage</h4>
                <p>Native BigQuery data lineage for query and table relationships</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Data Lineage</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Query optimization, dependency tracking, impact analysis
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Monitoring & Observability</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Cloud Monitoring</h4>
                <p>Comprehensive monitoring for all GCP services and custom metrics</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Monitoring</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Infrastructure monitoring, performance tracking, alerting
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Cloud Logging</h4>
                <p>Centralized logging service for applications and infrastructure</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Logging</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Log aggregation, troubleshooting, audit trails
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Error Reporting</h4>
                <p>Application error tracking and debugging with stack traces</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Error Tracking</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Application debugging, error monitoring, performance analysis
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Cloud Trace</h4>
                <p>Distributed tracing for microservices and application performance</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Tracing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Performance optimization, microservices debugging, latency analysis
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>8️⃣ Metadata, Catalog, Governance</h3>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>Dataplex</h4>
              <p>Unified platform for governance, metadata, quality, and lineage</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Governance Platform</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Data governance, metadata management, quality monitoring
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Data Catalog (now part of Dataplex)</h4>
              <p>Enterprise data catalog for data discovery and documentation</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Data Catalog</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Data discovery, metadata management, data literacy
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>IAM</h4>
              <p>Identity and access management for fine-grained permissions</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Access Control</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Access control, security management, compliance
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>VPC Service Controls</h4>
              <p>Data perimeter controls for security and compliance</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Security</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Data perimeter security, compliance, data exfiltration prevention
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Cloud DLP</h4>
              <p>Data classification, masking, and sensitive data protection</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Data Protection</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Data classification, PII protection, compliance
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>9️⃣ Serving & Consumption</h3>
          <div class="sub-category">
            <h4>BI & Analytics</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Looker</h4>
                <p>Business intelligence platform with embedded analytics and modeling</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Business Intelligence</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Business intelligence, embedded analytics, governed data access
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Looker Studio</h4>
                <p>Self-service BI and visualization platform for business users</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Business Intelligence</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Self-service analytics, dashboard creation, business user empowerment
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Connected Sheets</h4>
                <p>Google Sheets integration with BigQuery for business analytics</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Analytics</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Business analytics, spreadsheet-based analysis, familiar interface
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Reverse ETL / Operational Analytics</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Hightouch</h4>
                <p>Sync warehouse data back to SaaS tools for operational analytics</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Reverse ETL</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Sales team enablement, operational dashboards, data activation
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Census</h4>
                <p>Operational analytics platform for warehouse-to-app data sync</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Reverse ETL</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Customer success analytics, marketing automation, sales insights
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>🔟 ML / Feature Serving</h3>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>Vertex AI</h4>
              <p>Comprehensive ML platform for training, deployment, and serving</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">ML Platform</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Machine learning pipelines, model deployment, MLOps
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>BigQuery ML</h4>
              <p>In-database machine learning for predictive analytics</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">ML Platform</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> In-database ML, predictive analytics, SQL-based ML
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Feature Store (Vertex AI)</h4>
              <p>Centralized feature management for ML workflows</p>
              <div class="tool-details">
                <span class="cloud-badge">GCP Native</span>
                <span class="type-badge">Feature Store</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Feature engineering, ML workflows, feature reuse
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>1️⃣1️⃣ DevOps, CI/CD, Infrastructure for Data Engineering</h3>
          <div class="sub-category">
            <h4>Infrastructure</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Terraform on GCP</h4>
                <p>Infrastructure as code for managing GCP resources declaratively</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Infrastructure as Code</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Infrastructure automation, version control, reproducible environments
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Deployment Manager</h4>
                <p>Declarative infrastructure deployment and configuration management</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Infrastructure as Code</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Infrastructure deployment, configuration management, environment replication
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Cloud Build</h4>
                <p>CI/CD platform for building and deploying data applications</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">CI/CD</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Application building, automated deployment, container images
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Artifact Registry</h4>
                <p>Container and artifact repository for data applications</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Artifact Registry</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Container storage, artifact management, deployment pipeline
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Compute Runtimes</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4><a href="{{ site.baseurl }}/tools/#google-cloud-run">Cloud Run</a></h4>
                <p>Serverless container platform for data applications</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Container Platform</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Containerized applications, serverless compute, HTTP services
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>GKE (Kubernetes)</h4>
                <p>Managed Kubernetes cluster for container orchestration</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Container Orchestration</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Complex applications, microservices, container orchestration
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Compute Engine</h4>
                <p>Virtual machines for custom data processing workloads</p>
                <div class="tool-details">
                  <span class="cloud-badge">GCP Native</span>
                  <span class="type-badge">Virtual Machines</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Custom software, specialized workloads, full control
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>🧭 End-to-End GCP Data Engineering Pipeline (Ordered)</h3>
          <div class="pipeline-summary">
            <table class="pipeline-table">
              <thead>
                <tr>
                  <th>Stage</th>
                  <th>GCP Tools</th>
                  <th>Description</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td><strong>Ingest</strong></td>
                  <td>Pub/Sub, Datastream, Data Fusion, Storage Transfer</td>
                  <td>Event streaming, CDC, ETL, batch transfers</td>
                </tr>
                <tr>
                  <td><strong>Land</strong></td>
                  <td>Cloud Storage</td>
                  <td>Data lake with medallion architecture</td>
                </tr>
                <tr>
                  <td><strong>Process</strong></td>
                  <td>Dataflow, Dataproc, BigQuery</td>
                  <td>Stream processing, Spark, SQL transformations</td>
                </tr>
                <tr>
                  <td><strong>Model</strong></td>
                  <td>dbt, BigQuery SQL, LookML</td>
                  <td>Analytics engineering, SQL modeling, BI modeling</td>
                </tr>
                <tr>
                  <td><strong>Orchestrate</strong></td>
                  <td>Cloud Composer, Workflows</td>
                  <td>Airflow, serverless orchestration</td>
                </tr>
                <tr>
                  <td><strong>Validate</strong></td>
                  <td>Dataplex Data Quality</td>
                  <td>Data quality monitoring, automated validation</td>
                </tr>
                <tr>
                  <td><strong>Catalog</strong></td>
                  <td>Dataplex, Data Catalog</td>
                  <td>Metadata management, data discovery</td>
                </tr>
                <tr>
                  <td><strong>Serve</strong></td>
                  <td>Looker, Looker Studio, Vertex AI</td>
                  <td>Business intelligence, self-service analytics, ML serving</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  </div> <!-- Close GCP section div -->

  <section class="azure-section">
    <div class="cloud-header" onclick="toggleCloud('azure')">
      <h2 class="cloud-title">🔵 Microsoft Azure</h2>
      <span class="tool-count">40+ tools</span>
      <span class="toggle-icon">▶</span>
    </div>
    <p class="cloud-description">Enterprise-focused cloud platform with strong Microsoft ecosystem integration</p>
    
    <div id="azure-tools" class="cloud-content" style="display: none;">
    
    <div class="tool-categories">
      <div class="category-section">
        <h3>1️⃣ Ingestion (Batch + Streaming)</h3>
        <div class="sub-category">
          <h4>Batch Ingestion</h4>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>Azure Data Factory (ADF)</h4>
              <p>ETL/ELT pipelines with 90+ connectors and visual drag-and-drop interface</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">ETL Platform</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Visual ETL development, scheduled batch processing, data integration
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Data Box</h4>
              <p>Physical data transfer appliance for large-scale offline data migration</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Physical Transfer</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Large-scale data migration, network-limited transfers, initial data lake seeding
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Data Share</h4>
              <p>Secure dataset sharing across organizations with governance and monitoring</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Data Sharing</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Cross-organization data sharing, partner data exchange, secure data distribution
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Functions</h4>
              <p>Event-driven serverless functions for lightweight data ingestion and processing</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Serverless</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Event-driven ingestion, API-based data collection, lightweight transformations
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Logic Apps</h4>
              <p>Low-code ingestion workflows with 900+ connectors and visual designer</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Low-Code</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Workflow automation, connector-based integration, low-code data pipelines
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Streaming Ingestion</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Azure Event Hubs</h4>
                <p>Kafka-like event ingestion with high throughput and partitioning</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Streaming</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Real-time analytics, IoT data ingestion, event-driven architectures
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure IoT Hub</h4>
                <p>IoT device ingestion with device management, provisioning, and routing</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">IoT</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> IoT data collection, device management, sensor data processing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Event Grid</h4>
                <p>Event routing service for building reactive and event-driven applications</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Event Routing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Event-driven architectures, service integration, reactive applications
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Stream Analytics Inputs</h4>
                <p>Real-time ingestion for Stream Analytics with multiple input sources</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Streaming</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Real-time analytics, stream processing, multi-source ingestion
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>2️⃣ CDC & Database Migration</h3>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>Azure Database Migration Service (DMS)</h4>
              <p>Managed database migration service for heterogeneous database migrations</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Database Migration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Database migration, ongoing replication, lift-and-shift projects
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Data Factory Mapping Data Flows (CDC patterns)</h4>
              <p>Change data capture patterns with visual mapping and transformation</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">CDC</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Real-time database replication, change data capture, streaming updates
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure SQL CDC → Event Hubs / Data Lake</h4>
              <p>Native SQL Server CDC integration with streaming destinations</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">CDC</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> SQL Server real-time replication, streaming analytics, change tracking
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>3️⃣ Storage (Lake + Warehouse)</h3>
          <div class="sub-category">
            <h4>Object Storage (Data Lake)</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Azure Data Lake Storage Gen2 (ADLS)</h4>
                <p>Hierarchical namespace storage optimized for big data analytics workloads</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Data Lake</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data lake implementation, big data analytics, hierarchical storage
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Blob Storage</h4>
                <p>Object storage for unstructured data with multiple access tiers</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Object Storage</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Unstructured data storage, backup, content delivery, tiered storage
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Data Warehouse</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Azure Synapse Analytics Dedicated SQL Pool</h4>
                <p>Enterprise data warehouse with distributed processing and MPP</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Data Warehouse</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Enterprise analytics, large-scale data warehousing, complex queries
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Synapse Serverless SQL</h4>
                <p>Serverless SQL engine for querying data directly in storage</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Serverless</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Ad-hoc analytics, cost-effective queries, direct storage queries
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Lakehouse Table Formats</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Delta Lake (native in Synapse & Fabric)</h4>
                <p>Native Delta Lake support with ACID transactions and time travel</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Table Format</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Lakehouse architecture, ACID transactions, time travel queries
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Apache Iceberg</h4>
                <p>Open table format for massive analytic datasets with schema evolution</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Table Format</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Large-scale analytics, data lake queries, multi-engine processing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Apache Hudi</h4>
                <p>Transactional data lake platform with ACID transactions and incremental processing</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Table Format</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data lake transactions, incremental updates, CDC workloads
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Parquet / ORC / Avro</h4>
                <p>Columnar file formats optimized for analytical queries and compression</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">File Format</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Analytical storage, compression optimization, schema evolution
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Catalog / Metadata</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Microsoft Purview (now Microsoft Purview)</h4>
                <p>Unified data catalog with governance, lineage, and classification</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Data Catalog</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data discovery, governance, metadata management, compliance
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Synapse Workspace Catalog</h4>
                <p>Workspace-level metadata catalog for Synapse analytics assets</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Data Catalog</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Synapse asset management, workspace metadata, analytics catalog
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>4️⃣ Processing (Batch + Streaming)</h3>
          <div class="sub-category">
            <h4>Batch Processing</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Azure Databricks</h4>
                <p>Managed Databricks platform for big data analytics and machine learning</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Analytics Platform</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Big data analytics, machine learning development, collaborative data science
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Synapse Spark Pools</h4>
                <p>Serverless Spark pools for big data processing and analytics</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Distributed Computing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Big data transformations, Spark processing, serverless analytics
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Synapse SQL (serverless + dedicated)</h4>
                <p>Unified SQL engine for both serverless and dedicated processing</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">SQL Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> SQL-based analytics, flexible processing, cost optimization
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Data Factory Mapping Data Flows</h4>
                <p>Visual data transformation with code-free mapping and processing</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Data Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Visual transformations, code-free ETL, data mapping
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Functions for lightweight transforms</h4>
                <p>Serverless functions for lightweight data transformations and enrichment</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Serverless</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Lightweight transformations, event-driven processing, cost-effective compute
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Streaming Processing</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Azure Stream Analytics</h4>
                <p>Real-time stream processing with SQL-based analytics and windowing</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Stream Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Real-time analytics, windowed aggregations, SQL-based streaming
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Databricks Structured Streaming</h4>
                <p>Managed Databricks with structured streaming capabilities and ML integration</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Stream Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Complex streaming logic, ML-powered streaming, advanced analytics
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Event Hubs + Kafka Streams</h4>
                <p>Kafka-compatible event streaming with Azure integration and management</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Streaming</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Kafka workloads, event streaming, microservices communication
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Functions (real-time transforms)</h4>
                <p>Serverless functions for real-time data processing and enrichment</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Serverless</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Real-time transformations, event-driven processing, low-latency analytics
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>5️⃣ Orchestration & Workflow Management</h3>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>Azure Data Factory Pipelines</h4>
              <p>Visual workflow orchestration with drag-and-drop interface and scheduling</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Orchestration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Visual workflow building, ETL orchestration, scheduled jobs
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Synapse Pipelines</h4>
              <p>Integrated workflow orchestration for Synapse analytics workloads</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Orchestration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Synapse workflow orchestration, integrated analytics pipelines
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Logic Apps</h4>
              <p>Low-code workflow automation with 900+ connectors and visual designer</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Low-Code</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Workflow automation, connector-based integration, low-code orchestration
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Functions (event-driven orchestration)</h4>
              <p>Serverless functions for event-driven orchestration and coordination</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Orchestration</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Event-driven orchestration, lightweight workflows, serverless coordination
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Automation</h4>
              <p>Process automation and configuration management for cloud resources</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Automation</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Process automation, configuration management, scheduled tasks
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Scheduler (legacy)</h4>
              <p>Cron-based job scheduling for periodic task execution</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Job Scheduling</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Cron jobs, scheduled tasks, periodic data processing
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>6️⃣ Data Modeling & Transformation</h3>
          <div class="sub-category">
            <h4>Modeling</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>dbt Core on Azure</h4>
                <p>SQL-based transformation tool with Azure Synapse and Databricks adapters</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data warehouse transformations, analytics engineering, SQL-based pipelines
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>dbt Cloud</h4>
                <p>Managed dbt service with CI/CD, scheduling, and team collaboration</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Team collaboration, managed transformations, automated testing
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Synapse SQL</h4>
                <p>Advanced SQL engine with analytics functions and stored procedures</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">SQL Modeling</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data warehouse analytics, complex queries, advanced SQL features
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Databricks SQL</h4>
                <p>SQL interface for Databricks with analytics and ML capabilities</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">SQL Modeling</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Databricks analytics, SQL-based data exploration, ML integration
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Power BI Dataflows</h4>
                <p>Self-service data preparation and transformation for Power BI users</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Data Preparation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Self-service analytics, Power BI integration, citizen data science
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Transformation Engines</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Databricks (Spark)</h4>
                <p>Managed Spark platform with ML libraries and collaborative notebooks</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Big data transformations, ML pipelines, collaborative data science
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Synapse Spark</h4>
                <p>Serverless Spark service for large-scale data transformations</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Big data transformations, serverless processing, Spark analytics
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Synapse SQL</h4>
                <p>Advanced SQL engine with analytics functions and optimization</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> SQL-based transformations, data warehouse analytics, complex queries
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>ADF Mapping Data Flows</h4>
                <p>Visual data transformation with code-free mapping and processing</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Transformation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Visual transformations, code-free ETL, data mapping
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>7️⃣ Data Quality, Lineage & Observability</h3>
          <div class="sub-category">
            <h4>Data Quality</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Microsoft Purview Data Quality</h4>
                <p>Comprehensive data quality framework with rules and monitoring</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Data Quality</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data quality monitoring, automated validation, quality rules enforcement
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Databricks Expectations</h4>
                <p>Data quality testing framework for Databricks workflows</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Data Quality</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data quality testing, validation automation, quality assurance
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>dbt tests</h4>
                <p>SQL-based data testing framework for data validation and quality checks</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Data Quality</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Data testing, validation automation, quality assurance
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Lineage</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Microsoft Purview Lineage</h4>
                <p>Automated data lineage tracking and visualization for data dependencies</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Data Lineage</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Impact analysis, data governance, compliance reporting, dependency tracking
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Synapse Lineage</h4>
                <p>Native Synapse data lineage for query and dataset relationships</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Data Lineage</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Query optimization, dependency tracking, impact analysis
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Monitoring & Observability</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Azure Monitor</h4>
                <p>Comprehensive monitoring for all Azure services and custom applications</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Monitoring</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Infrastructure monitoring, performance tracking, alerting
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Log Analytics</h4>
                <p>Centralized logging and log analytics for applications and infrastructure</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Logging</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Log aggregation, troubleshooting, audit trails, log analysis
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Application Insights</h4>
                <p>Application performance monitoring and telemetry for web applications</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">APM</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Application monitoring, performance optimization, user experience tracking
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>8️⃣ Metadata, Catalog, Governance</h3>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>Microsoft Purview</h4>
              <p>Unified platform for catalog, lineage, governance, and classification</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Governance Platform</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Data governance, metadata management, compliance, data discovery
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Active Directory (Entra ID)</h4>
              <p>Identity and access management for fine-grained permissions and security</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Access Control</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Access control, security management, compliance, fine-grained permissions
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Key Vault</h4>
              <p>Secure secrets management and encryption key storage</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Security</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Secrets management, encryption key storage, security compliance
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure Policy</h4>
              <p>Policy-based governance for resource compliance and management</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Governance</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Resource governance, compliance enforcement, policy management
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure RBAC</h4>
              <p>Role-based access control for fine-grained permissions management</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Access Control</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Fine-grained access control, role-based permissions, security management
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>9️⃣ Serving & Consumption</h3>
          <div class="sub-category">
            <h4>BI & Analytics</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Power BI</h4>
                <p>Business intelligence platform with interactive dashboards and analytics</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Business Intelligence</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Business intelligence, interactive dashboards, self-service analytics
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Power BI Dataflows</h4>
                <p>Self-service data preparation and transformation for Power BI users</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Data Preparation</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Self-service analytics, data preparation, Power BI integration
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Synapse SQL Serverless</h4>
                <p>Serverless SQL engine for ad-hoc analytics and data exploration</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">SQL Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Ad-hoc analytics, cost-effective queries, data exploration
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Databricks SQL</h4>
                <p>SQL interface for Databricks with analytics and ML capabilities</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">SQL Processing</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Databricks analytics, SQL-based data exploration, ML integration
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Reverse ETL / Operational Analytics</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Hightouch</h4>
                <p>Sync warehouse data back to SaaS tools for operational analytics and activation</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Reverse ETL</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Sales team enablement, operational dashboards, data activation
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Census</h4>
                <p>Operational analytics platform for warehouse-to-app data sync and activation</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Reverse ETL</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Customer success analytics, marketing automation, sales team insights
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>🔟 ML / Feature Serving</h3>
          <div class="cloud-tools">
            <div class="cloud-tool">
              <h4>Azure Machine Learning (Azure ML)</h4>
              <p>Comprehensive ML platform for training, deployment, and managing models</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">ML Platform</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Machine learning pipelines, model training, MLOps, deployment
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Azure ML Feature Store</h4>
              <p>Centralized feature management for ML workflows with low-latency serving</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Feature Store</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Feature engineering, ML workflows, feature reuse, low-latency serving
              </div>
            </div>
            
            <div class="cloud-tool">
              <h4>Databricks Feature Store</h4>
              <p>Centralized feature management for Databricks ML workflows</p>
              <div class="tool-details">
                <span class="cloud-badge">Azure Native</span>
                <span class="type-badge">Feature Store</span>
              </div>
              <div class="when-to-use">
                <strong>When to use:</strong> Feature engineering, ML workflows, feature reuse, Databricks integration
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>1️⃣1️⃣ DevOps, CI/CD, Infrastructure for Data Engineering</h3>
          <div class="sub-category">
            <h4>Infrastructure</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Azure Resource Manager (ARM)</h4>
                <p>Infrastructure as code service for managing Azure resources declaratively</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Infrastructure as Code</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Infrastructure automation, version control, reproducible environments
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Terraform on Azure</h4>
                <p>Multi-cloud infrastructure as code tool with Azure provider support</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">Infrastructure as Code</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Multi-cloud infrastructure, version control, provider-agnostic deployments
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Bicep</h4>
                <p>Domain-specific language for Azure infrastructure as code with better syntax</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Infrastructure as Code</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Azure infrastructure, improved ARM templates, declarative deployments
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>CI/CD</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Azure DevOps Pipelines</h4>
                <p>Continuous integration and delivery service for automated build and deployment</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">CI/CD</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Automated deployments, CI/CD pipelines, release management
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>GitHub Actions</h4>
                <p>CI/CD platform for automated workflows and deployments</p>
                <div class="tool-details">
                  <span class="cloud-badge">Multi-Cloud</span>
                  <span class="type-badge">CI/CD</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Automated workflows, CI/CD pipelines, GitHub integration
                </div>
              </div>
            </div>
          </div>
          
          <div class="sub-category">
            <h4>Compute Runtimes</h4>
            <div class="cloud-tools">
              <div class="cloud-tool">
                <h4>Azure Kubernetes Service (AKS)</h4>
                <p>Managed Kubernetes cluster for container orchestration and scaling</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Container Orchestration</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Complex applications, microservices, container orchestration
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Container Instances (ACI)</h4>
                <p>Serverless containers for quick application deployment and scaling</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Container Platform</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Serverless containers, quick deployments, microservices
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure Functions</h4>
                <p>Serverless compute for event-driven functions and lightweight processing</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Serverless</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Event-driven processing, lightweight functions, serverless architecture
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure App Service</h4>
                <p>Managed web application platform with automatic scaling and deployment</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Web Platform</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Web applications, API hosting, managed platform services
                </div>
              </div>
              
              <div class="cloud-tool">
                <h4>Azure VMs</h4>
                <p>Virtual machines for custom data processing workloads and full control</p>
                <div class="tool-details">
                  <span class="cloud-badge">Azure Native</span>
                  <span class="type-badge">Virtual Machines</span>
                </div>
                <div class="when-to-use">
                  <strong>When to use:</strong> Custom software, specialized workloads, full control, HPC applications
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="category-section">
          <h3>🧭 End-to-End Azure Data Engineering Pipeline (Ordered)</h3>
          <div class="pipeline-summary">
            <table class="pipeline-table">
              <thead>
                <tr>
                  <th>Stage</th>
                  <th>Azure Tools</th>
                  <th>Description</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td><strong>Ingest</strong></td>
                  <td>ADF, Event Hubs, IoT Hub, DMS</td>
                  <td>ETL pipelines, event streaming, IoT ingestion, database migration</td>
                </tr>
                <tr>
                  <td><strong>Land</strong></td>
                  <td>ADLS Gen2</td>
                  <td>Data lake with hierarchical namespace and storage tiers</td>
                </tr>
                <tr>
                  <td><strong>Process</strong></td>
                  <td>Databricks, Synapse Spark, Synapse SQL</td>
                  <td>Big data analytics, Spark processing, SQL transformations</td>
                </tr>
                <tr>
                  <td><strong>Model</strong></td>
                  <td>dbt, Synapse SQL, Databricks SQL</td>
                  <td>Analytics engineering, SQL modeling, collaborative analytics</td>
                </tr>
                <tr>
                  <td><strong>Orchestrate</strong></td>
                  <td>ADF Pipelines, Synapse Pipelines</td>
                  <td>Visual workflow orchestration, integrated pipeline management</td>
                </tr>
                <tr>
                  <td><strong>Validate</strong></td>
                  <td>Purview Data Quality</td>
                  <td>Data quality monitoring, automated validation, compliance</td>
                </tr>
                <tr>
                  <td><strong>Catalog</strong></td>
                  <td>Purview</td>
                  <td>Metadata management, data discovery, governance</td>
                </tr>
                <tr>
                  <td><strong>Serve</strong></td>
                  <td>Power BI, Azure ML</td>
                  <td>Business intelligence, machine learning serving, analytics delivery</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  </div> <!-- Close Azure section div -->

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
</script>

<section class="comparison-section">
    <h2 class="cloud-title">🌐 Unified Cloud Data Engineering Tools Comparison</h2>
    <p class="cloud-description">Direct comparison of equivalent data engineering tools across AWS, GCP, and Azure</p>
    
    <div class="comparison-categories">
      <div class="category-section">
        <h3>🧱 Compute Engines (Spark / Hadoop / Distributed Processing)</h3>
        <div class="comparison-table-wrapper">
          <table class="comparison-table">
            <thead>
              <tr>
                <th>Category</th>
                <th>AWS</th>
                <th>GCP</th>
                <th>Azure</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>Managed Spark / Hadoop</strong></td>
                <td><strong>EMR</strong></td>
                <td><strong>Dataproc</strong></td>
                <td><strong>Azure Databricks</strong> / <strong>Synapse Spark</strong></td>
              </tr>
              <tr>
                <td><strong>Serverless SQL on Data Lake</strong></td>
                <td>Athena</td>
                <td>BigQuery</td>
                <td>Synapse Serverless SQL</td>
              </tr>
              <tr>
                <td><strong>General Batch Compute</strong></td>
                <td>AWS Batch</td>
                <td>Dataflow (batch)</td>
                <td>Azure Batch</td>
              </tr>
              <tr>
                <td><strong>Container Compute</strong></td>
                <td>ECS / EKS</td>
                <td>GKE</td>
                <td>AKS</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
      
      <div class="category-section">
        <h3>🔄 Streaming Ingestion & Processing</h3>
        <div class="comparison-table-wrapper">
          <table class="comparison-table">
            <thead>
              <tr>
                <th>Category</th>
                <th>AWS</th>
                <th>GCP</th>
                <th>Azure</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>Event Streaming (Kafka-like)</strong></td>
                <td>MSK (Managed Kafka)</td>
                <td>Pub/Sub</td>
                <td>Event Hubs</td>
              </tr>
              <tr>
                <td><strong>Streaming Ingestion</strong></td>
                <td>Kinesis Data Streams</td>
                <td>Pub/Sub</td>
                <td>Event Hubs / IoT Hub</td>
              </tr>
              <tr>
                <td><strong>Streaming ETL</strong></td>
                <td>Kinesis Data Firehose</td>
                <td>Dataflow (streaming)</td>
                <td>Stream Analytics</td>
              </tr>
              <tr>
                <td><strong>Streaming Compute Engine</strong></td>
                <td>Kinesis Data Analytics (Flink)</td>
                <td>Dataflow (Beam)</td>
                <td>Stream Analytics / Databricks Structured Streaming</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
      
      <div class="category-section">
        <h3>📥 Ingestion (Batch, CDC, File Transfer)</h3>
        <div class="comparison-table-wrapper">
          <table class="comparison-table">
            <thead>
              <tr>
                <th>Category</th>
                <th>AWS</th>
                <th>GCP</th>
                <th>Azure</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>Batch ETL / ELT</strong></td>
                <td>Glue ETL</td>
                <td>Data Fusion</td>
                <td>Data Factory</td>
              </tr>
              <tr>
                <td><strong>CDC / Database Migration</strong></td>
                <td>DMS</td>
                <td>Datastream</td>
                <td>Azure DMS</td>
              </tr>
              <tr>
                <td><strong>File Transfer</strong></td>
                <td>DataSync / Transfer Family</td>
                <td>Storage Transfer Service</td>
                <td>Data Box / ADF Copy</td>
              </tr>
              <tr>
                <td><strong>Event-driven ingestion</strong></td>
                <td>Lambda</td>
                <td>Cloud Functions</td>
                <td>Azure Functions</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
      
      <div class="category-section">
        <h3>🗄️ Storage (Lake, Warehouse, Table Formats)</h3>
        <div class="comparison-table-wrapper">
          <table class="comparison-table">
            <thead>
              <tr>
                <th>Category</th>
                <th>AWS</th>
                <th>GCP</th>
                <th>Azure</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>Object Storage (Data Lake)</strong></td>
                <td>S3</td>
                <td>GCS</td>
                <td>ADLS Gen2</td>
              </tr>
              <tr>
                <td><strong>Data Warehouse</strong></td>
                <td>Redshift</td>
                <td>BigQuery</td>
                <td>Synapse SQL Pool</td>
              </tr>
              <tr>
                <td><strong>Lakehouse Table Formats</strong></td>
                <td>Iceberg / Hudi / Delta Lake</td>
                <td>BigLake + Iceberg/Delta/Hudi</td>
                <td>Delta Lake (native) / Iceberg / Hudi</td>
              </tr>
              <tr>
                <td><strong>Metadata Catalog</strong></td>
                <td>Glue Catalog</td>
                <td>Dataplex / Data Catalog</td>
                <td>Purview</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
      
      <div class="category-section">
        <h3>🧮 Transformation & Modeling</h3>
        <div class="comparison-table-wrapper">
          <table class="comparison-table">
            <thead>
              <tr>
                <th>Category</th>
                <th>AWS</th>
                <th>GCP</th>
                <th>Azure</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>SQL Transform Engine</strong></td>
                <td>Redshift SQL / Athena</td>
                <td>BigQuery SQL</td>
                <td>Synapse SQL / Databricks SQL</td>
              </tr>
              <tr>
                <td><strong>Spark Transform Engine</strong></td>
                <td>EMR / Glue</td>
                <td>Dataproc</td>
                <td>Databricks / Synapse Spark</td>
              </tr>
              <tr>
                <td><strong>Low-code Transform</strong></td>
                <td>Glue DataBrew</td>
                <td>DataPrep (Trifacta)</td>
                <td>ADF Mapping Data Flows</td>
              </tr>
              <tr>
                <td><strong>Data Modeling</strong></td>
                <td>dbt</td>
                <td>dbt</td>
                <td>dbt</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
      
      <div class="category-section">
        <h3>🧭 Orchestration & Workflow</h3>
        <div class="comparison-table-wrapper">
          <table class="comparison-table">
            <thead>
              <tr>
                <th>Category</th>
                <th>AWS</th>
                <th>GCP</th>
                <th>Azure</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>Managed Airflow</strong></td>
                <td>MWAA</td>
                <td>Cloud Composer</td>
                <td>(No native Airflow)</td>
              </tr>
              <tr>
                <td><strong>Serverless Orchestration</strong></td>
                <td>Step Functions</td>
                <td>Workflows</td>
                <td>Logic Apps</td>
              </tr>
              <tr>
                <td><strong>Scheduling</strong></td>
                <td>CloudWatch Events</td>
                <td>Cloud Scheduler</td>
                <td>Azure Scheduler (legacy)</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
      
      <div class="category-section">
        <h3>🧪 Data Quality, Lineage, Observability</h3>
        <div class="comparison-table-wrapper">
          <table class="comparison-table">
            <thead>
              <tr>
                <th>Category</th>
                <th>AWS</th>
                <th>GCP</th>
                <th>Azure</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>Data Quality</strong></td>
                <td>Glue Data Quality / Deequ</td>
                <td>Dataplex Data Quality</td>
                <td>Purview Data Quality</td>
              </tr>
              <tr>
                <td><strong>Lineage</strong></td>
                <td>Glue Lineage</td>
                <td>Dataplex Lineage</td>
                <td>Purview Lineage</td>
              </tr>
              <tr>
                <td><strong>Monitoring</strong></td>
                <td>CloudWatch</td>
                <td>Cloud Monitoring</td>
                <td>Azure Monitor</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
      
      <div class="category-section">
        <h3>📊 BI, Analytics, ML Serving</h3>
        <div class="comparison-table-wrapper">
          <table class="comparison-table">
            <thead>
              <tr>
                <th>Category</th>
                <th>AWS</th>
                <th>GCP</th>
                <th>Azure</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>BI Tools</strong></td>
                <td>QuickSight</td>
                <td>Looker / Looker Studio</td>
                <td>Power BI</td>
              </tr>
              <tr>
                <td><strong>ML Platform</strong></td>
                <td>SageMaker</td>
                <td>Vertex AI</td>
                <td>Azure ML</td>
              </tr>
              <tr>
                <td><strong>Feature Store</strong></td>
                <td>SageMaker Feature Store</td>
                <td>Vertex Feature Store</td>
                <td>Azure ML Feature Store / Databricks Feature Store</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
      
      <div class="category-section">
        <h3>⭐ Most Useful 1:1 Mappings (Quick Reference)</h3>
        <div class="comparison-table-wrapper">
          <table class="comparison-table highlight-mapping">
            <thead>
              <tr>
                <th>AWS</th>
                <th>GCP</th>
                <th>Azure</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>EMR</strong></td>
                <td><strong>Dataproc</strong></td>
                <td><strong>Azure Databricks / Synapse Spark</strong></td>
              </tr>
              <tr>
                <td><strong>Kinesis</strong></td>
                <td><strong>Pub/Sub</strong></td>
                <td><strong>Event Hubs</strong></td>
              </tr>
              <tr>
                <td><strong>Glue ETL</strong></td>
                <td><strong>Dataflow / Data Fusion</strong></td>
                <td><strong>Data Factory</strong></td>
              </tr>
              <tr>
                <td><strong>Redshift</strong></td>
                <td><strong>BigQuery</strong></td>
                <td><strong>Synapse SQL</strong></td>
              </tr>
              <tr>
                <td><strong>Athena</strong></td>
                <td><strong>BigQuery (external tables)</strong></td>
                <td><strong>Synapse Serverless SQL</strong></td>
              </tr>
              <tr>
                <td><strong>Glue Catalog</strong></td>
                <td><strong>Dataplex / Data Catalog</strong></td>
                <td><strong>Purview</strong></td>
              </tr>
              <tr>
                <td><strong>Step Functions</strong></td>
                <td><strong>Workflows</strong></td>
                <td><strong>Logic Apps</strong></td>
              </tr>
              <tr>
                <td><strong>QuickSight</strong></td>
                <td><strong>Looker</strong></td>
                <td><strong>Power BI</strong></td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </section>
    
    <div class="tool-categories">
      <div class="category-section">
        <h3>Data Warehouses & Lakehouses</h3>
        <div class="cloud-tools">
          <div class="cloud-tool">
            <h4><a href="{{ site.baseurl }}/tools/#snowflake">Snowflake</a></h4>
            <p>Cloud data platform with automatic scaling, performance, and data sharing</p>
            <div class="tool-details">
              <span class="cloud-badge">Multi-Cloud</span>
              <span class="type-badge">Data Warehouse</span>
            </div>
            <div class="when-to-use">
              <strong>When to use:</strong> Enterprise analytics, data warehousing, multi-cloud data strategy
            </div>
          </div>
          
          <div class="cloud-tool">
            <h4><a href="{{ site.baseurl }}/tools/#databricks">Databricks</a></h4>
            <p>Unified analytics platform for big data, machine learning, and collaborative data science</p>
            <div class="tool-details">
              <span class="cloud-badge">Multi-Cloud</span>
              <span class="type-badge">Analytics Platform</span>
            </div>
            <div class="when-to-use">
              <strong>When to use:</strong> Big data analytics, machine learning pipelines, collaborative data science
            </div>
          </div>
        </div>
      </div>
      
      <div class="category-section">
        <h3>Data Transformation & Orchestration</h3>
        <div class="cloud-tools">
          <div class="cloud-tool">
            <h4><a href="{{ site.baseurl }}/tools/#dbt">dbt</a></h4>
            <p>SQL-first transformation tool that brings software engineering practices to data analytics</p>
            <div class="tool-details">
              <span class="cloud-badge">Multi-Cloud</span>
              <span class="type-badge">Transformation</span>
            </div>
            <div class="when-to-use">
              <strong>When to use:</strong> Data warehouse transformations, analytics engineering, SQL-based pipeline development
            </div>
          </div>
          
          <div class="cloud-tool">
            <h4><a href="{{ site.baseurl }}/tools/#fivetran">Fivetran</a></h4>
            <p>Fully managed data ingestion service with 300+ pre-built connectors for SaaS platforms</p>
            <div class="tool-details">
              <span class="cloud-badge">Multi-Cloud</span>
              <span class="type-badge">ELT Platform</span>
            </div>
            <div class="when-to-use">
              <strong>When to use:</strong> Rapid SaaS data integration, warehouse loading, automated schema management
            </div>
          </div>
        </div>
      </div>
      
      <div class="category-section">
        <h3>Orchestration & Workflow</h3>
        <div class="cloud-tools">
          <div class="cloud-tool">
            <h4><a href="{{ site.baseurl }}/tools/#prefect">Prefect</a></h4>
            <p>Modern workflow orchestration platform with native Python support and dynamic scaling</p>
            <div class="tool-details">
              <span class="cloud-badge">Multi-Cloud</span>
              <span class="type-badge">Orchestration</span>
            </div>
            <div class="when-to-use">
              <strong>When to use:</strong> Building reliable data pipelines, real-time workflow monitoring, infrastructure automation
            </div>
          </div>
          
          <div class="cloud-tool">
            <h4><a href="{{ site.baseurl }}/tools/#dagster">Dagster</a></h4>
            <p>Data-aware orchestration platform that understands pipeline dependencies and data assets</p>
            <div class="tool-details">
              <span class="cloud-badge">Multi-Cloud</span>
              <span class="type-badge">Orchestration</span>
            </div>
            <div class="when-to-use">
              <strong>When to use:</strong> Managing complex data workflows, data lineage tracking, asset governance
            </div>
          </div>
        </div>
      </div>
      
      <div class="category-section">
        <h3>Data Quality & Observability</h3>
        <div class="cloud-tools">
          <div class="cloud-tool">
            <h4><a href="{{ site.baseurl }}/tools/#monte-carlo">Monte Carlo</a></h4>
            <p>Data observability platform providing end-to-end visibility into data pipelines</p>
            <div class="tool-details">
              <span class="cloud-badge">Multi-Cloud</span>
              <span class="type-badge">Monitoring</span>
            </div>
            <div class="when-to-use">
              <strong>When to use:</strong> Data pipeline monitoring, freshness tracking, data reliability assurance
            </div>
          </div>
          
          <div class="cloud-tool">
            <h4><a href="{{ site.baseurl }}/tools/#great-expectations">Great Expectations</a></h4>
            <p>Comprehensive data validation framework for ensuring data quality and reliability</p>
            <div class="tool-details">
              <span class="cloud-badge">Multi-Cloud</span>
              <span class="type-badge">Data Quality</span>
            </div>
            <div class="when-to-use">
              <strong>When to use:</strong> Data quality testing, pipeline validation, automated data documentation
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="strategy-section">
    <h2>🎯 Cloud Strategy Guidance</h2>
    
    <div class="strategy-grid">
      <div class="strategy-item">
        <h3>Single Cloud Strategy</h3>
        <p><strong>Best for:</strong> Simplicity, performance, reduced complexity</p>
        <div class="strategy-details">
          <h4>Advantages:</h4>
          <ul>
            <li>Native integration and performance</li>
            <li>Unified billing and support</li>
            <li>Simplified security and compliance</li>
            <li>Better cloud-specific features</li>
          </ul>
          <h4>Considerations:</h4>
          <ul>
            <li>Vendor lock-in risks</li>
            <li>Limited flexibility across clouds</li>
            <li>Potential cost optimization challenges</li>
          </ul>
        </div>
      </div>
      
      <div class="strategy-item">
        <h3>Multi-Cloud Strategy</h3>
        <p><strong>Best for:</strong> Flexibility, cost optimization, risk mitigation</p>
        <div class="strategy-details">
          <h4>Advantages:</h4>
          <ul>
            <li>Vendor diversity and flexibility</li>
            <li>Cost optimization across providers</li>
            <li>Reduced vendor lock-in</li>
            <li>Best-of-breed tool selection</li>
          </ul>
          <h4>Considerations:</h4>
          <ul>
            <li>Increased complexity</li>
            <li>Multi-cloud security management</li>
            <li>Data transfer costs between clouds</li>
            <li>Integration complexity</li>
          </ul>
        </div>
      </div>
      
      <div class="strategy-item">
        <h3>Hybrid Approach</h3>
        <p><strong>Best for:</strong> Balance of simplicity and flexibility</p>
        <div class="strategy-details">
          <h4>Recommended Mix:</h4>
          <ul>
            <li><strong>Storage:</strong> Native cloud storage + Multi-cloud warehouse</li>
            <li><strong>Processing:</strong> Native for cloud-specific features, Multi-cloud for standard workloads</li>
            <li><strong>Orchestration:</strong> Multi-cloud for flexibility</li>
          </ul>
          <h4>Benefits:</h4>
          <ul>
            <li>Optimized performance where it matters</li>
            <li>Flexibility for standard workflows</li>
            <li>Cost optimization opportunities</li>
            <li>Reduced vendor lock-in</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <section class="next-steps">
    <h2>Next Steps</h2>
    <div class="step-navigation">
      <div class="step-card">
        <h3>← Back to Tools</h3>
        <a href="{{ site.baseurl }}/tools/" class="step-link">Browse All Tools</a>
      </div>
      
      <div class="step-card">
        <h3>🎯 Explore Layers</h3>
        <p>Understand how these tools fit into the data engineering lifecycle</p>
        <a href="{{ site.baseurl }}/layers/" class="step-link primary">View Data Layers</a>
      </div>
    </div>
  </section>
</div>

<style>
.cloud-header {
  background: var(--background-secondary);
  padding: 1rem 1.5rem;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: background-color 0.2s ease;
  border-radius: 8px;
  margin-bottom: 1rem;
  border: 1px solid var(--border-color);
}

.cloud-header:hover {
  background: var(--background-tertiary);
}

.cloud-header h2 {
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
  padding: 1rem;
  background: white;
  border-radius: 0 0 8px 8px;
  margin-bottom: 2rem;
}

.aws-section, .gcp-section, .azure-section {
  margin-bottom: 2rem;
}
</style>
