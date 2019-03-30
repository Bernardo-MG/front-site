---
layout: page
title: Projects
permalink: /projects/
---

{%- for project in site.projects -%}
<div class="card">
  <div class="card-body">
    <h5 class="card-title">{{ project.title | escape }}</h5>
    <p class="card-text">{{ project.content }}</p>
    <a href="{{ project.link }}" class="btn btn-primary">Check the project</a>
  </div>
</div>
{%- endfor -%}