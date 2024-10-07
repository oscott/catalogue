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
        {% if page.date %}
          {% assign year = page.date | date: "%Y" %}       <!-- Get the full year -->
          {% assign month = page.date | date: "%b" %}      <!-- Get the abbreviated month -->
          {% assign day = page.date | date: "%d" %}        <!-- Get the day -->
          
          {% assign last_three_year = year | slice: 1, 3 %} <!-- Get the last three digits of the year -->
        <p class="date">{{ last_three_year }}</p>
          {% endif %}
      </div>
    </li>
  {% endfor %}
</ul>

<p><a href="{{ '/' | relative_url }}">..</a></p>
