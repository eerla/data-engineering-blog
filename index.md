---
layout: default
title: "Home"
---

<div class="page-header">
  <h1 class="page-title">Most Data Engineering Advice is Wrong.</h1>
  <p class="page-subtitle">Here's what actually works in real-world systems.</p>
</div>

<div class="container">
  <div class="text-center mb-3">
    <h2>I'm Guru, Lead Engineer</h2>
    <p class="page-subtitle">I build data systems that work, not systems that look good on slides.</p>
  </div>

  <div class="text-center mb-4">
    <h3>❌ Bad Advice → ✅ What Actually Works</h3>
    <div style="max-width: 800px; margin: 0 auto;">
      <div style="background: var(--background-light); padding: 1.5rem; border-radius: 8px; margin-bottom: 1rem; text-align: left;">
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1rem;">
          <div>
            <h4 style="color: #e74c3c; margin-bottom: 0.5rem;">❌ "Use the latest tech stack"</h4>
            <p style="margin-bottom: 0; font-size: 0.9rem;">Chasing trends, complex setups, vendor lock-in</p>
          </div>
          <div>
            <h4 style="color: #27ae60; margin-bottom: 0.5rem;">✅ Use boring technology</h4>
            <p style="margin-bottom: 0; font-size: 0.9rem;">PostgreSQL, Python, S3. Things that actually work.</p>
          </div>
        </div>
      </div>
      
      <div style="background: var(--background-light); padding: 1.5rem; border-radius: 8px; margin-bottom: 1rem; text-align: left;">
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1rem;">
          <div>
            <h4 style="color: #e74c3c; margin-bottom: 0.5rem;">❌ "Build perfect data models"</h4>
            <p style="margin-bottom: 0; font-size: 0.9rem;">Months of modeling, over-engineered schemas</p>
          </div>
          <div>
            <h4 style="color: #27ae60; margin-bottom: 0.5rem;">✅ Build good enough models</h4>
            <p style="margin-bottom: 0; font-size: 0.9rem;">Start simple, evolve as needs change. Schema-on-read.</p>
          </div>
        </div>
      </div>
      
      <div style="background: var(--background-light); padding: 1.5rem; border-radius: 8px; margin-bottom: 1rem; text-align: left;">
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1rem;">
          <div>
            <h4 style="color: #e74c3c; margin-bottom: 0.5rem;">❌ "Real-time processing always"</h4>
            <p style="margin-bottom: 0; font-size: 0.9rem;">Expensive, complex, often unnecessary</p>
          </div>
          <div>
            <h4 style="color: #27ae60; margin-bottom: 0.5rem;">✅ Batch when you can</h4>
            <p style="margin-bottom: 0; font-size: 0.9rem;">80% of use cases. Stream when you absolutely must.</p>
          </div>
        </div>
      </div>
      
      <div style="background: var(--background-light); padding: 1.5rem; border-radius: 8px; margin-bottom: 1rem; text-align: left;">
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1rem;">
          <div>
            <h4 style="color: #e74c3c; margin-bottom: 0.5rem;">❌ "Microservices for everything"</h4>
            <p style="margin-bottom: 0; font-size: 0.9rem;">Distributed complexity, operational overhead</p>
          </div>
          <div>
            <h4 style="color: #27ae60; margin-bottom: 0.5rem;">✅ Start simple, break apart later</h4>
            <p style="margin-bottom: 0; font-size: 0.9rem;">Monolith first. Split when you feel pain.</p>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="text-center mb-4">
    <h3>🎯 3 Things That Actually Work Right Now</h3>
    <div style="max-width: 700px; margin: 0 auto;">
      <div style="background: var(--background-secondary); padding: 1.5rem; border-radius: 8px; margin-bottom: 1rem; text-align: left; border-left: 4px solid var(--primary-color);">
        <h4 style="color: var(--primary-color); margin-bottom: 0.5rem;">1. Start with CSV, not complex formats</h4>
        <p style="margin-bottom: 0;">Ship faster, get feedback, optimize later. I've seen teams spend 3 months on a "perfect" Parquet pipeline when CSV would have solved the business problem in 3 days.</p>
      </div>
      
      <div style="background: var(--background-secondary); padding: 1.5rem; border-radius: 8px; margin-bottom: 1rem; text-align: left; border-left: 4px solid var(--primary-color);">
        <h4 style="color: var(--primary-color); margin-bottom: 0.5rem;">2. SQL first, Python second</h4>
        <p style="margin-bottom: 0;">80% of data problems can be solved with SQL. It's faster, more maintainable, and your analysts can actually read it.</p>
      </div>
      
      <div style="background: var(--background-secondary); padding: 1.5rem; border-radius: 8px; margin-bottom: 1rem; text-align: left; border-left: 4px solid var(--primary-color);">
        <h4 style="color: var(--primary-color); margin-bottom: 0.5rem;">3. Manual beats automated for first 3 months</h4>
        <p style="margin-bottom: 0;">Understand the workflow before you automate. I've seen $500k automation projects for processes that took 2 hours per week.</p>
      </div>
    </div>
  </div>

  <div class="text-center mb-3">
    <h3>What I Write About</h3>
    <div style="max-width: 600px; margin: 0 auto;">
      <ul style="text-align: left; line-height: 2;">
        <li><strong>Real-world data engineering</strong> - not academic theory</li>
        <li><strong>System design tradeoffs</strong> - why simple beats complex</li>
        <li><strong>Tool evaluations</strong> - when to use what (and when not to)</li>
        <li><strong>Lessons from production</strong> - what actually breaks and why</li>
        <li><strong>Opinions on industry trends</strong> - separating hype from reality</li>
      </ul>
    </div>
  </div>

  <div class="text-center mb-3">
    <h3>Explore</h3>
    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 1rem; max-width: 800px; margin: 0 auto;">
      <a href="{{ site.baseurl }}/tools/" style="background: var(--primary-color); color: white; padding: 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
        🛠️ Tools Catalog
      </a>
      <a href="{{ site.baseurl }}/cloud-tools/" style="background: var(--secondary-color); color: white; padding: 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
        ☁️ Cloud Tools
      </a>
      <a href="{{ site.baseurl }}/roadmap/" style="background: var(--primary-color); color: white; padding: 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
        🗺️ Learning Roadmap
      </a>
      <a href="{{ site.baseurl }}/layers/" style="background: var(--primary-color); color: white; padding: 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
        🏢 Data Layers
      </a>
      <a href="{{ site.baseurl }}/comparisons/" style="background: var(--secondary-color); color: white; padding: 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
        ⚖️ Tool Comparisons
      </a>
      <a href="{{ site.baseurl }}/blog/" style="background: var(--primary-color); color: white; padding: 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
        📝 Blog Posts
      </a>
      <a href="{{ site.baseurl }}/series/" style="background: var(--secondary-color); color: white; padding: 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
        📚 Content Series
      </a>
      <a href="{{ site.baseurl }}/projects/" style="background: var(--primary-color); color: white; padding: 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
        🚀 Projects
      </a>
      <a href="{{ site.baseurl }}/about/" style="background: var(--secondary-color); color: white; padding: 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
        👤 About Me
      </a>
    </div>
  </div>

  <div class="text-center">
    <h3>Connect</h3>
    <p>Find me on <a href="https://github.com/eerla" target="_blank">GitHub</a>, <a href="https://medium.com/@think-data" target="_blank">Medium</a>, and <a href="https://www.linkedin.com/in/guru-e/" target="_blank">LinkedIn</a>.</p>
  </div>
</div>
