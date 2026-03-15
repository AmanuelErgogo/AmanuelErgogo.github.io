---
title: "Home"
layout: homelay
sitemap: false
permalink: /
---

{% assign member = site.data.pi[0] %}

<div class="jumbotron hero-card">
  <p class="eyebrow">Robot learning · simulation · teleoperation · sim-to-real</p>
  <h1 class="hero-title">{{ member.name }}</h1>
  <p class="hero-lead">PhD student in Computer Science and Engineering at the University of South Florida building robot learning systems across simulation, VR teleoperation, imitation learning, reinforcement learning, and real-robot deployment.</p>
  <p>My work sits at the intersection of robotics, embodied AI, and human-centered learning systems. I am especially interested in building practical pipelines that connect data collection, simulation, policy training, evaluation, and deployment on physical robots.</p>
  <div class="link-row">
    <a class="btn btn-primary" href="{{ '/Resume_AE.pdf' | relative_url }}" target="_blank" rel="noreferrer">Resume</a>
    <a class="btn btn-outline-primary" href="https://github.com/AmanuelErgogo" target="_blank" rel="noreferrer">GitHub</a>
    <a class="btn btn-outline-primary" href="https://www.linkedin.com/in/amanuel-ergogo-9506631a8/" target="_blank" rel="noreferrer">LinkedIn</a>
    <a class="btn btn-outline-primary" href="mailto:aergogo@usf.edu">Email</a>
  </div>
</div>

## Featured projects

<p class="section-copy">A few projects that best represent the robotics and machine learning work I want this site to emphasize.</p>

{% for project in site.data.projects limit:3 %}
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

## Selected publications

{% for publication in site.data.publications limit:4 %}
<div class="jumbotron publication-entry">
  <h4>{{ publication.title }}</h4>
  <p class="item-meta">{{ publication.venue }} {{ publication.year }} | {{ publication.status }} | {{ publication.note }}</p>
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

## Research direction

<div class="jumbotron section-card">
  <p>I focus on human-in-the-loop robot learning, simulation-driven manipulation, and explainable embodied AI. The common thread is practical robotics: collect better demonstrations, train more capable policies, inspect their failures, and deploy them on real hardware with fewer surprises.</p>
  <div class="link-row">
    <a class="btn btn-outline-primary btn-sm" href="{{ '/research/' | relative_url }}">Research themes</a>
    <a class="btn btn-outline-primary btn-sm" href="{{ '/experience/' | relative_url }}">Experience</a>
    <a class="btn btn-outline-primary btn-sm" href="{{ '/projects/' | relative_url }}">All projects</a>
  </div>
</div>
