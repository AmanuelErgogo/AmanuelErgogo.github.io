---
title: "Publications"
layout: gridlay
sitemap: false
permalink: /publications/
---

## Publications

<p class="section-copy">Selected publications and works in progress related to robot learning, teleoperation, manipulation, and explainable embodied AI.</p>

{% for publication in site.data.publications %}
<div class="jumbotron publication-entry">
  <div class="publication-header">
    <h3>{{ publication.title }}</h3>
    <span class="date-pill">{{ publication.year }}</span>
  </div>
  <p class="item-meta">{{ publication.venue }} | {{ publication.status }} | {{ publication.note }}</p>
  <p>{{ publication.authors }}</p>
  {% if publication.links.size > 0 %}
  <div class="link-row">
    {% for link in publication.links %}
      <a class="btn btn-outline-primary btn-sm" href="{{ link.url }}" target="_blank" rel="noreferrer">{{ link.label }}</a>
    {% endfor %}
  </div>
  {% endif %}
</div>
{% endfor %}
