---
layout: page
title: Projects
permalink: /projects/
---

{%- for project in site.projects -%}
<div class="card">
  <div class="card-body">
    <h5 class="card-title"><a href="{{ project.link }}">{{ project.title | escape }}</a></h5>
    {% if project.languages %}
    <h6 class="card-subtitle mb-2 text-muted">{{ project.languages }}</h6>
    {% endif %}
    {% if project.libraries %}
    <h6 class="card-subtitle mb-2 text-muted">{{ project.libraries }}</h6>
    {% endif %}
    <p class="card-text">{{ project.content }}</p>
    <a href="{{ project.link }}" class="btn btn-primary">Check the project</a>
  </div>
</div>
{%- endfor -%}