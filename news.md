---
layout: default
title: News
permalink: /news/
---
<div class="page">
<p class="eyebrow">NEWS</p>
# Lab News
<div class="news-grid">
{% assign sorted_news = site.news | sort: 'date' | reverse %}
{% for post in sorted_news %}
  <a class="news-card" href="{{ post.url | relative_url }}">
    <div class="news-date">{{ post.date | date: "%Y.%m.%d" }}</div>
    <h3>{{ post.title }}</h3>
    <div class="muted">{{ post.excerpt | strip_html | truncatewords: 24 }}</div>
  </a>
{% endfor %}
</div>
</div>
