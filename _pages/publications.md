---
layout: page
permalink: /publications/
title: Publications
years: [2026, 2025, 2024, 2023]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->

<style>
.pub-item {
  font-family: 'Merriweather', Georgia, serif;
}

/* Hide year headers and list chrome */
.publications h2.bibliography {
  display: none !important;
}

.publications ol.bibliography {
  list-style: none;
  padding: 0;
  margin: 0;
}

.publications ol.bibliography li {
  margin: 0;
  padding: 0;
  border: none;
}

/* Publication items */
.pub-item {
  margin-bottom: 1.25rem;
}

.pub-item-highlighted {
  background: rgba(0, 50, 98, 0.055);
  padding: 0.65rem 0.85rem;
  border-radius: 4px;
}

.pub-title-line {
  line-height: 1.5;
}

.pub-title {
  font-weight: 600;
  font-size: 0.92rem;
  color: var(--global-text-color);
  text-decoration: none;
}

a.pub-title:hover {
  text-decoration: underline;
}

.pub-author {
  font-size: 0.88rem;
  color: var(--global-text-color-light);
  line-height: 1.5;
  margin-top: 0.1rem;
}

.pub-author a {
  color: var(--global-text-color-light);
  text-decoration: none;
}

.pub-author a:hover {
  color: var(--global-text-color);
}

.pub-author strong {
  color: var(--global-text-color);
  font-weight: 600;
}

.pub-author .more-authors {
  color: var(--global-text-color-light);
  border-bottom: 1px dashed var(--global-text-color-light);
  cursor: pointer;
}

.pub-author .more-authors:hover {
  color: var(--global-text-color);
  border-bottom-color: var(--global-text-color);
}

.pub-venue-tag {
  font-weight: 600;
  font-size: 0.88rem;
  font-style: italic;
  color: #003262;
}

.pub-link {
  color: var(--global-text-color-light);
  text-decoration: underline;
  cursor: pointer;
  font-size: 0.88rem;
  font-weight: 600;
}

.pub-link:hover {
  color: var(--global-text-color);
}

.pub-link-sep, .pub-sep {
  color: var(--global-text-color-light);
  opacity: 0.5;
}

/* Hidden blocks (abstract, bibtex) */
.pub-item .hidden {
  font-size: 0.875rem;
  max-height: 0px;
  overflow: hidden;
  transition: all 0.15s ease;
  margin-top: 0;
}

.pub-item .hidden.open {
  max-height: 100em;
  transition: all 0.15s ease;
  margin-top: 0.5rem;
}

.pub-item div.abstract.hidden {
  border: dashed 1px var(--global-bg-color);
}

.pub-item div.abstract.hidden.open {
  border-color: var(--global-text-color);
}

.pub-item .hidden p {
  line-height: 1.4em;
  margin: 10px;
}

.pub-item .hidden pre {
  font-size: 1em;
  line-height: 1.4em;
  padding: 10px;
}

</style>

<div class="publications">

{%- for y in page.years %}
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}

</div>
