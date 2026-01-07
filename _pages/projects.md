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
    <div class="project-image-wrap">
      <img class="project-image" src="{{ p.image | relative_url }}" alt="{{ p.title }}">
    </div>

    <div class="project-body">
      <h2 class="project-title">{{ p.title }}</h2>
      <p class="project-desc">{{ p.description }}</p>

      {% if p.stack %}
      <div class="project-stack">
        {% for s in p.stack %}
          <span class="stack-pill">{{ s }}</span>
        {% endfor %}
      </div>
      {% endif %}

      <div class="project-actions">
        <a class="project-btn project-btn-ghost"
           href="{{ p.github_url }}"
           target="_blank"
           rel="noopener">GitHub</a>

        <a class="project-btn"
           href="{{ p.report_url | relative_url }}"
           target="_blank"
           rel="noopener">Read more</a>
      </div>
    </div>
  </div>
  {% endfor %}
</div>

