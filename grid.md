---
layout: main
title: Grid View
---
<h1>Grid View</h1>
<ul class="item-grid">
  {% for item in site.catalog %}
    <li class="item">
      <div class="item-content">
        <h3>{{ item.title }}</h3>
        <p>{{ item.artist }}</p>
        <p>{{ item.format }}</p>
      </div>
    </li>
  {% endfor %}
</ul>

<p><a href="{{ '/' | relative_url }}">..</a></p>
