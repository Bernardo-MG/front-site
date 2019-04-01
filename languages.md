---
layout: page
title: Languages
permalink: /languages/
---

<div>
   {%- assign languages = '' | split: '' -%}
   {% assign all_projects = site.projects | concat: site.examples %}
   {%- for project in all_projects -%}
      {%- for lang in project.languages -%}
         {% unless languages contains lang %}
            {% assign languages = languages | push: lang %}
         {% endunless %}
      {%- endfor -%}
   {%- endfor -%}
   {% assign languages = languages | sort %}
   {%- for language in languages -%}
   <div id="#{{ language | slugize }}">
   <h2>{{ language }}</h2>
   {%- assign projects = '' | split: '' -%}
   {%- for project in all_projects -%}
      {%- if project.languages contains language -%}
      {% assign projects = projects | push: project %}
      {%- endif -%}
   {%- endfor -%}
   {% include projects.html projects=projects %}
   </div>
   {%- endfor -%}
</div>
