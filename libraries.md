---
layout: page
title: Libraries
permalink: /libraries/
---

<div>
   {%- assign libraries = '' | split: '' -%}
   {% assign all_projects = site.projects | concat: site.examples %}
   {%- for project in all_projects -%}
      {%- for fram in project.libraries -%}
         {% unless libraries contains fram %}
            {% assign libraries = libraries | push: fram %}
         {% endunless %}
      {%- endfor -%}
   {%- endfor -%}
   {% assign libraries = libraries | sort %}
   {%- for library in libraries -%}
   <section id="{{ library | downcase | slugize }}">
      <h2>{{ library }}</h2>
      {%- assign projects = '' | split: '' -%}
      {%- for project in all_projects -%}
         {%- if project.libraries contains library -%}
         {% assign projects = projects | push: project %}
         {%- endif -%}
      {%- endfor -%}
      {% include projects.html projects=projects %}
   </section>
   {%- endfor -%}
</div>
