---
layout: page
title: projects
permalink: /projects/
description: Work in progress. Much like the rest of AI governance.
nav: true
nav_order: 2
display_categories: [work]
horizontal: false
---

<div class="projects">
  {% assign sorted_projects = site.projects | sort: "importance" %}
  <div class="container py-3">
    <div class="row row-cols-1 row-cols-md-2 g-4">
      {% for project in sorted_projects %}
        <div class="col">
          <a href="{{ project.url | relative_url }}" class="text-decoration-none text-reset d-block">
            <div class="card h-100 hoverable shadow-sm border-0">
              {% if project.img %}
              <div style="height: 240px; overflow: hidden; border-top-left-radius: 0.375rem; border-top-right-radius: 0.375rem;">
                <img src="{{ project.img | relative_url }}" class="w-100 h-100" style="object-fit: cover;" alt="{{ project.title }}">
              </div>
              {% endif %}
              <div class="card-body p-4">
                <h3 class="card-title mb-2">{{ project.title }}</h3>
                <p class="card-text text-muted mb-3">{{ project.description }}</p>
                <span class="btn btn-sm btn-outline-primary">Read write-up &rarr;</span>
              </div>
            </div>
          </a>
        </div>
      {% endfor %}
    </div>
  </div>
</div>
