---
layout: page
permalink: /talks/
title: Talks
description: 
nav: true
nav_order: 4
---

<!-- pages/talks.md -->
<div class="talks">
  <style>
    .talks {
      width: 100%;
    }

    .talk-list {
      list-style: none;
      padding: 0;
      margin: 0;
      width: 100%;
      font-family: 'Merriweather', Georgia, serif;
    }

    .talk-item {
      margin-bottom: 1.25rem;
    }

    .talk-content {
      font-size: 0.95rem;
      line-height: 1.5;
      color: var(--global-text-color);
    }

    .talk-content a {
      color: var(--global-text-color);
      text-decoration: none;
    }

    .talk-content a:hover {
      color: var(--global-text-color-light);
    }

    .talk-content em {
      color: var(--global-theme-color);
      font-style: normal;
      text-decoration: underline;
      text-decoration-color: #722F37;
    }

    .talk-meta {
      font-size: 0.83rem;
      color: var(--global-text-color-light);
      margin-top: 0.1rem;
    }
  </style>

{% if site.talks != blank -%}
<ul class="talk-list">
  {%- assign talks = site.talks | reverse -%}
  {% for item in talks %}
  <li class="talk-item">
    <div class="talk-content">
    {% if item.inline -%}
      {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
    {%- else -%}
      <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
    {%- endif %}
    </div>
    <div class="talk-meta">
      {{ item.date | date: "%b %-d, %Y" }}{% if item.place %} · {{ item.place }}{% endif %}{% if item.hoster %} · Hosted by {{ item.hoster | markdownify | remove: '<p>' | remove: '</p>' }}{% endif %}{% if item.related %} · Related: {{ item.related | markdownify | remove: '<p>' | remove: '</p>' }}{% endif %}{% if item.slides %} · <a href="{{ item.slides | relative_url }}">[slides]</a>{% endif %}
    </div>
  </li>
  {%- endfor %}
</ul>
{%- else -%}
<p>No talks so far...</p>
{%- endif %}
</div>
