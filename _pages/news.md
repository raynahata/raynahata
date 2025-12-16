---
layout: page
title: News
permalink: /news/
nav: true
nav_order: 3
---

<ul>
  {% assign items = site.news | sort: "date" | reverse %}
  {% for item in items %}
    <li>
      <strong>{{ item.date | date: "%b %d, %Y" }}</strong>:
      {{ item.title }}
    </li>
  {% endfor %}
</ul>