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
      {% assign source_tools = site.data.tools | where: "layer", "Data Sources" %}
      
      {% for tool in source_tools %}
      <div class="tool-item">
        <h4><a href="{{ site.baseurl }}/tools/#{{ tool.name | replace: ' ', '-' | downcase }}">{{ tool.name }}</a></h4>
        <p><strong>Use case:</strong> {{ tool.use_case }}</p>
        <div class="tool-meta">
          <span class="type-badge">{{ tool.type }}</span>
          <span class="category-badge">{{ tool.category }}</span>
        </div>
        <div class="when-to-use">
          <strong>When to use:</strong> {{ tool.use_case }}
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

<style>
/* Fix for numbered headings with emojis */
h3 {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  white-space: nowrap;
}

.tools-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 1.5rem;
  margin: 2rem 0;
}

.tool-item {
  background: var(--background-secondary);
  padding: 1.5rem;
  border-radius: 8px;
  border: 1px solid var(--border-color);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.tool-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.tool-item h4 {
  margin: 0 0 1rem 0;
  color: var(--primary-color);
}

.tool-item h4 a {
  color: inherit;
  text-decoration: none;
}

.tool-item h4 a:hover {
  text-decoration: underline;
}

.tool-item p {
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

.type-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
  margin: 2rem 0;
}

.type-card {
  background: var(--background-secondary);
  padding: 1.5rem;
  border-radius: 8px;
  border: 1px solid var(--border-color);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.type-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.type-card h4 {
  margin: 0 0 1rem 0;
  color: var(--primary-color);
  font-size: 1.1rem;
  font-weight: 600;
}

.type-card p {
  margin: 0 0 1rem 0;
  color: var(--text-secondary);
  line-height: 1.6;
}

.type-card .examples,
.type-card .use-cases {
  margin: 0.5rem 0;
  font-size: 0.9rem;
}

.type-card .examples strong,
.type-card .use-cases strong {
  color: var(--primary-color);
}
</style>
