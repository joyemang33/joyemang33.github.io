---
layout: page
permalink: /publications/
title: Publications
years: [2026, 2025, 2024, 2023, Manuscript]
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
  padding-bottom: 0;
  border-bottom: none;
}

.publications .bibliography li:last-child {
  border-bottom: none;
}

.publications .bibliography h2 {
  font-size: 1.75rem;
  font-weight: 700;
  margin-top: 2rem;
  margin-bottom: 1rem;
  color: var(--global-text-color);
  padding-top: 1.5rem;
  border-top: 2px solid var(--global-divider-color);
}

.publications .bibliography h2:first-of-type {
  margin-top: 0;
  padding-top: 0;
  border-top: none;
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

.filter-buttons {
  margin: 1.5rem 0;
  display: flex;
  gap: 0.8rem;
}

.filter-btn {
  padding: 0.4rem 1rem;
  border: 1px solid var(--global-theme-color);
  background: transparent;
  color: var(--global-theme-color);
  border-radius: 4px;
  cursor: pointer;
  font-size: 0.9rem;
  font-family: 'Merriweather', Georgia, serif;
  transition: all 0.3s ease;
}

.filter-btn:hover {
  background: rgba(138, 43, 226, 0.1);
}

.filter-btn.active {
  background: var(--global-theme-color);
  color: white;
}
</style>

<div class="publications">

<div class="filter-buttons">
  <button class="filter-btn" onclick="filterPublications('all')">All Publications</button>
  <button class="filter-btn active" onclick="filterPublications('first-author')">First & Co-first Author</button>
</div>

<script>
// Run filter on page load with a small delay to ensure bibliography is rendered
window.addEventListener('load', function() {
  setTimeout(function() {
    filterPublications('first-author');
  }, 100);
});

function filterPublications(type) {
  // Update button states
  document.querySelectorAll('.filter-btn').forEach(btn => {
    btn.classList.remove('active');
  });
  
  // Find and activate the correct button
  if (type === 'all') {
    document.querySelector('.filter-btn[onclick*="all"]').classList.add('active');
  } else if (type === 'first-author') {
    document.querySelector('.filter-btn[onclick*="first-author"]').classList.add('active');
  }
  
  // Get all bibliography items
  const items = document.querySelectorAll('.bibliography li');
  
  items.forEach(item => {
    if (type === 'all') {
      item.style.display = '';
    } else if (type === 'first-author') {
      const authorText = item.querySelector('.author')?.textContent || '';
      // Check if Qiuyang Mang is first author OR has * (co-first) anywhere
      const isFirstAuthor = authorText.match(/^[^,]*Qiuyang Mang(\*)?[,\s]/);
      const isCoFirst = authorText.includes('Qiuyang Mang*');
      
      if (isFirstAuthor || isCoFirst) {
        item.style.display = '';
      } else {
        item.style.display = 'none';
      }
    }
  });
  
  // Handle 2023 section specially (no first-author papers)
  const year2023Section = document.querySelector('.year-2023-section');
  if (year2023Section) {
    if (type === 'first-author') {
      year2023Section.style.display = 'none';
    } else {
      year2023Section.style.display = '';
    }
  }
  
  // Hide empty year sections for other years
  const years = [2026, 2025, 2024, 'Manuscript'];
  
  years.forEach(year => {
    // Find the year header
    const yearHeaders = document.querySelectorAll('.bibliography h2, .bibliography h2.year');
    let yearHeader = null;
    
    for (let h2 of yearHeaders) {
      if (h2.textContent.trim() == year.toString()) {
        yearHeader = h2;
        break;
      }
    }
    
    if (!yearHeader) return;
    
    // Show all years when type is 'all'
    if (type === 'all') {
      yearHeader.style.display = '';
      // Show all following lists
      let sibling = yearHeader.nextElementSibling;
      while (sibling && sibling.tagName !== 'H2') {
        if (sibling.tagName === 'OL' || sibling.tagName === 'UL') {
          sibling.style.display = '';
        }
        sibling = sibling.nextElementSibling;
      }
      return;
    }
    
    // For other years in first-author filter, check if there are visible items
    let hasVisibleItems = false;
    let sibling = yearHeader.nextElementSibling;
    
    while (sibling && sibling.tagName !== 'H2') {
      if (sibling.tagName === 'OL' || sibling.tagName === 'UL') {
        const listItems = sibling.querySelectorAll('li');
        for (let item of listItems) {
          if (item.style.display !== 'none') {
            hasVisibleItems = true;
            break;
          }
        }
        if (hasVisibleItems) break;
      }
      sibling = sibling.nextElementSibling;
    }
    
    yearHeader.style.display = hasVisibleItems ? '' : 'none';
  });
}
</script>

{%- for y in page.years %}
  {% if y == 2023 %}
  <div class="year-2023-section">
    {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
  </div>
  {% elsif y == 2026 %}
  <div class="year-2026-section">
    {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
  </div>
  {% else %}
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
  {% endif %}
{% endfor %}

</div>