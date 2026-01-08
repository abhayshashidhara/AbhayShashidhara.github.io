---
layout: single
title: "Projects"
permalink: /projects/
author_profile: true
classes: projects-page
---

<div class="projects-grid">
  {% for p in site.data.projects %}
  <div class="project-card">

    <div class="project-body">
      <h2 class="project-title">{{ p.title }}</h2>

      <div class="project-image-wrap">
        <img class="project-image"
             src="{{ p.image | relative_url }}"
             alt="{{ p.title }}">
      </div>

      <p class="project-desc">{{ p.description }}</p>

      {% if p.stack %}
      <p class="project-stack-text">
        <strong>{{ p.stack | join: " | " }}</strong>
      </p>
      {% endif %}

      <div class="project-actions">
        {% if p.github_url %}
          <a class="project-btn project-btn-ghost"
             href="{{ p.github_url }}"
             target="_blank"
             rel="noopener">GitHub</a>
        {% endif %}

        {% if p.report_url %}
          <a class="project-btn"
             href="{{ p.report_url | relative_url }}"
             target="_blank"
             rel="noopener">Read more</a>
        {% endif %}
      </div>

    </div>
  </div>
  {% endfor %}
</div>
