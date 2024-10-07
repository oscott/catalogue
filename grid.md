---
layout: main
title: Grid View
---
<h1>Grid View</h1>
<!-- <ul class="item-grid">
  {% for item in site.catalog %}
    <li class="item">
      <div class="item-content">
        <h3>{{ item.title }}</h3>
        <p>{{ item.artist }}</p>
        <p>{{ item.format }}</p>
      </div>
    </li>
  {% endfor %}
</ul> -->

<ul class="item-grid">
  {% for item in site.catalog %}
    <li class="item" id="{{ item.id }}">
      <div class="item-content">
        <h3 class="title"><a href="{{ site.baseurl }}{{ item.url }}">{{ item.title }}</a></h3>
        <p class="artist">{{ item.artist }}</p>
        <p class="format">{{ item.format }}</p>
        <p class="catno">{{ item.catno }}.{{ item.date | date: "%Y" | slice: 1, 3 }}</p>
<!--         <p class="date">{{ item.date | date: "%Y" | slice: 1, 3 }}</p>
      </div> -->
    </li>
  {% endfor %}
</ul>

<p><a href="{{ '/' | relative_url }}">..</a></p>
