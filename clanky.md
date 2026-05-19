---
layout: page
title: Články
permalink: /clanky/
order: 1
---
# Všechny články

Tady najdeš moje zápisky, úvahy a postřehy z pískoviště.

<ul class="post-list">
  {% assign seřazené_clanky = site.clanky | sort: "date" | reverse %}
  {% for clanek in seřazené_clanky %}
    <li>
      <span class="post-meta">{{ clanek.date | date: "%b %d, %Y" }}</span>
      <h3>
        <a class="post-link" href="{{ clanek.url | relative_url }}">
          {{ clanek.title }}
        </a>
      </h3>
      <p>{{ clanek.excerpt }}</p>
    </li>
  {% endfor %}
</ul>