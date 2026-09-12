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
.publications {
  font-family: 'Merriweather', Georgia, serif;
}

.publications h2.bibliography {
  display: flex;
  align-items: center;
  gap: 0.65rem;
  margin: 1.8rem 0 0.45rem;
  font-size: 1rem;
  font-weight: 600;
  line-height: 1.3;
}

.publications h2.bibliography:first-child {
  margin-top: 0;
}

.publications h2.bibliography::after {
  content: '';
  width: 2.6rem;
  border-top: 1px solid rgba(0, 50, 98, 0.13);
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

.pub-item {
  display: grid;
  grid-template-columns: minmax(0, 1fr) 12.5rem;
  grid-template-areas:
    'title meta'
    'author meta'
    'venue-full meta';
  column-gap: 1.75rem;
  padding: 0.85rem 0;
  border-top: 1px solid rgba(0, 50, 98, 0.10);
}

.publications ol.bibliography li:first-child .pub-item {
  border-top-color: transparent;
}

.pub-title-line {
  grid-area: title;
  min-width: 0;
  line-height: 1.5;
}

.pub-title {
  font-weight: 600;
  font-size: 1rem;
  color: var(--global-text-color);
  text-decoration: none;
}

.pub-title::before {
  content: '';
  display: inline-block;
  width: 0.42rem;
  height: 0.42rem;
  margin: 0 0.52rem 0.08rem 0;
  border-radius: 50%;
  background: #9bafc1;
}

.pub-item-highlighted .pub-title::before {
  background: #c69214;
}

a.pub-title:hover {
  text-decoration: underline;
}

.pub-meta {
  grid-area: meta;
  align-self: start;
  min-width: 0;
  padding-top: 0.05rem;
  text-align: right;
  line-height: 1.55;
}

.pub-links {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-end;
  gap: 0 0.45rem;
}

.pub-links .pub-link-sep {
  display: none;
}

.pub-author {
  grid-area: author;
  min-width: 0;
  margin-top: 0.08rem;
  font-size: inherit;
  color: var(--global-text-color-light);
  line-height: 1.5;
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
  display: block;
  font-weight: 600;
  font-size: inherit;
  font-style: italic;
  color: #003262;
}

.pub-venue-full {
  grid-area: venue-full;
  min-width: 0;
  margin-top: 0.08rem;
  font-size: inherit;
  color: #3b6487;
  line-height: 1.45;
}

.pub-link {
  color: var(--global-text-color-light);
  text-decoration: underline;
  cursor: pointer;
  font-size: inherit;
  font-weight: 600;
}

.pub-link:hover {
  color: var(--global-text-color);
}

.pub-link-sep,
.pub-sep {
  color: var(--global-text-color-light);
  opacity: 0.5;
}

/* Hidden blocks (abstract, bibtex) */
.pub-item .hidden {
  grid-column: 1 / -1;
  font-size: 0.875rem;
  max-height: 0;
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

@media (max-width: 575px) {
  .publications h2.bibliography {
    margin-top: 1.5rem;
  }

  .pub-item {
    grid-template-columns: minmax(0, 1fr);
    grid-template-areas:
      'title'
      'meta'
      'author'
      'venue-full';
    padding: 0.8rem 0;
  }

  .pub-meta {
    margin-top: 0.08rem;
    padding-top: 0;
    text-align: left;
  }

  .pub-venue-tag,
  .pub-links {
    display: inline;
  }

  .pub-links {
    display: inline-flex;
    justify-content: flex-start;
  }

  .pub-links::before {
    content: ' \00b7 ';
    color: var(--global-text-color-light);
    opacity: 0.5;
  }
}
</style>

<div class="publications">

{%- for y in page.years %}
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}

</div>
