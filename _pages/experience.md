---
title: "Experience"
layout: gridlay
sitemap: false
permalink: /experience/
---

## Experience

<p class="section-copy">Research and engineering work spanning robot learning, immersive interfaces, simulation, and real-robot deployment.</p>

{% for item in site.data.experience %}
<div class="jumbotron section-card">
  <div class="experience-header">
    <div>
      <h3>{{ item.role }}</h3>
      <p class="item-meta">{{ item.organization }} | {{ item.location }}</p>
    </div>
    <span class="date-pill">{{ item.dates }}</span>
  </div>
  <ul class="clean-list">
    {% for bullet in item.bullets %}
      <li>{{ bullet }}</li>
    {% endfor %}
  </ul>
</div>
{% endfor %}

## Education

<div class="jumbotron section-card">
  <ul class="clean-list">
    {% for education in site.data.pi[0].education %}
      <li>{{ education }}</li>
    {% endfor %}
  </ul>
  <div class="link-row">
    <a class="btn btn-primary btn-sm" href="{{ '/Resume_AE.pdf' | relative_url }}" target="_blank" rel="noreferrer">Open resume</a>
  </div>
</div>
