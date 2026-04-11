---
layout: default
title: "Data Engineering Skills Guide"
---

<div class="page-header">
  <h1 class="page-title">Data Engineering Skills Guide</h1>
  <p class="page-subtitle">Essential technical and soft skills for data engineers</p>
</div>

<div class="container">
  <!-- Skills Assessment Tool -->
  <section class="skills-section">
    <h2 class="section-title"> Skills Assessment</h2>
    <p class="section-description">Find out which skills you need to focus on</p>
    
    <div class="assessment-tool">
      <div class="assessment-section">
        <h3>What's your current level?</h3>
        <div class="assessment-options">
          <label class="assessment-option">
            <input type="radio" name="level" value="beginner" onchange="filterSkills()">
            <span>Beginner (0-2 years)</span>
          </label>
          <label class="assessment-option">
            <input type="radio" name="level" value="intermediate" onchange="filterSkills()">
            <span>Intermediate (2-5 years)</span>
          </label>
          <label class="assessment-option">
            <input type="radio" name="level" value="advanced" onchange="filterSkills()">
            <span>Advanced (5+ years)</span>
          </label>
        </div>
      </div>
      
      <div class="assessment-section">
        <h3>What's your target role?</h3>
        <div class="assessment-options">
          <label class="assessment-option">
            <input type="radio" name="role" value="junior" onchange="filterSkills()">
            <span>Junior Data Engineer</span>
          </label>
          <label class="assessment-option">
            <input type="radio" name="role" value="data-engineer" onchange="filterSkills()">
            <span>Data Engineer</span>
          </label>
          <label class="assessment-option">
            <input type="radio" name="role" value="senior" onchange="filterSkills()">
            <span>Senior Data Engineer</span>
          </label>
        </div>
      </div>
      
      <div id="skills-results" class="skills-results" style="display: none;">
        <h3>Your Skill Priorities</h3>
        <div id="skills-content">
          <!-- Results will be populated here -->
        </div>
      </div>
    </div>
  </section>

  <!-- Technical Skills -->
  <section class="skills-section">
    <h2 class="section-title"> Technical Skills</h2>
    <p class="section-description">Core technical competencies for data engineering</p>
    
    <div class="skills-grid">
      <div class="skill-card essential" data-level="beginner" data-role="generalist,analytics,platform">
        <div class="skill-header">
          <h3>SQL Proficiency</h3>
          <span class="skill-level essential">Essential</span>
        </div>
        <p>Writing efficient queries, understanding joins, window functions, and optimization</p>
        <div class="skill-resources">
          <a href="{{ site.baseurl }}/roadmap/" class="skill-link">Learn on Roadmap</a>
        </div>
      </div>
      
      <div class="skill-card essential" data-level="beginner" data-role="generalist,analytics,platform">
        <div class="skill-header">
          <h3>Programming (Python/Scala)</h3>
          <span class="skill-level essential">Essential</span>
        </div>
        <p>Data manipulation, automation, and building data pipelines</p>
        <div class="skill-resources">
          <a href="{{ site.baseurl }}/roadmap/" class="skill-link">Learn on Roadmap</a>
        </div>
      </div>
      
      <div class="skill-card essential" data-level="intermediate" data-role="generalist,analytics,platform">
        <div class="skill-header">
          <h3>Data Warehousing</h3>
          <span class="skill-level essential">Essential</span>
        </div>
        <p>Warehouse design, star/snowflake schemas, optimization</p>
        <div class="skill-resources">
          <a href="{{ site.baseurl }}/database-guide/" class="skill-link">Database Guide</a>
        </div>
      </div>
      
      <div class="skill-card essential" data-level="intermediate" data-role="generalist,analytics,platform">
        <div class="skill-header">
          <h3>ETL/ELT Frameworks</h3>
          <span class="skill-level essential">Essential</span>
        </div>
        <p>Building data pipelines, understanding ETL vs ELT approaches</p>
        <div class="skill-resources">
          <a href="{{ site.baseurl }}/roadmap/" class="skill-link">Learn on Roadmap</a>
        </div>
      </div>
      
      <div class="skill-card important" data-level="intermediate" data-role="generalist,analytics,platform">
        <div class="skill-header">
          <h3>Cloud Platforms</h3>
          <span class="skill-level important">Important</span>
        </div>
        <p>AWS, GCP, or Azure - storage, compute, and managed services</p>
        <div class="skill-resources">
          <a href="{{ site.baseurl }}/tools/" class="skill-link">Cloud Tools</a>
        </div>
      </div>
      
      <div class="skill-card important" data-level="intermediate" data-role="generalist,analytics,platform">
        <div class="skill-header">
          <h3>Data Modeling</h3>
          <span class="skill-level important">Important</span>
        </div>
        <p>Schema design, normalization, dimensional modeling</p>
        <div class="skill-resources">
          <a href="{{ site.baseurl }}/roadmap/" class="skill-link">Core Engineering</a>
        </div>
      </div>
      
      <div class="skill-card advanced" data-level="advanced" data-role="generalist,platform">
        <div class="skill-header">
          <h3>Big Data Tools</h3>
          <span class="skill-level advanced">Advanced</span>
        </div>
        <p>Spark, Hadoop, Kafka for large-scale data processing</p>
        <div class="skill-resources">
          <a href="{{ site.baseurl }}/tools/" class="skill-link">Tools Catalog</a>
        </div>
      </div>
      
      <div class="skill-card important" data-level="intermediate" data-role="generalist,analytics,platform">
        <div class="skill-header">
          <h3>Automation & Orchestration</h3>
          <span class="skill-level important">Important</span>
        </div>
        <p>Airflow, dbt, or similar tools for pipeline automation</p>
        <div class="skill-resources">
          <a href="{{ site.baseurl }}/tools/" class="skill-link">Tools Catalog</a>
        </div>
      </div>
      
      <div class="skill-card advanced" data-level="advanced" data-role="generalist,platform">
        <div class="skill-header">
          <h3>Data Governance & Security</h3>
          <span class="skill-level advanced">Advanced</span>
        </div>
        <p>Data privacy, encryption, compliance (GDPR, etc.)</p>
        <div class="skill-resources">
          <a href="{{ site.baseurl }}/roadmap/" class="skill-link">Data Quality</a>
        </div>
      </div>
      
      <div class="skill-card important" data-level="intermediate" data-role="generalist,analytics,platform">
        <div class="skill-header">
          <h3>API Integration</h3>
          <span class="skill-level important">Important</span>
        </div>
        <p>REST APIs, data extraction from external systems</p>
        <div class="skill-resources">
          <a href="{{ site.baseurl }}/tools/" class="skill-link">Tools Catalog</a>
        </div>
      </div>
    </div>
  </section>

  <!-- Role-Specific Requirements -->
  <section class="skills-section">
    <h2 class="section-title"> Role-Specific Skill Requirements</h2>
    <p class="section-description">What you need for each data engineering role level</p>
    
    <div class="role-requirements">
      <!-- Junior Data Engineer -->
      <div class="role-card junior">
        <div class="role-header">
          <h3>Junior Data Engineer</h3>
          <span class="role-badge junior">Entry Level</span>
        </div>
        <p class="role-description">Despite the junior title, data engineering is typically not an entry-level job and therefore few of these positions exist. If you are starting from scratch, the best advice is to find an adjacent role and transition into data engineering. If you are already in an adjacent role such as: BI developer, SQL developer, or backend engineer then you probably have overlapping experience.</p>
        
        <div class="skill-requirements">
          <div class="requirement-group">
            <h4>Minimum Skills Required:</h4>
            <div class="skill-list">
              <div class="skill-item beginner">
                <span class="skill-name">SQL</span>
                <span class="skill-level-badge beginner">Beginner</span>
              </div>
              <div class="skill-item beginner">
                <span class="skill-name">Data Modeling</span>
                <span class="skill-level-badge beginner">Beginner</span>
              </div>
              <div class="skill-item beginner">
                <span class="skill-name">Relational Database</span>
                <span class="skill-level-badge beginner">Beginner</span>
              </div>
              <div class="skill-item beginner">
                <span class="skill-name">Soft Skills</span>
                <span class="skill-level-badge beginner">Beginner</span>
              </div>
            </div>
          </div>
          
          <div class="requirement-group">
            <h4>Nice to Have:</h4>
            <div class="skill-list">
              <div class="skill-item beginner">
                <span class="skill-name">Scripting Language (Python, Java, or Scala)</span>
                <span class="skill-level-badge beginner">Beginner</span>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Data Engineer -->
      <div class="role-card mid">
        <div class="role-header">
          <h3>Data Engineer</h3>
          <span class="role-badge mid">Mid Level</span>
        </div>
        
        <div class="skill-requirements">
          <div class="requirement-group">
            <h4>Minimum Skills Required:</h4>
            <div class="skill-list">
              <div class="skill-item intermediate">
                <span class="skill-name">SQL</span>
                <span class="skill-level-badge intermediate">Intermediate</span>
              </div>
              <div class="skill-item intermediate">
                <span class="skill-name">Data Modeling</span>
                <span class="skill-level-badge intermediate">Intermediate</span>
              </div>
              <div class="skill-item intermediate">
                <span class="skill-name">Scripting Language (Python, Java, or Scala)</span>
                <span class="skill-level-badge intermediate">Intermediate</span>
              </div>
              <div class="skill-item intermediate">
                <span class="skill-name">Indexing & Query Optimization</span>
                <span class="skill-level-badge intermediate">Intermediate</span>
              </div>
              <div class="skill-item intermediate">
                <span class="skill-name">Batch Data Processing</span>
                <span class="skill-level-badge intermediate">Intermediate</span>
              </div>
              <div class="skill-item intermediate">
                <span class="skill-name">Soft Skills</span>
                <span class="skill-level-badge intermediate">Intermediate</span>
              </div>
              <div class="skill-item intermediate">
                <span class="skill-name">Relational Database</span>
                <span class="skill-level-badge intermediate">Intermediate</span>
              </div>
              <div class="skill-item beginner">
                <span class="skill-name">Online Transaction Processing</span>
                <span class="skill-level-badge beginner">Beginner</span>
              </div>
              <div class="skill-item beginner">
                <span class="skill-name">Data Pipeline</span>
                <span class="skill-level-badge beginner">Beginner</span>
              </div>
              <div class="skill-item beginner">
                <span class="skill-name">Data Warehouse</span>
                <span class="skill-level-badge beginner">Beginner</span>
              </div>
            </div>
          </div>
          
          <div class="requirement-group">
            <h4>Nice to Have:</h4>
            <div class="skill-list">
              <div class="skill-item intermediate">
                <span class="skill-name">Cloud Platform (AWS, Azure, or GCP)</span>
                <span class="skill-level-badge intermediate">Intermediate</span>
              </div>
              <div class="skill-item beginner">
                <span class="skill-name">Stream Data Processing</span>
                <span class="skill-level-badge beginner">Beginner</span>
              </div>
              <div class="skill-item beginner">
                <span class="skill-name">Online Analytical Processing</span>
                <span class="skill-level-badge beginner">Beginner</span>
              </div>
              <div class="skill-item beginner">
                <span class="skill-name">Reporting Tools (Tableau, Superset, Metabase)</span>
                <span class="skill-level-badge beginner">Beginner</span>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Senior Data Engineer -->
      <div class="role-card senior">
        <div class="role-header">
          <h3>Senior Data Engineer</h3>
          <span class="role-badge senior">Senior Level</span>
        </div>
        
        <div class="skill-requirements">
          <div class="requirement-group">
            <h4>Minimum Skills Required:</h4>
            <div class="skill-list">
              <div class="skill-item advanced">
                <span class="skill-name">Soft Skills</span>
                <span class="skill-level-badge advanced">Intermediate/Advanced</span>
              </div>
              <div class="skill-item advanced">
                <span class="skill-name">SQL</span>
                <span class="skill-level-badge advanced">Advanced</span>
              </div>
              <div class="skill-item advanced">
                <span class="skill-name">Data Modeling</span>
                <span class="skill-level-badge advanced">Advanced</span>
              </div>
              <div class="skill-item advanced">
                <span class="skill-name">Scripting Language (Python, Java, or Scala)</span>
                <span class="skill-level-badge advanced">Advanced</span>
              </div>
              <div class="skill-item advanced">
                <span class="skill-name">Indexing & Query Optimization</span>
                <span class="skill-level-badge advanced">Advanced</span>
              </div>
              <div class="skill-item advanced">
                <span class="skill-name">Cloud Platform (AWS, Azure, or GCP)</span>
                <span class="skill-level-badge advanced">Advanced</span>
              </div>
              <div class="skill-item beginner">
                <span class="skill-name">Infrastructure as Code</span>
                <span class="skill-level-badge beginner">Beginner</span>
              </div>
              <div class="skill-item advanced">
                <span class="skill-name">Batch Data Processing</span>
                <span class="skill-level-badge advanced">Advanced</span>
              </div>
              <div class="skill-item advanced">
                <span class="skill-name">Relational Database</span>
                <span class="skill-level-badge advanced">Advanced</span>
              </div>
              <div class="skill-item advanced">
                <span class="skill-name">Non-relational Database</span>
                <span class="skill-level-badge advanced">Advanced</span>
              </div>
              <div class="skill-item intermediate">
                <span class="skill-name">Online Transaction Processing</span>
                <span class="skill-level-badge intermediate">Intermediate</span>
              </div>
              <div class="skill-item intermediate">
                <span class="skill-name">Online Analytical Processing</span>
                <span class="skill-level-badge intermediate">Intermediate</span>
              </div>
              <div class="skill-item advanced">
                <span class="skill-name">Data Pipeline</span>
                <span class="skill-level-badge advanced">Advanced</span>
              </div>
            </div>
          </div>
          
          <div class="requirement-group">
            <h4>Nice to Have:</h4>
            <div class="skill-list">
              <div class="skill-item advanced">
                <span class="skill-name">Infrastructure as Code</span>
                <span class="skill-level-badge advanced">Advanced</span>
              </div>
              <div class="skill-item intermediate">
                <span class="skill-name">Reporting Tools (Tableau, Superset, Metabase)</span>
                <span class="skill-level-badge intermediate">Beginner/Intermediate</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Soft Skills -->
  <section class="skills-section">
    <h2 class="section-title"> Soft Skills</h2>
    <p class="section-description">Non-technical skills that differentiate great data engineers</p>
    
    <div class="soft-skills-grid">
      <div class="soft-skill-card essential" data-level="beginner" data-role="generalist,analytics,platform">
        <div class="soft-skill-header">
          <h3>Communication</h3>
          <span class="skill-level essential">Essential</span>
        </div>
        <p>Explaining technical concepts to non-technical stakeholders, understanding requirements</p>
      </div>
      
      <div class="soft-skill-card essential" data-level="beginner" data-role="generalist,analytics,platform">
        <div class="soft-skill-header">
          <h3>Problem-Solving</h3>
          <span class="skill-level essential">Essential</span>
        </div>
        <p>Debugging pipelines, optimizing performance, creative troubleshooting</p>
      </div>
      
      <div class="soft-skill-card essential" data-level="beginner" data-role="generalist,analytics,platform">
        <div class="soft-skill-header">
          <h3>Collaboration</h3>
          <span class="skill-level essential">Essential</span>
        </div>
        <p>Working with analysts, scientists, and IT teams effectively</p>
      </div>
      
      <div class="soft-skill-card important" data-level="intermediate" data-role="generalist,analytics,platform">
        <div class="soft-skill-header">
          <h3>Attention to Detail</h3>
          <span class="skill-level important">Important</span>
        </div>
        <p>Ensuring data integrity, catching small errors before they become big problems</p>
      </div>
      
      <div class="soft-skill-card important" data-level="intermediate" data-role="generalist,analytics,platform">
        <div class="soft-skill-header">
          <h3>Adaptability</h3>
          <span class="skill-level important">Important</span>
        </div>
        <p>Learning new technologies, adapting to changing requirements</p>
      </div>
      
      <div class="soft-skill-card advanced" data-level="advanced" data-role="generalist,platform">
        <div class="soft-skill-header">
          <h3>Project Management</h3>
          <span class="skill-level advanced">Advanced</span>
        </div>
        <p>Prioritizing tasks, managing deadlines, coordinating projects</p>
      </div>
    </div>
  </section>

  <!-- Learning Path -->
  <section class="skills-section">
    <h2 class="section-title"> Learning Path</h2>
    <p class="section-description">Recommended progression for skill development</p>
    
    <div class="learning-path">
      <div class="path-stage">
        <div class="stage-number">1</div>
        <div class="stage-content">
          <h3>Foundation (Months 0-6)</h3>
          <ul>
            <li>Master SQL basics</li>
            <li>Learn Python fundamentals</li>
            <li>Understand basic data concepts</li>
            <li>Practice communication skills</li>
          </ul>
        </div>
      </div>
      
      <div class="path-stage">
        <div class="stage-number">2</div>
        <div class="stage-content">
          <h3>Core Skills (Months 6-18)</h3>
          <ul>
            <li>Build ETL/ELT pipelines</li>
            <li>Learn data warehousing</li>
            <li>Master cloud platform basics</li>
            <li>Develop problem-solving abilities</li>
          </ul>
        </div>
      </div>
      
      <div class="path-stage">
        <div class="stage-number">3</div>
        <div class="stage-content">
          <h3>Advanced (Months 18+)</h3>
          <ul>
            <li>Big data tools (Spark, Kafka)</li>
            <li>Data governance & security</li>
            <li>Project management</li>
            <li>System architecture design</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</div>

