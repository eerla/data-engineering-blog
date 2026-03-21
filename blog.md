---
layout: default
title: "Blog"
---

<div class="page-header">
  <h1 class="page-title">Blog</h1>
  <p class="page-subtitle">Real-world data engineering insights, no fluff.</p>
</div>

<div class="container">
  <div class="blog-list">
    {% for post in site.posts %}
      <article class="blog-item">
        <h2 class="blog-title">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h2>
        <div class="blog-meta">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
          {% if post.categories %}
            <span class="post-categories">
              in 
              {% for category in post.categories %}
                <span class="category">{{ category }}</span>
              {% endfor %}
            </span>
          {% endif %}
        </div>
        {% if post.excerpt %}
          <p class="blog-excerpt">{{ post.excerpt | strip_html }}</p>
        {% endif %}
        {% if post.tags %}
          <div class="post-tags">
            <span class="tags-label">Tags:</span>
            {% for tag in post.tags %}
              <a href="/tag/{{ tag | slugify }}/" class="tag">{{ tag }}</a>
            {% endfor %}
          </div>
        {% endif %}
      </article>
    {% endfor %}
  </div>
</div>
