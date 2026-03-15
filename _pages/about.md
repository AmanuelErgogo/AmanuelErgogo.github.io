---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

{% assign member = site.data.pi[0] %}

## About

<div class="jumbotron section-card">
  <div class="row align-items-center">
    <div class="col-md-4 text-center">
      {% if member.photo %}
        <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px" alt="{{ member.name }}">
      {% else %}
        <div class="profile-placeholder profile-placeholder-large">{{ member.initials }}</div>
      {% endif %}
    </div>
    <div class="col-md-8">
      <h3>{{ member.name }}</h3>
      <p class="item-meta">{{ member.info }}</p>
      {% for paragraph in member.summary %}
        <p>{{ paragraph }}</p>
      {% endfor %}
      <div class="link-row">
        <a class="btn btn-primary btn-sm" href="{{ member.cv | relative_url }}" target="_blank" rel="noreferrer">Resume</a>
        <a class="btn btn-outline-primary btn-sm" href="{{ member.github }}" target="_blank" rel="noreferrer">GitHub</a>
        <a class="btn btn-outline-primary btn-sm" href="{{ member.linkedin }}" target="_blank" rel="noreferrer">LinkedIn</a>
        <a class="btn btn-outline-primary btn-sm" href="mailto:{{ member.email }}">Email</a>
      </div>
    </div>
  </div>
</div>

## Education

<div class="jumbotron section-card">
  <ul class="clean-list">
    {% for education in member.education %}
      <li>{{ education }}</li>
    {% endfor %}
  </ul>
</div>

## Skills

<div class="row">
  {% for skill in site.data.skills %}
  <div class="col-md-6">
    <div class="jumbotron section-card">
      <h4>{{ skill.category }}</h4>
      <div class="tag-row">
        {% for item in skill.items %}
          <span class="tag-pill">{{ item }}</span>
        {% endfor %}
      </div>
    </div>
  </div>
  {% endfor %}
</div>