<script>
// Skills assessment logic
function filterSkills() {
  const level = document.querySelector('input[name="level"]:checked')?.value;
  const role = document.querySelector('input[name="role"]:checked')?.value;
  const resultsDiv = document.getElementById('skills-results');
  const skillsContent = document.getElementById('skills-content');
  
  if (!level || !role) {
    resultsDiv.style.display = 'none';
    return;
  }
  
  // Skill recommendations based on level and role
  const skillPriorities = {
    'beginner-generalist': [
      { skill: 'SQL Proficiency', priority: 'Start here - foundation of all data work' },
      { skill: 'Programming (Python/Scala)', priority: 'Essential for building pipelines' },
      { skill: 'Communication', priority: 'Critical for team collaboration' },
      { skill: 'Problem-Solving', priority: 'Daily requirement for debugging' }
    ],
    'beginner-analytics': [
      { skill: 'SQL Proficiency', priority: 'Core skill for analytics work' },
      { skill: 'Programming (Python/Scala)', priority: 'Data manipulation and analysis' },
      { skill: 'Data Warehousing', priority: 'Understanding analytics structures' },
      { skill: 'Communication', priority: 'Working with business stakeholders' }
    ],
    'beginner-platform': [
      { skill: 'Programming (Python/Scala)', priority: 'Building robust systems' },
      { skill: 'SQL Proficiency', priority: 'Data access and optimization' },
      { skill: 'Cloud Platforms', priority: 'Modern infrastructure foundation' },
      { skill: 'Problem-Solving', priority: 'System troubleshooting' }
    ],
    'intermediate-generalist': [
      { skill: 'Data Warehousing', priority: 'Design efficient data structures' },
      { skill: 'ETL/ELT Frameworks', priority: 'Build reliable pipelines' },
      { skill: 'Cloud Platforms', priority: 'Scale data infrastructure' },
      { skill: 'Data Modeling', priority: 'Optimize data organization' }
    ],
    'intermediate-analytics': [
      { skill: 'Data Modeling', priority: 'Design for analytics performance' },
      { skill: 'Data Warehousing', priority: 'Optimize for reporting' },
      { skill: 'ETL/ELT Frameworks', priority: 'Build analytics pipelines' },
      { skill: 'Attention to Detail', priority: 'Ensure data accuracy' }
    ],
    'intermediate-platform': [
      { skill: 'Cloud Platforms', priority: 'Build scalable infrastructure' },
      { skill: 'Automation & Orchestration', priority: 'Manage complex systems' },
      { skill: 'Big Data Tools', priority: 'Handle large-scale data' },
      { skill: 'Data Governance & Security', priority: 'Secure systems' }
    ],
    'advanced-generalist': [
      { skill: 'Big Data Tools', priority: 'Process massive datasets' },
      { skill: 'Data Governance & Security', priority: 'Enterprise requirements' },
      { skill: 'Project Management', priority: 'Lead data initiatives' },
      { skill: 'API Integration', priority: 'Connect diverse systems' }
    ],
    'advanced-analytics': [
      { skill: 'Data Modeling', priority: 'Complex analytical structures' },
      { skill: 'Data Warehousing', priority: 'Advanced optimization' },
      { skill: 'Project Management', priority: 'Lead analytics projects' },
      { skill: 'Communication', priority: 'Stakeholder management' }
    ],
    'advanced-platform': [
      { skill: 'Big Data Tools', priority: 'Scale to enterprise level' },
      { skill: 'Data Governance & Security', priority: 'Enterprise security' },
      { skill: 'Automation & Orchestration', priority: 'Complex system management' },
      { skill: 'Project Management', priority: 'Lead infrastructure projects' }
    ]
  };
  
  const key = `${level}-${role}`;
  const priorities = skillPriorities[key] || [];
  
  if (priorities.length > 0) {
    let skillsHTML = '<div class="priority-list">';
    priorities.forEach(item => {
      skillsHTML += `
        <div class="priority-item">
          <h4>${item.skill}</h4>
          <p>${item.priority}</p>
        </div>
      `;
    });
    skillsHTML += '</div>';
    
    skillsContent.innerHTML = skillsHTML;
    resultsDiv.style.display = 'block';
  } else {
    resultsDiv.style.display = 'none';
  }
}
</script>
