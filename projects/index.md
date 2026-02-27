---
layout: page
title: Projects
permalink: /projects/
---

<div class="projects-list">
  {% assign sorted = site.projects | sort: "year" | reverse %}
  {% for project in sorted %}
    <article class="project-card">
      <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
      <p class="subtitle">
        {% if project.year %}{{ project.year }}{% endif %}
        {% if project.authors %} • {{ project.authors | map: "name" | join: ", " }}{% endif %}
      </p>
      <p class="excerpt">{{ project.abstract | strip_html | truncate: 220 }}</p>
    </article>
  {% endfor %}
</div>
