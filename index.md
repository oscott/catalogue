---
layout: default
title: "Koept Catalogue"
---

# The catalogue

<ul>
  {% for item in site.catalog %}
    <li>
      <a href="{{ site.baseurl }}{{ item.url }}">{{ item.title }}</a> by {{ item.artist }} - {{ item.format }} from {{ item.date | date: "%Y" | slice: 1, 3 }}
    </li>
  {% endfor %}
</ul>
 
