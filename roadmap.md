---
layout: default
title: "Data Engineering Roadmap"
---

<div class="page-header">
  <h1 class="page-title">Data Engineering Roadmap</h1>
  <p class="page-subtitle">Your guide from foundations to advanced data systems</p>
</div>

<div class="container">
  <section class="roadmap-section">
    <h2 class="section-title">🏗️ Foundations</h2>
    <p class="section-description">Start here if you're new to data engineering</p>
    
    <div class="foundation-grid">
      <div class="foundation-item" onclick="showConcepts('sql')">
        <h3>SQL</h3>
        <p>The language of data. Master SELECT, JOIN, GROUP BY, and window functions.</p>
        <div class="click-hint">💡 Click to see core concepts</div>
        <div class="next-step">Next step → <a href="#core-engineering">Core Engineering</a></div>
      </div>
      
      <div class="foundation-item" onclick="showConcepts('python')">
        <h3>Python</h3>
        <p>Essential for data manipulation, automation, and modern data tools.</p>
        <div class="click-hint">💡 Click to see core concepts</div>
        <div class="next-step">Next step → <a href="#core-engineering">Core Engineering</a></div>
      </div>
      
      <div class="foundation-item" onclick="showConcepts('pyspark')">
        <h3>Apache Spark (PySpark)</h3>
        <p>Big data processing framework for distributed computing and large-scale data analysis.</p>
        <div class="click-hint">💡 Click to see core concepts</div>
        <div class="next-step">Next step → <a href="#core-engineering">Core Engineering</a></div>
      </div>
      
      <div class="foundation-item" onclick="showConcepts('linux')">
        <h3>Linux</h3>
        <p>Command-line skills and shell scripting for data pipeline operations.</p>
        <div class="click-hint">💡 Click to see core concepts</div>
        <div class="next-step">Next step → <a href="#core-engineering">Core Engineering</a></div>
      </div>
    </div>
  </section>

  <!-- Core Concepts Modal -->
  <div id="concepts-modal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeConcepts()">&times;</span>
      <h2 id="modal-title">Core Concepts</h2>
      <div id="modal-body">
        <!-- Concepts will be loaded here -->
      </div>
    </div>
  </div>

  <script>
  // Core Concepts Data
  const coreConcepts = {
    sql: {
      title: "SQL - Top 20% Concepts (80% Coverage)",
      concepts: [
        { name: "Basic Queries", description: "SELECT, FROM, WHERE, ORDER BY, LIMIT" },
        { name: "Aggregations", description: "COUNT, SUM, AVG, MAX, MIN with GROUP BY" },
        { name: "Joins", description: "INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL OUTER JOIN" },
        { name: "Subqueries", description: "Nested queries and correlated subqueries" },
        { name: "CTEs", description: "Common Table Expressions (WITH clauses)" },
        { name: "Window Functions", description: "ROW_NUMBER(), RANK(), LAG(), LEAD()" },
        { name: "Data Types", description: "VARCHAR, INT, DATE, TIMESTAMP, BOOLEAN" },
        { name: "Indexes", description: "Primary keys, foreign keys, and performance indexes" }
      ]
    },
    python: {
      title: "Python - Top 20% Concepts (80% Coverage)",
      concepts: [
        { name: "Data Structures", description: "Lists, dictionaries, tuples, sets, and their methods" },
        { name: "List Comprehensions", description: "[x for x in iterable if condition] patterns" },
        { name: "Functions", description: "def, return, parameters, *args, **kwargs" },
        { name: "Lambda Functions", description: "Anonymous functions for quick operations" },
        { name: "Pandas Basics", description: "read_csv(), DataFrame, select, filter, groupby" },
        { name: "File Operations", description: "open(), read(), write(), with statements" },
        { name: "Error Handling", description: "try, except, finally, raise exceptions" },
        { name: "Modules & Imports", description: "import, from, pip, virtual environments" }
      ]
    },
    pyspark: {
      title: "PySpark - Top 20% Concepts (80% Coverage)",
      concepts: [
        { name: "SparkSession", description: "Creating and configuring Spark sessions" },
        { name: "DataFrame Basics", description: "Creating, reading, and basic operations" },
        { name: "Transformations", description: "select(), filter(), withColumn(), drop()" },
        { name: "Actions", description: "show(), collect(), count(), take(), first()" },
        { name: "Aggregations", description: "groupBy(), agg(), sum(), count(), avg()" },
        { name: "Joins", description: "Inner, left, right joins between DataFrames" },
        { name: "File Formats", description: "CSV, JSON, Parquet, ORC read/write operations" },
        { name: "Lazy Evaluation", description: "Understanding transformations vs actions" }
      ]
    },
    linux: {
      title: "Linux - Top 20% Concepts (80% Coverage)",
      concepts: [
        { name: "File Navigation", description: "ls, cd, pwd, find, locate commands" },
        { name: "File Operations", description: "cp, mv, rm, mkdir, touch, chmod" },
        { name: "Text Processing", description: "grep, sed, awk, sort, uniq, wc" },
        { name: "Process Management", description: "ps, top, kill, killall, jobs, bg, fg" },
        { name: "Permissions", description: "chmod, chown, chgrp, umask concepts" },
        { name: "Shell Scripting", description: "Variables, loops, conditionals, functions" },
        { name: "Pipes & Redirection", description: "|, >, >>, <, 2>&1 concepts" },
        { name: "System Monitoring", description: "df, du, free, uptime, netstat" }
      ]
    }
  };

  function showConcepts(topic) {
    const modal = document.getElementById('concepts-modal');
    const modalTitle = document.getElementById('modal-title');
    const modalBody = document.getElementById('modal-body');
    
    const data = coreConcepts[topic];
    modalTitle.textContent = data.title;
    
    let conceptsHTML = '<div class="concepts-grid">';
    data.concepts.forEach((concept, index) => {
      conceptsHTML += `
        <div class="concept-item">
          <div class="concept-number">${index + 1}</div>
          <div class="concept-content">
            <h4>${concept.name}</h4>
            <p>${concept.description}</p>
          </div>
        </div>
      `;
    });
    conceptsHTML += '</div>';
    
    modalBody.innerHTML = conceptsHTML;
    modal.style.display = 'block';
  }

  function closeConcepts() {
    document.getElementById('concepts-modal').style.display = 'none';
  }

  // Close modal when clicking outside
  window.onclick = function(event) {
    const modal = document.getElementById('concepts-modal');
    if (event.target == modal) {
      modal.style.display = 'none';
    }
  }
  </script>

  <section class="roadmap-section" id="core-engineering">
    <h2 class="section-title">⚙️ Core Data Engineering</h2>
    <p class="section-description">Essential concepts and tools for data professionals</p>
    
    <div class="core-grid">
      <div class="core-item">
        <h3>Data Modeling</h3>
        <p>Designing schemas, relationships, and data architectures.</p>
        <div class="next-step">Next step → <a href="#layers">Data Layers</a></div>
      </div>
      
      <div class="core-item">
        <h3>ETL / ELT</h3>
        <p>Extract, Transform, Load patterns and modern data pipelines.</p>
        <div class="next-step">Next step → <a href="#layers">Data Layers</a></div>
      </div>
    </div>
  </section>

  <section class="roadmap-section" id="ai-ml-engineering">
    <h2 class="section-title">🤖 AI/ML Data Engineering</h2>
    <p class="section-description">Optional: For engineers interested in ML infrastructure and pipelines</p>
    
    <div class="core-grid">
      <div class="core-item">
        <h3>Vector Databases</h3>
        <p>Pinecone, Weaviate, Chroma - Storage for AI embeddings and semantic search.</p>
        <div class="next-step">Next step → <a href="#real-time-streaming">Real-time Streaming</a></div>
      </div>
      
      <div class="core-item">
        <h3>Feature Stores</h3>
        <p>Feast, Tecton - Centralized feature management for ML models.</p>
        <div class="next-step">Next step → <a href="#real-time-streaming">Real-time Streaming</a></div>
      </div>
      
      <div class="core-item">
        <h3>ML Pipelines</h3>
        <p>MLflow, Kubeflow, SageMaker - Orchestrate ML training and deployment.</p>
        <div class="next-step">Next step → <a href="#real-time-streaming">Real-time Streaming</a></div>
      </div>
      
      <div class="core-item">
        <h3>Model Serving</h3>
        <p>BentoML, TorchServe, KServe - Deploy and serve ML models at scale.</p>
        <div class="next-step">Next step → <a href="#real-time-streaming">Real-time Streaming</a></div>
      </div>
    </div>
  </section>

  <section class="roadmap-section" id="real-time-streaming">
    <h2 class="section-title">⚡ Real-time Streaming</h2>
    <p class="section-description">Modern stream processing and real-time data systems</p>
    
    <div class="core-grid">
      <div class="core-item">
        <h3>Stream Processing</h3>
        <p>Kafka, Flink, Pulsar - Real-time data processing and event streaming.</p>
        <div class="next-step">Next step → <a href="#data-quality">Data Quality</a></div>
      </div>
      
      <div class="core-item">
        <h3>Change Data Capture</h3>
        <p>Debezium, Fivetran CDC - Capture database changes in real-time.</p>
        <div class="next-step">Next step → <a href="#data-quality">Data Quality</a></div>
      </div>
      
      <div class="core-item">
        <h3>Real-time Analytics</h3>
        <p>Druid, Pinot, ClickHouse - Low-latency analytics on streaming data.</p>
        <div class="next-step">Next step → <a href="#data-quality">Data Quality</a></div>
      </div>
    </div>
  </section>

  <section class="roadmap-section" id="data-quality">
    <h2 class="section-title">🔒 Data Quality & Governance</h2>
    <p class="section-description">Essential practices for reliable data systems</p>
    
    <div class="core-grid">
      <div class="core-item">
        <h3>Data Observability</h3>
        <p>Monte Carlo, Great Expectations - Monitor and ensure data quality.</p>
        <div class="next-step">Next step → <a href="#cloud-economics">Cloud Economics</a></div>
      </div>
      
      <div class="core-item">
        <h3>Data Contracts</h3>
        <p>Define and enforce data schemas and quality standards.</p>
        <div class="next-step">Next step → <a href="#cloud-economics">Cloud Economics</a></div>
      </div>
      
      <div class="core-item">
        <h3>Privacy Engineering</h3>
        <p>PII handling, GDPR compliance, and data privacy practices.</p>
        <div class="next-step">Next step → <a href="#cloud-economics">Cloud Economics</a></div>
      </div>
    </div>
  </section>

  <section class="roadmap-section" id="cloud-economics">
    <h2 class="section-title">💰 Cloud Economics</h2>
    <p class="section-description">Cost optimization and financial operations</p>
    
    <div class="core-grid">
      <div class="core-item">
        <h3>Cost Optimization</h3>
        <p>Spot instances, autoscaling, resource efficiency strategies.</p>
        <div class="next-step">Next step → <a href="#learning-paths">Learning Paths</a></div>
      </div>
      
      <div class="core-item">
        <h3>Serverless Trade-offs</h3>
        <p>When to use serverless vs managed services.</p>
        <div class="next-step">Next step → <a href="#learning-paths">Learning Paths</a></div>
      </div>
      
      <div class="core-item">
        <h3>FinOps Basics</h3>
        <p>Cost monitoring, budgeting, and financial accountability.</p>
        <div class="next-step">Next step → <a href="#learning-paths">Learning Paths</a></div>
      </div>
    </div>
  </section>

  <section class="roadmap-section" id="layers">
    <h2 class="section-title">🏢 Data Engineering Layers</h2>
    <p class="section-description">Understanding the complete data lifecycle</p>
    
    <div class="layers-grid">
      <div class="layer-item">
        <h3><a href="{{ site.baseurl }}/layers/data-sources/">Data Sources</a></h3>
        <p>Where data originates and how to access it</p>
        <div class="next-step">Next step → <a href="{{ site.baseurl }}/layers/data-ingestion/">Data Ingestion</a></div>
      </div>
      
      <div class="layer-item">
        <h3><a href="{{ site.baseurl }}/layers/data-ingestion/">Data Ingestion</a></h3>
        <p>Moving data from sources to storage systems</p>
        <div class="next-step">Next step → <a href="{{ site.baseurl }}/layers/data-processing/">Data Processing</a></div>
      </div>
      
      <div class="layer-item">
        <h3><a href="{{ site.baseurl }}/layers/data-processing/">Data Processing</a></h3>
        <p>Transforming raw data into valuable insights</p>
        <div class="next-step">Next step → <a href="{{ site.baseurl }}/layers/data-storage/">Data Storage</a></div>
      </div>
      
      <div class="layer-item">
        <h3><a href="{{ site.baseurl }}/layers/data-storage/">Data Storage</a></h3>
        <p>Storing processed data for analysis and consumption</p>
        <div class="next-step">Next step → <a href="{{ site.baseurl }}/layers/data-consumption/">Data Consumption</a></div>
      </div>
      
      <div class="layer-item">
        <h3><a href="{{ site.baseurl }}/layers/data-consumption/">Data Consumption</a></h3>
        <p>Making data accessible to users and applications</p>
        <div class="next-step">Final step → <a href="{{ site.baseurl }}/tools/">Explore Tools</a></div>
      </div>
    </div>
  </section>

  <section class="roadmap-section">
    <h2 class="section-title">🛠️ Explore Tools</h2>
    <p class="section-description">Find the right tools for each layer</p>
    
    <div class="tools-cta">
      <a href="{{ site.baseurl }}/tools/" class="cta-button">Browse Complete Tools Catalog</a>
    </div>
  </section>

  <section class="roadmap-section" id="learning-paths">
    <h2 class="section-title">🎯 Learning Paths</h2>
    <p class="section-description">Common journeys and recommendations</p>
    
    <div class="path-grid">
      <div class="path-item">
        <h3>Beginner Path</h3>
        <p>SQL → Python → Batch Processing (PySpark) → Basic ETL → Simple BI → Data Quality Basics → Streaming Fundamentals</p>
        <div class="time-estimate">6-9 months</div>
      </div>
      
      <div class="path-item">
        <h3>Analytics Engineer</h3>
        <p>Advanced SQL → Data Modeling → Advanced Batch Processing (dbt) → Real-time Analytics → BI Tools → ML Data Prep</p>
        <div class="time-estimate">9-15 months</div>
      </div>
      
      <div class="path-item">
        <h3>Data Platform Engineer</h3>
        <p>Python → Batch Architecture (Spark) → Streaming Architecture → Orchestration → Cloud Architecture → DevOps → ML Ops → Cost Optimization</p>
        <div class="time-estimate">15-24 months</div>
      </div>
      
      <div class="path-item">
        <h3>ML Data Engineer</h3>
        <p>SQL → Python → Batch Processing → Vector Databases → Feature Stores → ML Pipelines → Model Serving</p>
        <div class="time-estimate">12-18 months</div>
      </div>
    </div>
  </section>
</div>
