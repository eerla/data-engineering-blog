---
layout: default
title: "Data Storage"
---

<div class="page-header">
  <h1 class="page-title">Data Storage</h1>
  <p class="page-subtitle">Storing processed data for analysis and consumption</p>
</div>

<div class="container">
  <section class="layer-intro">
    <div class="analogy-box">
      <h3>🏪 Analogy</h3>
      <p>The warehouse system that organizes finished products for distribution</p>
    </div>
    
    <div class="problems-solved">
      <h3>Problems Solved</h3>
      <ul>
        <li>Scalable data storage</li>
        <li>Fast query performance</li>
        <li>Data governance and security</li>
        <li>Cost optimization</li>
      </ul>
    </div>
  </section>

  <section class="layer-content">
    <h2>Understanding Data Storage</h2>
    
    <div class="content-section">
      <h3>Types of Data Storage</h3>
      
      <div class="type-grid">
        <div class="type-card">
          <h4>Data Warehouses</h4>
          <p>Optimized for analytics with SQL interface and built-in optimizations</p>
          <div class="examples">
            <strong>Examples:</strong> BigQuery, Snowflake, Redshift, Azure Synapse
          </div>
          <div class="use-cases">
            <strong>Best for:</strong> Business intelligence, analytics, structured queries
          </div>
        </div>
        
        <div class="type-card">
          <h4>Data Lakes</h4>
          <p>Scalable object storage for any data type with schema-on-read</p>
          <div class="examples">
            <strong>Examples:</strong> S3, Google Cloud Storage, Azure Data Lake
          </div>
          <div class="use-cases">
            <strong>Best for:</strong> Big data, machine learning, cost-effective storage
          </div>
        </div>
        
        <div class="type-card">
          <h4>Lakehouses</h4>
          <p>Combining data warehouse performance with data lake flexibility</p>
          <div class="examples">
            <strong>Examples:</strong> Databricks, Snowflake (with Iceberg), BigQuery (with BigLake)
          </div>
          <div class="use-cases">
            <strong>Best for:</strong> Analytics + ML, ACID transactions, flexibility
          </div>
        </div>
        
        <div class="type-card">
          <h4>Table Formats</h4>
          <p>Optimized file formats for analytical queries and data management</p>
          <div class="examples">
            <strong>Examples:</strong> Parquet, Delta Lake, Iceberg, Hudi
          </div>
          <div class="use-cases">
            <strong>Best for:</strong> Performance, ACID transactions, schema evolution
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="tools-section">
    <h2>Recommended Tools</h2>
    <p>Tools for data storage by category:</p>
    
    <div class="tools-list">
      {% assign storage_tools = site.data.tools | where: "layer", "Data Storage" %}
      
      {% for tool in storage_tools %}
      <div class="tool-item">
        <h4><a href="{{ site.baseurl }}/tools/#{{ tool.name | replace: ' ', '-' | downcase }}">{{ tool.name }}</a></h4>
        <p>{{ tool.description }}</p>
        <div class="tool-meta">
          <span class="type-badge">{{ tool.type }}</span>
          <span class="category-badge">{{ tool.category }}</span>
        </div>
        <div class="when-to-use">
          <strong>When to use:</strong> {{ tool.when_to_use }}
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
        <a href="{{ site.baseurl }}/layers/data-processing/" class="step-link">Data Processing</a>
      </div>
      
      <div class="step-card">
        <h3>Data Consumption →</h3>
        <p>Learn how to make data accessible and useful</p>
        <a href="{{ site.baseurl }}/layers/data-consumption/" class="step-link primary">Next Layer</a>
      </div>
    </div>
  </section>
</div>
