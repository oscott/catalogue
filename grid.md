---
layout: main
title: Grid View
---
<h1>Grid View</h1>
{% assign sorted_items = site.catalog | sort: 'id' | reverse %}
<ul class="item-grid">
  {% for item in sorted_items %}
    <li class="item" id="{{ item.id }}">
      <div class="item-content">
        <h3 class="title"><a href="{{ site.baseurl }}{{ item.url }}">{{ item.title }}</a></h3>
        <p class="artist">{{ item.artist }}</p>
        <p class="format">{{ item.format }}</p>
        <p class="dataz"><span class="catno">{{ item.catno }}<span class="date">.{{ item.date | date: "%Y" | slice: 1, 3 }}</p>
      </div>
    </li>
  {% endfor %}
</ul>

<p><a href="{{ '/' | relative_url }}">..</a></p>
