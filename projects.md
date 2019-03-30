---
layout: page
title: Projects
permalink: /projects/
---

{%- for project in site.projects -%}
   <h1>{{ project.title | escape }}</h1>
   <a class="post-link" href="{{ project.url | relative_url }}">
      {{ project.title | escape }}
   </a>
{%- endfor -%}
