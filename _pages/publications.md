---
layout: page
permalink: /publications/
title: Publications
years: [2025, 2024, 2023, Manuscript]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->

<style>
.post-header .post-title::after {
  content: " * denotes equal contribution";
  font-size: 0.85rem;
  color: var(--global-text-color-light);
  font-style: italic;
  font-weight: 400;
  margin-left: 1rem;
}

.publications * {
  font-family: 'Merriweather', Georgia, serif;
}

.publications .bibliography {
  margin-top: 2rem;
}

.publications .bibliography h2 {
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1rem;
  color: var(--global-text-color);
}

.publications .bibliography li {
  margin-bottom: 1rem;
  padding-bottom: 1rem;
  border-bottom: 1px solid var(--global-divider-color);
}

.publications .bibliography li:last-child {
  border-bottom: none;
}

.publications .title {
  font-weight: 600;
  font-size: 1.1rem;
  line-height: 1.4;
}

.publications .author {
  font-style: normal;
  margin-top: 0.3rem;
}

.publications .author em {
  font-weight: 600;
  font-style: normal;
  color: var(--global-theme-color);
}

.publications .periodical {
  margin-top: 0.3rem;
  font-style: italic;
  color: var(--global-text-color-light);
}

.publications .links a {
  display: inline-block;
  padding: 0.2rem 0.6rem;
  margin-right: 0.5rem;
  margin-top: 0.5rem;
  background: rgba(138, 43, 226, 0.08);
  color: var(--global-theme-color) !important;
  text-decoration: none !important;
  border: 1px solid rgba(138, 43, 226, 0.25);
  border-radius: 4px;
  font-size: 0.85rem;
  font-weight: 500;
  transition: all 0.3s ease;
}

.publications .links a:hover {
  background: rgba(138, 43, 226, 0.15);
  border-color: rgba(138, 43, 226, 0.4);
  transform: translateY(-1px);
}
</style>

<div class="publications">

{%- for y in page.years %}

  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}

</div>