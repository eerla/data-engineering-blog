---
layout: default
title: "Data Engineering Layers"
---

<div class="page-header">
  <h1 class="page-title">Data Engineering Layers</h1>
  <p class="page-subtitle">Understanding the complete data lifecycle</p>
</div>

<div class="container">
  <section class="layers-intro">
    <p class="intro-text">Data engineering is organized into distinct layers, each solving specific problems in the data lifecycle. Click on any layer below to explore tools and concepts.</p>
  </section>

  <section class="layers-grid">
    <div class="layer-card">
      <div class="layer-number">1</div>
      <div class="layer-content">
        <h3><a href="{{ site.baseurl }}/layers/data-sources/">Data Sources</a></h3>
        <p>Where data originates and how to access it</p>
        <div class="layer-problems">
          <strong>Solves:</strong> Data accessibility, API integration, format standardization
        </div>
        <div class="layer-next">
          <strong>Next:</strong> <a href="{{ site.baseurl }}/layers/data-ingestion/">Data Ingestion</a>
        </div>
      </div>
    </div>
    
    <div class="layer-card">
      <div class="layer-number">2</div>
      <div class="layer-content">
        <h3><a href="{{ site.baseurl }}/layers/data-ingestion/">Data Ingestion</a></h3>
        <p>Moving data from sources to storage systems</p>
        <div class="layer-problems">
          <strong>Solves:</strong> Reliable transfer, quality validation, error handling
        </div>
        <div class="layer-next">
          <strong>Next:</strong> <a href="{{ site.baseurl }}/layers/data-processing/">Data Processing</a>
        </div>
      </div>
    </div>
    
    <div class="layer-card">
      <div class="layer-number">3</div>
      <div class="layer-content">
        <h3><a href="{{ site.baseurl }}/layers/data-processing/">Data Processing</a></h3>
        <p>Transforming raw data into valuable insights</p>
        <div class="layer-problems">
          <strong>Solves:</strong> Data transformation, business logic, performance
        </div>
        <div class="layer-next">
          <strong>Next:</strong> <a href="{{ site.baseurl }}/layers/data-storage/">Data Storage</a>
        </div>
      </div>
    </div>
    
    <div class="layer-card">
      <div class="layer-number">4</div>
      <div class="layer-content">
        <h3><a href="{{ site.baseurl }}/layers/data-storage/">Data Storage</a></h3>
        <p>Storing processed data for analysis and consumption</p>
        <div class="layer-problems">
          <strong>Solves:</strong> Scalable storage, query performance, governance
        </div>
        <div class="layer-next">
          <strong>Next:</strong> <a href="{{ site.baseurl }}/layers/data-consumption/">Data Consumption</a>
        </div>
      </div>
    </div>
    
    <div class="layer-card">
      <div class="layer-number">5</div>
      <div class="layer-content">
        <h3><a href="{{ site.baseurl }}/layers/data-consumption/">Data Consumption</a></h3>
        <p>Making data accessible to users and applications</p>
        <div class="layer-problems">
          <strong>Solves:</strong> Visualization, reporting, self-service access
        </div>
        <div class="layer-next">
          <strong>Final:</strong> <a href="{{ site.baseurl }}/tools/">Explore Tools</a>
        </div>
      </div>
    </div>
  </section>

  <section class="journey-section">
    <h2>Complete Your Journey</h2>
    <div class="journey-visual">
      <div class="journey-step completed">
        <div class="step-icon">🏗️</div>
        <div class="step-text">
          <strong>Start Here</strong><br>
          <a href="{{ site.baseurl }}/roadmap/">Begin with Foundations</a>
        </div>
      </div>
      
      <div class="journey-arrow">→</div>
      
      <div class="journey-step">
        <div class="step-icon">🛠️</div>
        <div class="step-text">
          <strong><a href="{{ site.baseurl }}/tools/" style="color: inherit; text-decoration: none;">Explore Tools</a></strong><br>
          Find solutions for each layer
        </div>
      </div>
    </div>
  </section>

  <section class="tools-preview">
    <h2>Quick Tool Access</h2>
    <div class="preview-grid">
      {% assign ingestion_tools = site.data.tools | where: "layer", "Data Ingestion" %}
      {% assign processing_tools = site.data.tools | where: "layer", "Data Processing" %}
      {% assign storage_tools = site.data.tools | where: "layer", "Data Storage" %}
      {% assign consumption_tools = site.data.tools | where: "layer", "Data Consumption" %}
      
      <div class="preview-card">
        <h4>Ingestion</h4>
        <div class="tool-count">{{ ingestion_tools.size }} tools</div>
        <a href="{{ site.baseurl }}/tools/" class="preview-link">Browse All</a>
      </div>
      
      <div class="preview-card">
        <h4>Processing</h4>
        <div class="tool-count">{{ processing_tools.size }} tools</div>
        <a href="{{ site.baseurl }}/tools/" class="preview-link">Browse All</a>
      </div>
      
      <div class="preview-card">
        <h4>Storage</h4>
        <div class="tool-count">{{ storage_tools.size }} tools</div>
        <a href="{{ site.baseurl }}/tools/" class="preview-link">Browse All</a>
      </div>
      
      <div class="preview-card">
        <h4>Consumption</h4>
        <div class="tool-count">{{ consumption_tools.size }} tools</div>
        <a href="{{ site.baseurl }}/tools/" class="preview-link">Browse All</a>
      </div>
    </div>
  </section>
</div>
