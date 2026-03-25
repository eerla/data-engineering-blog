---
layout: default
title: "Database Landscape Guide"
---

<div class="page-header">
  <h1 class="page-title">Database Landscape Guide</h1>
  <p class="page-subtitle">Complete guide to database types, use cases, and selection criteria</p>
</div>

<div class="container">
  <!-- Database Selection Tool -->
  <section class="database-section">
    <h2 class="section-title">🎯 Database Selection Tool</h2>
    <p class="section-description">Find the right database for your use case</p>
    
    <div class="selection-tool">
      <div class="filter-section">
        <h3>What's your primary use case?</h3>
        <div class="filter-options">
          <label class="filter-option">
            <input type="radio" name="use-case" value="transactions" onchange="filterDatabases()">
            <span>Transactional Systems (OLTP)</span>
          </label>
          <label class="filter-option">
            <input type="radio" name="use-case" value="analytics" onchange="filterDatabases()">
            <span>Analytics & Reporting (OLAP)</span>
          </label>
          <label class="filter-option">
            <input type="radio" name="use-case" value="real-time" onchange="filterDatabases()">
            <span>Real-time Applications</span>
          </label>
          <label class="filter-option">
            <input type="radio" name="use-case" value="ai-ml" onchange="filterDatabases()">
            <span>AI/ML Applications</span>
          </label>
          <label class="filter-option">
            <input type="radio" name="use-case" value="content" onchange="filterDatabases()">
            <span>Content Management</span>
          </label>
        </div>
      </div>
      
      <div class="filter-section">
        <h3>What's your data scale?</h3>
        <div class="filter-options">
          <label class="filter-option">
            <input type="radio" name="scale" value="small" onchange="filterDatabases()">
            <span>Small (< 1M records)</span>
          </label>
          <label class="filter-option">
            <input type="radio" name="scale" value="medium" onchange="filterDatabases()">
            <span>Medium (1M-100M records)</span>
          </label>
          <label class="filter-option">
            <input type="radio" name="scale" value="large" onchange="filterDatabases()">
            <span>Large (100M+ records)</span>
          </label>
        </div>
      </div>
      
      <!-- Results Section -->
      <div id="selection-results" class="selection-results" style="display: none;">
        <h3>Recommended Databases</h3>
        <div id="results-content">
          <!-- Results will be populated here -->
        </div>
      </div>
    </div>
  </section>

  <!-- Database Categories Overview -->
  <section class="database-section">
    <h2 class="section-title">📊 Database Categories</h2>
    <p class="section-description">Understanding the different types of databases</p>
    
    <div class="category-grid">
      <div class="category-card" onclick="showCategoryDetails('oltp')">
        <h3>OLTP Databases</h3>
        <p>Online Transaction Processing - Optimized for high-volume transactions</p>
        <div class="category-features">
          <span class="feature-tag">ACID Compliance</span>
          <span class="feature-tag">Row-based Storage</span>
          <span class="feature-tag">Low Latency</span>
        </div>
        <div class="category-examples">
          <strong>Examples:</strong> PostgreSQL, MySQL, SQL Server
        </div>
      </div>
      
      <div class="category-card" onclick="showCategoryDetails('olap')">
        <h3>OLAP Databases</h3>
        <p>Online Analytical Processing - Optimized for complex queries and analytics</p>
        <div class="category-features">
          <span class="feature-tag">Columnar Storage</span>
          <span class="feature-tag">Complex Queries</span>
          <span class="feature-tag">High Throughput</span>
        </div>
        <div class="category-examples">
          <strong>Examples:</strong> Snowflake, BigQuery, Redshift
        </div>
      </div>
      
      <div class="category-card" onclick="showCategoryDetails('nosql')">
        <h3>NoSQL Databases</h3>
        <p>Non-relational databases for flexible data models and horizontal scaling</p>
        <div class="category-features">
          <span class="feature-tag">Flexible Schema</span>
          <span class="feature-tag">Horizontal Scale</span>
          <span class="feature-tag">High Availability</span>
        </div>
        <div class="category-examples">
          <strong>Examples:</strong> MongoDB, Cassandra, Redis
        </div>
      </div>
      
      <div class="category-card" onclick="showCategoryDetails('vector')">
        <h3>Vector Databases</h3>
        <p>Specialized for AI/ML applications with embedding similarity search</p>
        <div class="category-features">
          <span class="feature-tag">Vector Search</span>
          <span class="feature-tag">AI/ML Focus</span>
          <span class="feature-tag">Similarity Search</span>
        </div>
        <div class="category-examples">
          <strong>Examples:</strong> Pinecone, Weaviate, Chroma
        </div>
      </div>
    </div>
  </section>

  <!-- OLTP vs OLAP Deep Dive -->
  <section class="database-section">
    <h2 class="section-title">⚖️ OLTP vs OLAP Deep Dive</h2>
    <p class="section-description">Understanding the fundamental differences</p>
    
    <div class="comparison-table">
      <table class="database-comparison">
        <thead>
          <tr>
            <th>Aspect</th>
            <th>OLTP (Transactional)</th>
            <th>OLAP (Analytical)</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td><strong>Purpose</strong></td>
            <td>Day-to-day operations, transactions</td>
            <td>Business intelligence, analytics</td>
          </tr>
          <tr>
            <td><strong>Data Structure</strong></td>
            <td>Normalized (3NF)</td>
            <td>Denormalized (Star/Snowflake)</td>
          </tr>
          <tr>
            <td><strong>Storage</strong></td>
            <td>Row-based</td>
            <td>Column-based</td>
          </tr>
          <tr>
            <td><strong>Query Type</strong></td>
            <td>Simple CRUD operations</td>
            <td>Complex aggregations, joins</td>
          </tr>
          <tr>
            <td><strong>Performance</strong></td>
            <td>Low latency, high concurrency</td>
            <td>High throughput, batch processing</td>
          </tr>
          <tr>
            <td><strong>Users</strong></td>
            <td>Applications, end-users</td>
            <td>Analysts, data scientists</td>
          </tr>
          <tr>
            <td><strong>Examples</strong></td>
            <td>E-commerce, banking, CRM</td>
            <td>Reporting, dashboards, ML training</td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>

  <!-- SQL Databases -->
  <section class="database-section">
    <h2 class="section-title">🗄️ SQL Databases (Relational)</h2>
    <p class="section-description">Traditional relational databases with ACID compliance</p>
    
    <div class="database-grid">
      <div class="database-card">
        <div class="db-header">
          <h3>PostgreSQL</h3>
          <span class="db-type open-source">Open Source</span>
        </div>
        <div class="db-content">
          <p class="db-description">Advanced open-source relational database with extensive features</p>
          <div class="db-features">
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>Advanced data types (JSON, arrays)</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>Extensions (PostGIS, TimescaleDB)</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>Strong ACID compliance</span>
            </div>
          </div>
          <div class="db-use-cases">
            <h4>Best For:</h4>
            <ul>
              <li>Complex applications</li>
              <li>Geospatial data</li>
              <li>Time series data</li>
              <li>General purpose</li>
            </ul>
          </div>
        </div>
      </div>
      
      <div class="database-card">
        <div class="db-header">
          <h3>MySQL</h3>
          <span class="db-type open-source">Open Source</span>
        </div>
        <div class="db-content">
          <p class="db-description">Popular open-source database known for performance and reliability</p>
          <div class="db-features">
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>High performance read operations</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>Easy to use and deploy</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>Large community support</span>
            </div>
          </div>
          <div class="db-use-cases">
            <h4>Best For:</h4>
            <ul>
              <li>Web applications</li>
              <li>E-commerce</li>
              <li>Content management</li>
              <li>Read-heavy workloads</li>
            </ul>
          </div>
        </div>
      </div>
      
      <div class="database-card">
        <div class="db-header">
          <h3>SQL Server</h3>
          <span class="db-type commercial">Commercial</span>
        </div>
        <div class="db-content">
          <p class="db-description">Microsoft's enterprise database with integrated BI capabilities</p>
          <div class="db-features">
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>Integrated BI tools</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>Advanced security features</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>Enterprise support</span>
            </div>
          </div>
          <div class="db-use-cases">
            <h4>Best For:</h4>
            <ul>
              <li>Enterprise applications</li>
              <li>Microsoft ecosystem</li>
              <li>Business intelligence</li>
              <li>Regulated industries</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- NoSQL Databases -->
  <section class="database-section">
    <h2 class="section-title">📱 NoSQL Databases</h2>
    <p class="section-description">Non-relational databases for specific use cases and scaling needs</p>
    
    <div class="nosql-types">
      <div class="nosql-category">
        <h3>Document Databases</h3>
        <div class="database-card">
          <div class="db-header">
            <h4>MongoDB</h4>
            <span class="db-type open-source">Open Source</span>
          </div>
          <div class="db-content">
            <p>Flexible document database with JSON-like documents</p>
            <div class="db-use-cases">
              <strong>Best For:</strong> Content management, mobile apps, catalog management
            </div>
          </div>
        </div>
      </div>
      
      <div class="nosql-category">
        <h3>Key-Value Databases</h3>
        <div class="database-card">
          <div class="db-header">
            <h4>Redis</h4>
            <span class="db-type open-source">Open Source</span>
          </div>
          <div class="db-content">
            <p>In-memory key-value store for ultra-fast performance</p>
            <div class="db-use-cases">
              <strong>Best For:</strong> Caching, session storage, real-time leaderboards
            </div>
          </div>
        </div>
      </div>
      
      <div class="nosql-category">
        <h3>Column-Family Databases</h3>
        <div class="database-card">
          <div class="db-header">
            <h4>Cassandra</h4>
            <span class="db-type open-source">Open Source</span>
          </div>
          <div class="db-content">
            <p>Distributed wide-column database for massive scalability</p>
            <div class="db-use-cases">
              <strong>Best For:</strong> Time series, IoT, high-write workloads
            </div>
          </div>
        </div>
      </div>
      
      <div class="nosql-category">
        <h3>Graph Databases</h3>
        <div class="database-card">
          <div class="db-header">
            <h4>Neo4j</h4>
            <span class="db-type commercial">Commercial</span>
          </div>
          <div class="db-content">
            <p>Native graph database for relationship-heavy data</p>
            <div class="db-use-cases">
              <strong>Best For:</strong> Social networks, fraud detection, recommendation engines
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Vector Databases -->
  <section class="database-section">
    <h2 class="section-title">🤖 Vector Databases</h2>
    <p class="section-description">Specialized databases for AI/ML applications and similarity search</p>
    
    <div class="database-grid">
      <div class="database-card">
        <div class="db-header">
          <h3>Pinecone</h3>
          <span class="db-type managed">Managed Service</span>
        </div>
        <div class="db-content">
          <p class="db-description">Fully managed vector database service for production AI applications</p>
          <div class="db-features">
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>Managed service</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>High-performance vector search</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>Easy integration</span>
            </div>
          </div>
          <div class="db-use-cases">
            <h4>Best For:</h4>
            <ul>
              <li>RAG applications</li>
              <li>Semantic search</li>
              <li>Recommendation systems</li>
            </ul>
          </div>
        </div>
      </div>
      
      <div class="database-card">
        <div class="db-header">
          <h3>Weaviate</h3>
          <span class="db-type open-source">Open Source</span>
        </div>
        <div class="db-content">
          <p class="db-description">Open-source vector database with knowledge graph capabilities</p>
          <div class="db-features">
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>Knowledge graph features</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>Self-hosting option</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">✓</span>
              <span>GraphQL API</span>
            </div>
          </div>
          <div class="db-use-cases">
            <h4>Best For:</h4>
            <ul>
              <li>Knowledge management</li>
              <li>Enterprise search</li>
              <li>AI research</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Database Selection Matrix -->
  <section class="database-section">
    <h2 class="section-title">📋 Database Selection Matrix</h2>
    <p class="section-description">Quick reference for choosing the right database</p>
    
    <div class="selection-matrix">
      <table class="matrix-table">
        <thead>
          <tr>
            <th>Use Case</th>
            <th>Recommended Database</th>
            <th>Key Reason</th>
            <th>Alternatives</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>E-commerce Platform</td>
            <td>PostgreSQL</td>
            <td>ACID compliance, reliability</td>
            <td>MySQL, SQL Server</td>
          </tr>
          <tr>
            <td>Analytics Dashboard</td>
            <td>Snowflake</td>
            <td>Columnar storage, scalability</td>
            <td>BigQuery, Redshift</td>
          </tr>
          <tr>
            <td>Mobile App Backend</td>
            <td>MongoDB</td>
            <td>Flexible schema, offline sync</td>
            <td>PostgreSQL, DynamoDB</td>
          </tr>
          <tr>
            <td>Session Caching</td>
            <td>Redis</td>
            <td>In-memory speed</td>
            <td>Memcached, DynamoDB</td>
          </tr>
          <tr>
            <td>Social Network</td>
            <td>Neo4j</td>
            <td>Relationship queries</td>
            <td>PostgreSQL + adjacency lists</td>
          </tr>
          <tr>
            <td>IoT Data Platform</td>
            <td>Cassandra</td>
            <td>High write throughput</td>
            <td>InfluxDB, TimescaleDB</td>
          </tr>
          <tr>
            <td>RAG Application</td>
            <td>Pinecone</td>
            <td>Vector search capabilities</td>
            <td>Weaviate, Chroma</td>
          </tr>
          <tr>
            <td>Content Management</td>
            <td>PostgreSQL</td>
            <td>JSON support, reliability</td>
            <td>MongoDB, MySQL</td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>
