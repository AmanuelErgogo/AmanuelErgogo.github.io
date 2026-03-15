---
title: "Projects"
layout: gridlay
sitemap: false
permalink: /projects/
---

## Projects

<p class="section-copy">Selected work spanning simulation, teleoperation, imitation learning, reinforcement learning, and real-world robot deployment.</p>

{% for project in site.data.projects %}
<div class="jumbotron section-card">
  <h3>{{ project.title }}</h3>
  <p class="item-meta">{{ project.subtitle }}</p>
  <p>{{ project.description }}</p>
  <div class="tag-row">
    {% for tag in project.tags %}
      <span class="tag-pill">{{ tag }}</span>
    {% endfor %}
  </div>
  <ul class="clean-list">
    {% for highlight in project.highlights %}
      <li>{{ highlight }}</li>
    {% endfor %}
  </ul>
  {% if project.links.size > 0 %}
  <div class="link-row">
    {% for link in project.links %}
      <a class="btn btn-outline-primary btn-sm" href="{{ link.url }}" target="_blank" rel="noreferrer">{{ link.label }}</a>
    {% endfor %}
  </div>
  {% endif %}
</div>
{% endfor %}
