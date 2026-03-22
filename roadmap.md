---
layout: default
title: "Data Engineering Roadmap"
---

<div class="page-header">
  <h1 class="page-title">Data Engineering Roadmap</h1>
  <p class="page-subtitle">Your guide from foundations to advanced data systems</p>
</div>

<div class="container">
  <section class="roadmap-section">
    <h2 class="section-title">🏗️ Foundations</h2>
    <p class="section-description">Start here if you're new to data engineering</p>
    
    <div class="foundation-grid">
      <div class="foundation-item">
        <h3>SQL</h3>
        <p>The language of data. Master SELECT, JOIN, GROUP BY, and window functions.</p>
        <div class="next-step">Next step → <a href="#core-engineering">Core Engineering</a></div>
      </div>
      
      <div class="foundation-item">
        <h3>Python</h3>
        <p>Essential for data manipulation, automation, and modern data tools.</p>
        <div class="next-step">Next step → <a href="#core-engineering">Core Engineering</a></div>
      </div>
      
      <div class="foundation-item">
        <h3>Apache Spark (PySpark)</h3>
        <p>Big data processing framework for distributed computing and large-scale data analysis.</p>
        <div class="next-step">Next step → <a href="#core-engineering">Core Engineering</a></div>
      </div>
      
      <div class="foundation-item">
        <h3>Linux</h3>
        <p>Command-line skills and shell scripting for data pipeline operations.</p>
        <div class="next-step">Next step → <a href="#core-engineering">Core Engineering</a></div>
      </div>
    </div>
  </section>

  <section class="roadmap-section" id="core-engineering">
    <h2 class="section-title">⚙️ Core Data Engineering</h2>
    <p class="section-description">Essential concepts and tools for data professionals</p>
    
    <div class="core-grid">
      <div class="core-item">
        <h3>Data Modeling</h3>
        <p>Designing schemas, relationships, and data architectures.</p>
        <div class="next-step">Next step → <a href="#layers">Data Layers</a></div>
      </div>
      
      <div class="core-item">
        <h3>ETL / ELT</h3>
        <p>Extract, Transform, Load patterns and modern data pipelines.</p>
        <div class="next-step">Next step → <a href="#layers">Data Layers</a></div>
      </div>
    </div>
  </section>

  <section class="roadmap-section" id="layers">
    <h2 class="section-title">🏢 Data Engineering Layers</h2>
    <p class="section-description">Understanding the complete data lifecycle</p>
    
    <div class="layers-grid">
      <div class="layer-item">
        <h3><a href="{{ site.baseurl }}/layers/data-sources/">Data Sources</a></h3>
        <p>Where data originates and how to access it</p>
        <div class="next-step">Next step → <a href="{{ site.baseurl }}/layers/data-ingestion/">Data Ingestion</a></div>
      </div>
      
      <div class="layer-item">
        <h3><a href="{{ site.baseurl }}/layers/data-ingestion/">Data Ingestion</a></h3>
        <p>Moving data from sources to storage systems</p>
        <div class="next-step">Next step → <a href="{{ site.baseurl }}/layers/data-processing/">Data Processing</a></div>
      </div>
      
      <div class="layer-item">
        <h3><a href="{{ site.baseurl }}/layers/data-processing/">Data Processing</a></h3>
        <p>Transforming raw data into valuable insights</p>
        <div class="next-step">Next step → <a href="{{ site.baseurl }}/layers/data-storage/">Data Storage</a></div>
      </div>
      
      <div class="layer-item">
        <h3><a href="{{ site.baseurl }}/layers/data-storage/">Data Storage</a></h3>
        <p>Storing processed data for analysis and consumption</p>
        <div class="next-step">Next step → <a href="{{ site.baseurl }}/layers/data-consumption/">Data Consumption</a></div>
      </div>
      
      <div class="layer-item">
        <h3><a href="{{ site.baseurl }}/layers/data-consumption/">Data Consumption</a></h3>
        <p>Making data accessible to users and applications</p>
        <div class="next-step">Final step → <a href="{{ site.baseurl }}/tools/">Explore Tools</a></div>
      </div>
    </div>
  </section>

  <section class="roadmap-section">
    <h2 class="section-title">🛠️ Explore Tools</h2>
    <p class="section-description">Find the right tools for each layer</p>
    
    <div class="tools-cta">
      <a href="{{ site.baseurl }}/tools/" class="cta-button">Browse Complete Tools Catalog</a>
    </div>
  </section>

  <section class="roadmap-section">
    <h2 class="section-title">🎯 Learning Paths</h2>
    <p class="section-description">Common journeys and recommendations</p>
    
    <div class="path-grid">
      <div class="path-item">
        <h3>Beginner Path</h3>
        <p>SQL → Python → PySpark → Basic ETL → Simple BI</p>
        <div class="time-estimate">3-6 months</div>
      </div>
      
      <div class="path-item">
        <h3>Analytics Engineer</h3>
        <p>Advanced SQL → Data Modeling → dbt → PySpark → BI Tools</p>
        <div class="time-estimate">6-12 months</div>
      </div>
      
      <div class="path-item">
        <h3>Data Platform Engineer</h3>
        <p>Python → PySpark → Orchestration → Cloud Architecture → DevOps</p>
        <div class="time-estimate">12-24 months</div>
      </div>
    </div>
  </section>
</div>
