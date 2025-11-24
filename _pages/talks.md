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
    .talks * {
      font-family: 'Merriweather', Georgia, serif;
      font-weight: 400;
    }
  
    .talks table.table-borderless {
      border: none !important;
    }

    .talks table.table-sm {
      font-size: 0.95rem !important;
    }
    
    .talks table tr {
      border-bottom: 1px solid var(--global-divider-color);
      transition: background-color 0.2s ease;
    }
    
    .talks table tr:last-child {
      border-bottom: none;
    }
    
    .talks table tr:hover {
      background-color: rgba(0, 0, 0, 0.02);
    }
    
  	.talks th {
    	font-weight: 600 !important;
    	color: var(--global-theme-color);
    	vertical-align: top;
    	padding: 1rem 0.5rem !important;
  	}
  	
  	.talks td {
  	  vertical-align: top;
  	  padding: 1rem 0.5rem !important;
  	}
  	
  	.talks th[scope="row"], .talks td:first-child {
    	width: 80px;
    	white-space: nowrap !important;
    	font-size: 0.9rem;
  	}
  	
  	.talks-title {
  	  font-weight: 600;
  	  font-size: 1.05rem;
  	  color: var(--global-text-color) !important;
  	  text-decoration: none !important;
  	}
  	
  	.talks-title:hover {
  	  color: var(--global-theme-color) !important;
  	}
  	
  	.talks-place {
  	  color: var(--global-text-color-light);
  	  font-size: 0.9rem;
  	  font-size: 0.85rem;
  	  white-space: nowrap;
  	}
  </style>

{% if site.talks != blank -%} 
<div class="table-responsive">
    <table class="table table-sm table-borderless">
    {%- assign talks = site.talks | reverse -%} 
    {% for item in talks %} 
    <tr>
        <th scope="row">  
        	{{ item.date | date: "%b %-d," }}<br>
  			{{ item.date | date: "%Y" }}
        </th>
        <td>
        {% if item.inline -%} 
            {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
        {%- else -%} 
            <a class="talks-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
        {%- endif %} 
        </td>
        <td>
        {% if item.place -%} 
            <span class="talks-place">{{ item.place }}</span>
        {%- endif %} 
        </td>
    </tr>
    {%- endfor %} 
    </table>
</div>
{%- else -%} 
<p>No talks so far...</p>
{%- endif %} 
</div>
