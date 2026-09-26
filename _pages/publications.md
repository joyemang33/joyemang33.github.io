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
  display: grid;
  grid-template-columns: 4.75rem minmax(0, 1fr);
  column-gap: 1.625rem;
  row-gap: 2.25rem;
  font-family: 'Merriweather', Georgia, serif;
}

.publications h2.bibliography {
  grid-column: 1;
  display: flex;
  align-items: center;
  gap: 0.65rem;
  align-self: start;
  margin: 0;
  padding-top: 0.85rem;
  font-size: 1rem;
  font-weight: 600;
  line-height: 1.3;
  color: #003262;
}

.publications h2.bibliography::after {
  content: '';
  width: 1.5rem;
  border-top: 1px solid rgba(0, 50, 98, 0.13);
}

.publications ol.bibliography {
  grid-column: 2;
  min-width: 0;
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
  grid-template-columns: minmax(0, 1fr) auto;
  grid-template-areas:
    'title venue'
    'author author'
    'links links'
    'venue-full venue-full';
  column-gap: 1.5rem;
  padding: 0.8rem 0 0.9rem;
  border-top: 1px solid rgba(0, 50, 98, 0.10);
}

.publications ol.bibliography li:first-child .pub-item {
  border-top-color: rgba(0, 50, 98, 0.13);
}

.pub-title-line {
  grid-area: title;
  min-width: 0;
  line-height: 1.5;
}

.pub-title {
  position: relative;
  display: block;
  padding-left: 0.95rem;
  font-weight: 600;
  font-size: 1rem;
  color: var(--global-text-color);
  text-decoration: none;
}

.pub-title::before {
  content: '';
  position: absolute;
  top: 0.75em;
  left: 0;
  width: 0.42rem;
  height: 0.42rem;
  transform: translateY(-50%);
  border-radius: 50%;
  background: #9bafc1;
}

.pub-item-highlighted .pub-title::before {
  background: #c0266d;
}

a.pub-title:hover {
  text-decoration: underline;
}

.pub-meta {
  display: contents;
}

.pub-links {
  grid-area: links;
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  gap: 0;
  min-width: 0;
  margin: 0.28rem 0 0 0.95rem;
  line-height: 1.45;
}

.pub-links .pub-link-sep {
  display: inline;
  flex: 0 0 auto;
  margin: 0 0.35rem;
}

.pub-author {
  grid-area: author;
  min-width: 0;
  margin: 0.08rem 0 0 0.95rem;
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
  grid-area: venue;
  align-self: start;
  display: inline-block;
  padding-top: 0.05rem;
  font-weight: 600;
  font-size: inherit;
  font-style: normal;
  color: #003262;
  line-height: 1.5;
  text-align: right;
  white-space: nowrap;
}

.pub-venue-full {
  grid-area: venue-full;
  min-width: 0;
  margin: 0.18rem 0 0 0.95rem;
  font-size: inherit;
  color: #3b6487;
  line-height: 1.45;
}

.pub-link {
  color: #003262;
  text-decoration: none;
  cursor: pointer;
  font-size: inherit;
  font-weight: 600;
}

.pub-link:hover {
  color: var(--global-text-color);
  text-decoration: underline;
  text-underline-offset: 2px;
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

@media (max-width: 700px) {
  .publications {
    grid-template-columns: minmax(0, 1fr);
    row-gap: 0;
  }

  .publications h2.bibliography {
    grid-column: 1;
    margin: 1.5rem 0 0.45rem;
    padding-top: 0;
  }

  .publications h2.bibliography:first-child {
    margin-top: 0;
  }

  .publications h2.bibliography::after {
    width: 2.25rem;
  }

  .publications ol.bibliography {
    grid-column: 1;
  }

  .pub-item {
    grid-template-columns: minmax(0, 1fr);
    grid-template-areas:
      'title'
      'venue'
      'author'
      'links'
      'venue-full';
    padding: 0.8rem 0;
  }

  .pub-venue-tag {
    margin: 0.08rem 0 0 0.95rem;
    padding-top: 0;
    text-align: left;
  }
}
</style>

<div class="publications">

{%- for y in page.years %}
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}

</div>
