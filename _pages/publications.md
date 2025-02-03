---
layout: page
permalink: /publications/
title: Publications
years: [2025, 2024, 2023, Manuscript]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->

<div class="publications">

{%- for y in page.years %}

  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}

</div>