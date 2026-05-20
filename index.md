---
layout: page
title: "Moje tajné pískoviště | Vítejte"
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

      {% if prispevek.content contains '<h2' %}
        {% assign h2_casti = prispevek.content | split: '<h2' %}
        {% assign h2_konec = h2_casti[1] | split: '</h2>' %}
        {% assign ciste_h2 = h2_konec[0] | split: '>' | last %}
        
        <h4 class="karta-podnadpis" style="font-size: 1.0rem; font-weight: 600; margin-top: 4px; margin-bottom: 6px; color: #e0e0e0; opacity: 0.9;">
          {{ ciste_h2 | strip_html }}
        </h4>
      {% endif %}
      
      <p class="karta-anotace" style="margin-top: 4px;">
        {% if prispevek.content contains '<h2' %}
          {% assign text_za_nadpisem = prispevek.content | split: '</h2>' | last %}
          {{ text_za_nadpisem | strip_html | truncatewords: 12 }}
        {% else %}
          {{ prispevek.excerpt | strip_html | truncatewords: 12 }}
        {% endif %}
      </p>
      
    </div>
  {% endfor %}
</div>
