---
layout: page
title: "Domů"
permalink: /
---

# Vítejte na mém pískovišti

{% assign vsechny_prispevky = site.clanky | concat: site.projekty | sort: "date" | reverse %}

<h2 class="post-listing-heading">Nejnovější příspěvky</h2>

<div class="piskoviste-grid">
  {% for prispevek in vsechny_prispevky limit: 6 %}
    <div class="piskoviste-karta {% if prispevek.collection == 'projekty' %}karta-projekt{% else %}karta-clanek{% endif %}">
      <div class="karta-meta">
        <span class="karta-datum">{{ prispevek.date | date: "%d. %m. %Y" }}</span>
        <span class="karta-tag">
          {% if prispevek.collection == "projekty" %}🛠️ Projekt{% else %}📝 Článek{% endif %}
        </span>
      </div>
      
      <h3 class="karta-nadpis">
        <a class="karta-link" href="{{ prispevek.url | relative_url }}">
          {{ prispevek.title }}
        </a>
      </h3>
      
      <p class="karta-anotace">{{ prispevek.excerpt | strip_html | truncatewords: 12 }}</p>
    </div>
  {% endfor %}
</div>