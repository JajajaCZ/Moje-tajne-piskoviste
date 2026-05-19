---
layout: page
title: "Články"
permalink: /clanky/
order: 1
---

# Všechny články

<ul class="post-list">
  {% for clanek in site.clanky %}
    <li>
      <span class="post-meta">{{ clanek.date | date: "%b %d, %Y" }}</span>
      <h3>
        <a class="post-link" href="{{ clanek.url | relative_url }}">
          {{ clanek.title }}
        </a>
      </h3>
    </li>
  {% endfor %}
</ul>