---
layout: default
title: "Data Engineering Tools"
---

<div class="page-header">
  <h1 class="page-title">Data Engineering Tools</h1>
  <p class="page-subtitle">Find the right tools for your data engineering needs</p>
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

  <!-- Tool Comparisons -->
  <section class="tool-comparisons">
    <h2>Tool Comparisons</h2>
    
    <div class="comparison-grid">
      <div class="comparison-card">
        <h3>🔄 Orchestration Tools</h3>
        <div class="tools-compared">
          <div class="tool-compare-item">
            <strong>Airflow:</strong> Industry standard, batch-focused
          </div>
          <div class="tool-compare-item">
            <strong>Prefect:</strong> Modern, Python-native
          </div>
          <div class="tool-compare-item">
            <strong>Dagster:</strong> Data-aware, asset governance
          </div>
        </div>
      </div>
      
      <div class="comparison-card">
        <h3>📊 Data Warehouses</h3>
        <div class="tools-compared">
          <div class="tool-compare-item">
            <strong>Snowflake:</strong> Multi-cloud, auto-scaling
          </div>
          <div class="tool-compare-item">
            <strong>BigQuery:</strong> Serverless, ML-integrated
          </div>
          <div class="tool-compare-item">
            <strong>Redshift:</strong> Petabyte-scale, AWS-native
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

// Simple filtering functionality (updated for cloud-based structure)
document.getElementById('layer-filter').addEventListener('change', filterTools);
document.getElementById('type-filter').addEventListener('change', filterTools);

function filterTools() {
  const layerFilter = document.getElementById('layer-filter').value;
  const typeFilter = document.getElementById('type-filter').value;
  const toolCards = document.querySelectorAll('.tool-card');
  
  toolCards.forEach(card => {
    const layer = card.querySelector('.layer-badge').textContent;
    const type = card.querySelector('.type-badge').textContent;
    
    const layerMatch = layerFilter === 'all' || layer.includes(layerFilter);
    const typeMatch = typeFilter === 'all' || type.includes(typeFilter);
    
    if (layerMatch && typeMatch) {
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
