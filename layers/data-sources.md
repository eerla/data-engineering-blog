---
layout: default
title: "Data Sources"
---

<div class="page-header">
  <h1 class="page-title">Data Sources</h1>
  <p class="page-subtitle">Where data originates and how to access it</p>
</div>

<div class="container">
  <section class="layer-intro">
    <div class="analogy-box">
      <h3>🏞 Analogy</h3>
      <p>The starting point of your data journey - like different rivers flowing into a lake</p>
    </div>
    
    <div class="problems-solved">
      <h3>Problems Solved</h3>
      <ul>
        <li>Data accessibility and connectivity</li>
        <li>API integration challenges</li>
        <li>Data format standardization</li>
      </ul>
    </div>
  </section>

  <section class="layer-content">
    <h2>Understanding Data Sources</h2>
    
    <div class="content-section">
      <h3>Types of Data Sources</h3>
      
      <div class="type-grid">
        <div class="type-card">
          <h4>Databases</h4>
          <p>SQL and NoSQL databases for structured and unstructured data</p>
          <div class="examples">
            <strong>Examples:</strong> PostgreSQL, MongoDB, Cassandra, Redis
          </div>
        </div>
        
        <div class="type-card">
          <h4>APIs</h4>
          <p>REST and GraphQL interfaces for real-time data access</p>
          <div class="examples">
            <strong>Examples:</strong> Twitter API, Stripe API, Salesforce API
          </div>
        </div>
        
        <div class="type-card">
          <h4>File Systems</h4>
          <p>Structured and semi-structured files in various formats</p>
          <div class="examples">
            <strong>Examples:</strong> CSV, JSON, Parquet, Avro
          </div>
        </div>
        
        <div class="type-card">
          <h4>Streaming Sources</h4>
          <p>Real-time event streams and message queues</p>
          <div class="examples">
            <strong>Examples:</strong> Kafka, Kinesis, Pub/Sub
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="tools-section">
    <h2>Recommended Tools</h2>
    <p>Tools for working with different data sources:</p>
    
    <div class="tools-list">
      {% assign ingestion_tools = site.data.tools | where: "layer", "Data Ingestion" %}
      
      {% for tool in ingestion_tools %}
      <div class="tool-item">
        <h4><a href="{{ site.baseurl }}/tools/#{{ tool.name | replace: ' ', '-' | downcase }}">{{ tool.name }}</a></h4>
        <p>{{ tool.description }}</p>
        <div class="tool-meta">
          <span class="type-badge">{{ tool.type }}</span>
          <span class="category-badge">{{ tool.category }}</span>
        </div>
      </div>
      {% endfor %}
    </div>
  </section>

  <section class="next-steps">
    <h2>Next Steps</h2>
    <div class="step-navigation">
      <div class="step-card">
        <h3>← Previous</h3>
        <a href="{{ site.baseurl }}/roadmap/" class="step-link">Back to Roadmap</a>
      </div>
      
      <div class="step-card">
        <h3>Data Ingestion →</h3>
        <p>Learn how to move data from sources to storage</p>
        <a href="{{ site.baseurl }}/layers/data-ingestion/" class="step-link primary">Next Layer</a>
      </div>
    </div>
  </section>
</div>
