---
layout: page
title: Languages
permalink: /languages/
---

<div>
   {%- assign projects = '' | split: '' -%}
   {%- for language in site.languages -%}
   {%- for project in site.projects -%}
      {%- if project.languages == language.name -%}
      {% assign projects = projects | push: project %}
      {%- endif -%}
   {%- endfor -%}
   {{ language }}
   <div id="#{{ language.name | slugize }}">
   <h2>{{ language.name }}</h2>
   {% include projects.html projects=projects %}
   </div>
   {%- endfor -%}
</div>
