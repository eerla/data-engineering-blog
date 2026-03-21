---
layout: default
title: "Data Ingestion"
---

<div class="page-header">
  <h1 class="page-title">Data Ingestion</h1>
  <p class="page-subtitle">Moving data from sources to storage systems</p>
</div>

<div class="container">
  <section class="layer-intro">
    <div class="analogy-box">
      <h3>🚚 Analogy</h3>
      <p>The transportation network that moves goods from suppliers to warehouses</p>
    </div>
    
    <div class="problems-solved">
      <h3>Problems Solved</h3>
      <ul>
        <li>Reliable data transfer</li>
        <li>Real-time vs batch processing</li>
        <li>Data quality and validation</li>
        <li>Error handling and retry logic</li>
      </ul>
    </div>
  </section>

  <section class="layer-content">
    <h2>Understanding Data Ingestion</h2>
    
    <div class="content-section">
      <h3>Types of Data Ingestion</h3>
      
      <div class="type-grid">
        <div class="type-card">
          <h4>Batch Processing</h4>
          <p>Scheduled jobs that process data in batches at regular intervals</p>
          <div class="examples">
            <strong>Examples:</strong> Nightly ETL jobs, hourly data sync, daily report generation
          </div>
          <div class="use-cases">
            <strong>Best for:</strong> Large datasets, cost optimization, scheduled processing
          </div>
        </div>
        
        <div class="type-card">
          <h4>Stream Processing</h4>
          <p>Continuous flow of data processing as events arrive</p>
          <div class="examples">
            <strong>Examples:</strong> Real-time analytics, fraud detection, live monitoring
          </div>
          <div class="use-cases">
            <strong>Best for:</strong> Real-time insights, immediate response, event-driven systems
          </div>
        </div>
        
        <div class="type-card">
          <h4>Change Data Capture</h4>
          <p>Capturing database changes in real-time</p>
          <div class="examples">
            <strong>Examples:</strong> Database replication, audit logging, sync systems
          </div>
          <div class="use-cases">
            <strong>Best for:</strong> Data synchronization, real-time warehousing, microservices
          </div>
        </div>
        
        <div class="type-card">
          <h4>API-based Ingestion</h4>
          <p>Pulling data from external APIs and services</p>
          <div class="examples">
            <strong>Examples:</strong> CRM data sync, social media analytics, financial data feeds
          </div>
          <div class="use-cases">
            <strong>Best for:</strong> SaaS data, third-party integrations, web scraping
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="tools-section">
    <h2>Recommended Tools</h2>
    <p>Tools for data ingestion by category:</p>
    
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
        <a href="{{ site.baseurl }}/layers/data-sources/" class="step-link">Data Sources</a>
      </div>
      
      <div class="step-card">
        <h3>Data Processing →</h3>
        <p>Learn how to transform raw data into valuable insights</p>
        <a href="{{ site.baseurl }}/layers/data-processing/" class="step-link primary">Next Layer</a>
      </div>
    </div>
  </section>
</div>
