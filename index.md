---
layout: home
title: Index
---

<div class="row justify-content-center">
   <h2>Check me on GitHub</h2>
</div>

<div class="row justify-content-center">
   <div class="github-card" data-github="bernardo-mg" data-width="400" data-height="" data-theme="default"></div>
</div>

<div class="row justify-content-center">
   <h2>Or check my projects</h2>
</div>

<div class="row justify-content-center">
{%- assign default_paths = site.pages | map: "path" -%}
{%- assign page_paths = site.header_pages | default: default_paths -%}
{%- for path in page_paths -%}
   {%- assign current_page = site.pages | where: "path", path | first -%}
   {%- if current_page.title -%}
   <a href="{{ current_page.url | relative_url }}" type="button" class="btn btn-primary">{{ current_page.title | escape }}</a>
   {% endif %}
{%- endfor -%}
</div>