</div>

<!-- Database Details Modal -->
<div id="db-modal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeDbModal()">&times;</span>
    <h2 id="modal-title">Database Details</h2>
    <div id="modal-body">
      <!-- Content will be loaded here -->
    </div>
  </div>
</div>

<script>
// Database Categories Data
const categoryDetails = {
  oltp: {
    title: "OLTP Databases - Deep Dive",
    content: `
      <div class="category-detail">
        <h3>What are OLTP Databases?</h3>
        <p>OLTP (Online Transaction Processing) databases are optimized for handling large numbers of concurrent transactions with high reliability and consistency.</p>
        
        <h3>Key Characteristics</h3>
        <ul>
          <li><strong>ACID Compliance:</strong> Atomicity, Consistency, Isolation, Durability</li>
          <li><strong>Row-based Storage:</strong> Optimized for individual record operations</li>
          <li><strong>Low Latency:</strong> Millisecond response times</li>
          <li><strong>High Concurrency:</strong> Support many simultaneous users</li>
        </ul>
        
        <h3>Common Use Cases</h3>
        <div class="use-cases">
          <div class="use-case">
            <h4>E-commerce</h4>
            <p>Order processing, inventory management, customer accounts</p>
          </div>
          <div class="use-case">
            <h4>Banking Systems</h4>
            <p>Account transactions, transfers, ATM operations</p>
          </div>
          <div class="use-case">
            <h4>CRM Systems</h4>
            <p>Customer data, sales pipelines, support tickets</p>
          </div>
        </div>
      </div>
    `
  },
  olap: {
    title: "OLAP Databases - Deep Dive",
    content: `
      <div class="category-detail">
        <h3>What are OLAP Databases?</h3>
        <p>OLAP (Online Analytical Processing) databases are optimized for complex queries, aggregations, and business intelligence workloads.</p>
        
        <h3>Key Characteristics</h3>
        <ul>
          <li><strong>Columnar Storage:</strong> Optimized for analytical queries</li>
          <li><strong>Complex Queries:</strong> Support for aggregations, window functions</li>
          <li><strong>High Throughput:</strong> Process large datasets efficiently</li>
          <li><strong>Denormalized:</strong> Star and snowflake schemas</li>
        </ul>
        
        <h3>Common Use Cases</h3>
        <div class="use-cases">
          <div class="use-case">
            <h4>Business Intelligence</h4>
            <p>Dashboard queries, executive reporting</p>
          </div>
          <div class="use-case">
            <h4>Data Warehousing</h4>
            <p>Historical analysis, trend identification</p>
          </div>
          <div class="use-case">
            <h4>ML Training</h4>
            <p>Feature engineering, model training data</p>
          </div>
        </div>
      </div>
    `
  },
  nosql: {
    title: "NoSQL Databases - Deep Dive",
    content: `
      <div class="category-detail">
        <h3>What are NoSQL Databases?</h3>
        <p>NoSQL databases provide flexible data models and horizontal scalability for modern applications.</p>
        
        <h3>NoSQL Types</h3>
        <div class="nosql-types-detail">
          <div class="nosql-type">
            <h4>Document Databases</h4>
            <p>JSON-like documents with flexible schemas</p>
            <p><strong>Examples:</strong> MongoDB, Couchbase</p>
          </div>
          <div class="nosql-type">
            <h4>Key-Value Databases</h4>
            <p>Simple key-value pairs with ultra-fast access</p>
            <p><strong>Examples:</strong> Redis, DynamoDB</p>
          </div>
          <div class="nosql-type">
            <h4>Column-Family Databases</h4>
            <p>Wide columns for massive write scalability</p>
            <p><strong>Examples:</strong> Cassandra, HBase</p>
          </div>
          <div class="nosql-type">
            <h4>Graph Databases</h4>
            <p>Optimized for relationship queries</p>
            <p><strong>Examples:</strong> Neo4j, Amazon Neptune</p>
          </div>
        </div>
        
        <h3>When to Use NoSQL</h3>
        <ul>
          <li>Unstructured or semi-structured data</li>
          <li>Need for horizontal scaling</li>
          <li>High write throughput requirements</li>
          <li>Flexible schema requirements</li>
        </ul>
      </div>
    `
  },
  vector: {
    title: "Vector Databases - Deep Dive",
    content: `
      <div class="category-detail">
        <h3>What are Vector Databases?</h3>
        <p>Vector databases are specialized for storing and querying high-dimensional vectors, primarily for AI/ML applications.</p>
        
        <h3>Key Concepts</h3>
        <ul>
          <li><strong>Embeddings:</strong> Numerical representations of data</li>
          <li><strong>Similarity Search:</strong> Finding nearest vectors</li>
          <li><strong>Vector Indexing:</strong> Efficient search algorithms</li>
          <li><strong>Approximate Nearest Neighbor (ANN):</strong> Fast similarity search</li>
        </ul>
        
        <h3>Common Use Cases</h3>
        <div class="use-cases">
          <div class="use-case">
            <h4>RAG Applications</h4>
            <p>Retrieval-Augmented Generation for LLMs</p>
          </div>
          <div class="use-case">
            <h4>Semantic Search</h4>
            <p>Meaning-based search beyond keywords</p>
          </div>
          <div class="use-case">
            <h4>Recommendation Systems</h4>
            <p>Content recommendations, similarity matching</p>
          </div>
        </div>
        
        <h3>Popular Vector Databases</h3>
        <ul>
          <li><strong>Pinecone:</strong> Managed service, easy to use</li>
          <li><strong>Weaviate:</strong> Open source, knowledge graphs</li>
          <li><strong>Chroma:</strong> Lightweight, developer-friendly</li>
          <li><strong>FAISS:</strong> Library for vector similarity</li>
        </ul>
      </div>
    `
  }
};

