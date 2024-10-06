---
layout: main
title: "Koept Catalogue"
---

# The catalogue
{% assign sorted_items = site.catalog | sort: 'date' | reverse %}
<ul>
  {% for item in sorted_items %}
    <li>
      <a href="{{ site.baseurl }}{{ item.url }}">{{ item.title }}</a> by {{ item.artist }} - {{ item.format }} from {{ item.date | date: "%Y" | slice: 1, 3 }}
    </li>
  {% endfor %}
</ul>
 
<p class="hide"><a href="{{ '/grid' | relative_url }}">■ ■ ■ ■</a></p>
