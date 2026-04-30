---
layout: page
permalink: /blog/
title: Blog
nav: false
nav_order: 99
---

<div class="post-list">
  {% for post in site.posts %}
  <div style="margin-bottom: 2rem;">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p style="color: rgba(0, 50, 98, 0.55); font-size: 0.9rem;">{{ post.date | date: "%B %-d, %Y" }}</p>
    {% if post.description %}
    <p>{{ post.description }}</p>
    {% endif %}
  </div>
  {% endfor %}
</div>
