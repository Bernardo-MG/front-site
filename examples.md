---
layout: page
title: Examples
permalink: /examples/
---

<div>
   {%- for example in site.examples -%}
   <div class="card">
      <div class="card-body">
         <h5 class="card-title"><a href="{{ example.link }}">{{ example.title | escape }}</a></h5>
         {% if example.languages %}
         <h6 class="card-subtitle mb-2 text-muted">{{ example.languages }}</h6>
         {% endif %}
         {% if example.libraries %}
         <h6 class="card-subtitle mb-2 text-muted">{{ example.libraries }}</h6>
         {% endif %}
         <p class="card-text">{{ example.content }}</p>
      </div>
   </div>
   {%- endfor -%}
</div>