function showCategoryDetails(category) {
  const modal = document.getElementById('db-modal');
  const modalTitle = document.getElementById('modal-title');
  const modalBody = document.getElementById('modal-body');
  
  const data = categoryDetails[category];
  modalTitle.textContent = data.title;
  modalBody.innerHTML = data.content;
  modal.style.display = 'block';
}

function closeDbModal() {
  document.getElementById('db-modal').style.display = 'none';
}

function filterDatabases() {
  const useCase = document.querySelector('input[name="use-case"]:checked')?.value;
  const scale = document.querySelector('input[name="scale"]:checked')?.value;
  const resultsDiv = document.getElementById('selection-results');
  const resultsContent = document.getElementById('results-content');
  
  if (!useCase || !scale) {
    resultsDiv.style.display = 'none';
    return;
  }
  
  // Database recommendations based on use case and scale
  const recommendations = {
    'transactions-small': [
      { name: 'PostgreSQL', reason: 'Reliable, feature-rich, perfect for small applications', type: 'SQL' },
      { name: 'MySQL', reason: 'Fast, easy to setup, great for web apps', type: 'SQL' },
      { name: 'SQLite', reason: 'File-based, zero configuration, embedded use', type: 'SQL' }
    ],
    'transactions-medium': [
      { name: 'PostgreSQL', reason: 'Handles medium scale well, advanced features', type: 'SQL' },
      { name: 'MySQL', reason: 'Proven performance at medium scale', type: 'SQL' },
      { name: 'MongoDB', reason: 'Flexible schema, good for growing applications', type: 'NoSQL' }
    ],
    'transactions-large': [
      { name: 'PostgreSQL', reason: 'Enterprise features, high availability', type: 'SQL' },
      { name: 'Cassandra', reason: 'High write throughput, horizontal scaling', type: 'NoSQL' },
      { name: 'CockroachDB', reason: 'Distributed SQL, global scale', type: 'NewSQL' }
    ],
    'analytics-small': [
      { name: 'PostgreSQL', reason: 'Window functions, good for small analytics', type: 'SQL' },
      { name: 'DuckDB', reason: 'Fast analytical queries, embedded', type: 'OLAP' },
      { name: 'SQLite', reason: 'Simple analytics on small datasets', type: 'SQL' }
    ],
    'analytics-medium': [
      { name: 'ClickHouse', reason: 'Columnar storage, fast analytics', type: 'OLAP' },
      { name: 'PostgreSQL', reason: 'Good analytical capabilities', type: 'SQL' },
      { name: 'BigQuery', reason: 'Serverless, pay-per-query', type: 'OLAP' }
    ],
    'analytics-large': [
      { name: 'Snowflake', reason: 'Cloud-native, excellent performance', type: 'OLAP' },
      { name: 'BigQuery', reason: 'Serverless, massive scale', type: 'OLAP' },
      { name: 'Redshift', reason: 'AWS integration, proven at scale', type: 'OLAP' }
    ],
    'real-time-small': [
      { name: 'Redis', reason: 'In-memory, microsecond latency', type: 'Key-Value' },
      { name: 'PostgreSQL', reason: 'Good for real-time with proper indexing', type: 'SQL' },
      { name: 'SQLite', reason: 'Simple real-time applications', type: 'SQL' }
    ],
    'real-time-medium': [
      { name: 'Redis', reason: 'Excellent performance, clustering support', type: 'Key-Value' },
      { name: 'MongoDB', reason: 'Good real-time performance, flexible', type: 'NoSQL' },
      { name: 'PostgreSQL', reason: 'Real-time with LISTEN/NOTIFY', type: 'SQL' }
    ],
    'real-time-large': [
      { name: 'Kafka + RocksDB', reason: 'Streaming + persistent storage', type: 'Hybrid' },
      { name: 'ScyllaDB', reason: 'Cassandra-compatible, low latency', type: 'NoSQL' },
      { name: 'Redis Cluster', reason: 'Distributed in-memory, high performance', type: 'Key-Value' }
    ],
    'ai-ml-small': [
      { name: 'PostgreSQL', reason: 'pgvector extension, good for small ML', type: 'SQL' },
      { name: 'Chroma', reason: 'Lightweight vector database', type: 'Vector' },
      { name: 'SQLite', reason: 'Simple ML workloads, embedded', type: 'SQL' }
    ],
    'ai-ml-medium': [
      { name: 'Pinecone', reason: 'Managed vector database, easy to use', type: 'Vector' },
      { name: 'Weaviate', reason: 'Knowledge graphs, semantic search', type: 'Vector' },
      { name: 'PostgreSQL + pgvector', reason: 'Cost-effective vector operations', type: 'SQL' }
    ],
    'ai-ml-large': [
      { name: 'Pinecone', reason: 'Enterprise vector database at scale', type: 'Vector' },
      { name: 'Weaviate', reason: 'Scalable knowledge graphs', type: 'Vector' },
      { name: 'Milvus', reason: 'Open source, large scale vector search', type: 'Vector' }
    ],
    'content-small': [
      { name: 'PostgreSQL', reason: 'JSON support, structured content', type: 'SQL' },
      { name: 'MongoDB', reason: 'Document-oriented, flexible content', type: 'NoSQL' },
      { name: 'SQLite', reason: 'Simple content management', type: 'SQL' }
    ],
    'content-medium': [
      { name: 'MongoDB', reason: 'Flexible schemas, content management', type: 'NoSQL' },
      { name: 'PostgreSQL', reason: 'JSONB, full-text search', type: 'SQL' },
      { name: 'Elasticsearch', reason: 'Full-text search, content indexing', type: 'Search' }
    ],
    'content-large': [
      { name: 'MongoDB', reason: 'Scales well, content management', type: 'NoSQL' },
      { name: 'Elasticsearch', reason: 'Powerful search at scale', type: 'Search' },
      { name: 'PostgreSQL', reason: 'Reliable, can handle large content', type: 'SQL' }
    ]
  };
  
  const key = `${useCase}-${scale}`;
  const results = recommendations[key] || [];
  
  if (results.length > 0) {
    let resultsHTML = '<div class="recommendation-grid">';
    results.forEach((db, index) => {
      resultsHTML += `
        <div class="recommendation-card">
          <div class="rec-header">
            <h4>${db.name}</h4>
            <span class="rec-type">${db.type}</span>
          </div>
          <p class="rec-reason">${db.reason}</p>
          <div class="rec-priority">
            <span class="priority-badge priority-${index + 1}">#${index + 1} Recommendation</span>
          </div>
        </div>
      `;
    });
    resultsHTML += '</div>';
    
    resultsContent.innerHTML = resultsHTML;
    resultsDiv.style.display = 'block';
  } else {
    resultsDiv.style.display = 'none';
  }
}

// Close modal when clicking outside
window.onclick = function(event) {
  const modal = document.getElementById('db-modal');
  if (event.target == modal) {
    modal.style.display = 'none';
  }
}
</script>
