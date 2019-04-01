---
layout: page
title: Languages
permalink: /languages/
---

<div>
   {%- assign languages = '' | split: '' -%}
   {%- for project in site.projects -%}
      {%- for lang in project.languages -%}
         {% unless languages contains lang %}
            {% assign languages = languages | push: lang %}
         {% endunless %}
      {%- endfor -%}
   {%- endfor -%}
   {%- for example in site.examples -%}
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
   </div>
   {%- endfor -%}
</div>
