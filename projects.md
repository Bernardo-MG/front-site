---
layout: page
title: Projects
permalink: /projects/
---

{%- for project in site.projects -%}
   <a class="post-link" href="{{ project.url | relative_url }}">
      {{ project.title | escape }}
   </a>
{%- endfor -%}
