---
layout: default
title: People
permalink: /people/
---
<div class="page">
<p class="eyebrow">PEOPLE</p>
# Our Team
<div class="member-grid">
{% assign sorted_members = site.members | sort: 'order' %}
{% for member in sorted_members %}
  <a class="member-card" href="{{ member.url | relative_url }}">
    {% if member.photo %}
      <img class="member-avatar" src="{{ member.photo | relative_url }}" alt="{{ member.name }}">
    {% else %}
      <div class="member-avatar member-placeholder">{{ member.name | slice: 0 }}</div>
    {% endif %}
    <strong>{{ member.name }}</strong>
    <div class="member-role">{{ member.role }}</div>
  </a>
{% endfor %}
</div>
</div>
