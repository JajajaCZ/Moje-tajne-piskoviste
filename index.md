---
layout: home
title: Domovská stránka
---

# Ahoj, objevil jsi moje tajné pískoviště

Vem si lopatičku a pojď s podívat, s čím si tu hraju

{% assign vsechny_prispevky = site.clanky | concat: site.projekty | sort: "date" | reverse %}

<h2 class="post-listing-heading">Nejnovější příspěvky (Články & Projekty)</h2>

<ul class="post-list">
  {% for prispevek in vsechny_prispevky %}
    <li>
      <span class="post-meta">
        {{ prispevek.date | date: "%b %d, %Y" }} 
        • 
        {% if prispevek.collection == "projekty" %} 🛠️ Projekt {% else %} 📝 Článek {% endif %}
      </span>
      <h3>
        <a class="post-link" href="{{ prispevek.url | relative_url }}">
          {{ prispevek.title }}
        </a>
      </h3>
      <p>{{ prispevek.excerpt }}</p>
    </li>
  {% endfor %}
</ul>