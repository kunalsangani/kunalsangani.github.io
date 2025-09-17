---
layout: default
permalink: /files/teaching/
nav_exclude: true
hidden: true
exclude: true
---

<h1>Teaching Slides</h1>

<!-- <ul>
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
</ul> -->

<table>
  <thead><tr><th>File</th><th>Last Modified</th></tr></thead>
  <tbody>
  {% for f in teaching_files %}
    {% unless f.name == 'index.html' or f.name == 'index.md' %}
      <tr>
        <td><a href="{{ f.path | relative_url }}">{{ f.name }}</a></td>
        <td>{{ f.modified_time | date: "%Y-%m-%d" }}</td>
      </tr>
    {% endunless %}
  {% endfor %}
  </tbody>
</table>