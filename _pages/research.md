---
title: "Research"
layout: gridlay
sitemap: false
permalink: /research/
---

## Research

<p class="section-copy">My current work centers on building practical robot learning systems that can be trained in simulation, shaped by people, and evaluated clearly enough to trust on real hardware.</p>

{% for area in site.data.research_areas %}
<div class="jumbotron section-card">
  <h3>{{ area.title }}</h3>
  <p>{{ area.description }}</p>
  <ul class="clean-list">
    {% for highlight in area.highlights %}
      <li>{{ highlight }}</li>
    {% endfor %}
  </ul>
</div>
{% endfor %}
