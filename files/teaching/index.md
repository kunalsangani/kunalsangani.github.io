---
layout: default
title: Teaching Slides
permalink: /files/teaching/
---

<h1>Teaching Slides</h1>

<ul>
  {% assign teaching_files = site.static_files
     | where_exp: "f", "f.path contains '/files/teaching/'" 
     | sort: "name" %}
  {% for f in teaching_files %}
    {% unless f.name == 'index.html' or f.name == 'index.md' %}
      <li>
        <a href="{{ f.path | relative_url }}">{{ f.name }}</a>
      </li>
    {% endunless %}
  {% endfor %}
</ul>