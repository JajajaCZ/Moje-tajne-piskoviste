---
layout: home
title: Domovská stránka
---

# Ahoj, objevil jsi moje tajné pískoviště

Vem si lopatičku a pojď s podívat, s čím si tu hraju

{% assign vsechny_prispevky = site.clanky | concat: site.projekty | sort: "date" | reverse %}

<h2 class="post-listing-heading">Nejnovější příspěvky</h2>

<div class="piskoviste-grid">
  {% for prispevek in vsechny_prispevky limit: 6 %}
    <div class="piskoviste-karta {% if prispevek.collection == 'projekty' %}karta-projekt{% else %}karta-clanek{% endif %}">
      <div class="karta-meta">
        {{ prispevek.date | date: "%d. %m. %Y" }}
        <span class="karta-tag">
          {% if prispevek.collection == "projekty" %}🛠️ Projekt{% else %}📝 Článek{% endif %}
        </span>
      </div>
      
      <h3>
        <a class="karta-link" href="{{ prispevek.url | relative_url }}">
          {{ prispevek.title }}
        </a>
      </h3>
      
      <p class="karta-anotace">{{ prispevek.excerpt | strip_html | truncatewords: 15 }}</p>
    </div>
  {% endfor %}
</div>