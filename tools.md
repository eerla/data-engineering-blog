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

  <!-- Tools Grid -->
  <section class="tools-grid">
    {% assign tools = site.data.tools %}
    
    {% for tool in tools %}
    <div class="tool-card" 
         data-layer="{{ tool.layer }}" 
         data-type="{{ tool.type }}"
         data-category="{{ tool.category }}">
      
      <div class="tool-header">
        <h3 class="tool-name">{{ tool.name }}</h3>
        <div class="tool-badges">
          <span class="badge layer">{{ tool.layer }}</span>
          <span class="badge type">{{ tool.type }}</span>
        </div>
      </div>
      
      <div class="tool-content">
        <p class="tool-description">{{ tool.description }}</p>
        
        <div class="tool-details">
          <div class="detail-item">
            <strong>When to use:</strong>
            <p>{{ tool.when_to_use }}</p>
          </div>
          
          <div class="detail-item">
            <strong>Category:</strong>
            <span class="category-tag">{{ tool.category }}</span>
          </div>
        </div>
        
        <div class="tool-actions">
          <a href="{{ site.baseurl }}/layers/{{ tool.layer | replace: ' ', '-' | downcase }}/" 
             class="layer-link">
            View {{ tool.layer }} →
          </a>
        </div>
      </div>
    </div>
    {% endfor %}
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
// Simple filtering functionality
document.getElementById('layer-filter').addEventListener('change', filterTools);
document.getElementById('type-filter').addEventListener('change', filterTools);

function filterTools() {
  const layerFilter = document.getElementById('layer-filter').value;
  const typeFilter = document.getElementById('type-filter').value;
  const toolCards = document.querySelectorAll('.tool-card');
  
  toolCards.forEach(card => {
    const layer = card.dataset.layer;
    const type = card.dataset.type;
    
    const layerMatch = layerFilter === 'all' || layer === layerFilter;
    const typeMatch = typeFilter === 'all' || type === typeFilter;
    
    if (layerMatch && typeMatch) {
      card.style.display = 'block';
    } else {
      card.style.display = 'none';
    }
  });
}
</script>
