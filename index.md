---
layout: default
title: "Koept Catalogue"
---

# The catalogue

<ul>
  {% for item in site.catalog %}
    <li>
      <a href="{{ site.baseurl }}{{ item.url }}">{{ item.title }}</a> by {{ item.artist }} - {{ item.format }} 
      <br>
      <a href="{{ item.externalUrl }}">External Link</a>
    </li>
  {% endfor %}
</ul>
 
