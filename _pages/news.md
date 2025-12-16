---
layout: page
title: News
permalink: /news/
nav: true
nav_order: 3
---

{% assign items = site.news | sort: "date" | reverse %}
{% for item in items %}
  <div style="margin-bottom: 1.5rem;">
    <div>
      <strong>{{ item.date | date: "%b %d, %Y" }}</strong>
    </div>
    <div>
      {{ item.content | markdownify }}
    </div>
  </div>
{% endfor %}