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
    
    <div class="tools-grid">
      {% assign ingestion_tools = site.data.tools | where: "layer", "Data Ingestion" %}
      
      {% for tool in ingestion_tools %}
      <div class="tool-card">
        <h4>{{ tool.name }}</h4>
        <div class="tool-meta">
          <span class="type-badge">{{ tool.type }}</span>
          <span class="category-badge">{{ tool.category }}</span>
        </div>
        <p><strong>Use case:</strong> {{ tool.use_case }}</p>
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

<style>
/* Fix for numbered headings with emojis */
h3 {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  white-space: nowrap;
}

.tools-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 1.5rem;
  margin: 2rem 0;
}

.tool-card {
  background: var(--background-secondary);
  padding: 1.5rem;
  border-radius: 8px;
  border: 1px solid var(--border-color);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.tool-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.tool-card h4 {
  margin: 0 0 1rem 0;
  color: var(--primary-color);
}

.tool-card p {
  margin: 0 0 1rem 0;
  color: var(--text-secondary);
}

.tool-meta {
  display: flex;
  gap: 0.5rem;
  margin-bottom: 1rem;
}

.type-badge, .category-badge {
  padding: 0.25rem 0.75rem;
  border-radius: 20px;
  font-size: 0.75rem;
  font-weight: 600;
  color: white;
}

.type-badge {
  background: var(--secondary-color);
}

.category-badge {
  background: var(--primary-color);
}

.step-navigation {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  margin: 2rem 0;
}

.step-card {
  background: var(--background-secondary);
  padding: 1.5rem;
  border-radius: 8px;
  border: 1px solid var(--border-color);
  text-align: center;
}

.step-card h3 {
  margin: 0 0 1rem 0;
  color: var(--primary-color);
}

.step-link {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  background: var(--primary-color);
  color: white;
  text-decoration: none;
  border-radius: 6px;
  transition: background-color 0.2s ease;
}

.step-link:hover {
  background: var(--secondary-color);
}

.step-link.primary {
  background: var(--secondary-color);
}

.step-link.primary:hover {
  background: var(--primary-color);
}

/* Ensure proper spacing for content sections */
.layer-intro {
  margin: 2rem 0;
}

.analogy-box, .problems-solved {
  background: var(--background-secondary);
  padding: 1.5rem;
  border-radius: 8px;
  border: 1px solid var(--border-color);
  margin-bottom: 1rem;
}

.analogy-box h3, .problems-solved h3 {
  margin: 0 0 1rem 0;
  color: var(--primary-color);
}

.problems-solved ul {
  list-style: none;
  padding: 0;
}

.problems-solved li {
  padding: 0.5rem 0;
  border-bottom: 1px solid var(--border-color);
}

.problems-solved li:last-child {
  border-bottom: none;
}
</style>
