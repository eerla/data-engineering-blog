---
layout: default
title: "Data Consumption"
---

<div class="page-header">
  <h1 class="page-title">Data Consumption</h1>
  <p class="page-subtitle">Making data accessible to users and applications</p>
</div>

<div class="container">
  <section class="layer-intro">
    <div class="analogy-box">
      <h3>🏪 Analogy</h3>
      <p>The retail store where customers can easily find and purchase products</p>
    </div>
    
    <div class="problems-solved">
      <h3>Problems Solved</h3>
      <ul>
        <li>Data visualization and reporting</li>
        <li>Real-time analytics</li>
        <li>Self-service data access</li>
        <li>Decision support systems</li>
      </ul>
    </div>
  </section>

  <section class="layer-content">
    <h2>Understanding Data Consumption</h2>
    
    <div class="content-section">
      <h3>Types of Data Consumption</h3>
      
      <div class="type-grid">
        <div class="type-card">
          <h4>Business Intelligence Dashboards</h4>
          <p>Interactive visualizations and KPI tracking for business users</p>
          <div class="examples">
            <strong>Examples:</strong> Executive dashboards, sales analytics, operational metrics
          </div>
          <div class="use-cases">
            <strong>Best for:</strong> Business decisions, performance monitoring, trend analysis
          </div>
        </div>
        
        <div class="type-card">
          <h4>APIs and Data Services</h4>
          <p>Programmatic access to data for applications and automation</p>
          <div class="examples">
            <strong>Examples:</strong> REST APIs, GraphQL endpoints, data streaming services
          </div>
          <div class="use-cases">
            <strong>Best for:</strong> Application integration, automation, real-time access
          </div>
        </div>
        
        <div class="type-card">
          <h4>Notebooks and Analysis Tools</h4>
          <p>Interactive environments for data exploration and analysis</p>
          <div class="examples">
            <strong>Examples:</strong> Jupyter notebooks, Colab, Deepnote
          </div>
          <div class="use-cases">
            <strong>Best for:</strong> Data exploration, prototyping, collaborative analysis
          </div>
        </div>
        
        <div class="type-card">
          <h4>Automated Reporting Systems</h4>
          <p>Scheduled reports and alerts delivered to stakeholders</p>
          <div class="examples">
            <strong>Examples:</strong> Email reports, Slack notifications, automated dashboards
          </div>
          <div class="use-cases">
            <strong>Best for:</strong> Stakeholder communication, compliance, monitoring
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="tools-section">
    <h2>Recommended Tools</h2>
    <p>Tools for data consumption by category:</p>
    
    <div class="tools-list">
      {% assign consumption_tools = site.data.tools | where: "layer", "Data Consumption" %}
      
      {% for tool in consumption_tools %}
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
      </div>
      {% endfor %}
    </div>
  </section>

  <section class="next-steps">
    <h2>Next Steps</h2>
    <div class="step-navigation">
      <div class="step-card">
        <h3>← Previous</h3>
        <a href="{{ site.baseurl }}/layers/data-storage/" class="step-link">Data Storage</a>
      </div>
      
      <div class="step-card">
        <h3>🎯 Final Step</h3>
        <p>Congratulations! You've completed the data engineering journey.</p>
        <a href="{{ site.baseurl }}/tools/" class="step-link primary">Explore All Tools</a>
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
