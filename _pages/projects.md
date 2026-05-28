---
layout: page
title: projects
permalink: /projects/
description: Selected course and research-related projects.
nav: true
nav_order: 3
horizontal: true
---

{% include lang-switch.liquid en='/projects/' zh='/zh/projects/' current='en' %}

<div class="projects">
{% assign sorted_projects = site.projects | sort: "importance" %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
</div>

