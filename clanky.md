---
layout: page
title: "Články"
permalink: /clanky/
order: 1
---

<div class="piskoviste-grid">
  {% for clanek in site.clanky %}
    <div class="piskoviste-karta karta-clanek">
      <div class="karta-meta">
        <span class="karta-datum">{{ clanek.date | date: "%d. %m. %Y" }}</span>
        <span class="karta-tag">📝 Článek</span>
      </div>
      
      <h3 class="karta-nadpis">
        <a class="karta-link" href="{{ clanek.url | relative_url }}">
          {{ clanek.title }}
        </a>
      </h3>
      
      <p class="karta-anotace">{{ clanek.excerpt | strip_html | truncatewords: 12 }}</p>
    </div>
  {% endfor %}
</div>