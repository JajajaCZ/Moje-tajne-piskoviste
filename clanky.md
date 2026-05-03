---
layout: default
title: "Moje Články"
permalink: /clanky/
---

<div class="post-grid">
  {% for clanek in site.clanky %}  <!-- Tady je ta změna! -->
    <div class="post-card">
      <div class="post-thumbnail">
        {% if clanek.thumbnail %}
          <img src="{{ clanek.thumbnail | relative_url }}" alt="{{ clanek.title }}">
        {% else %}
          <img src="{{ '/img/default-thumb.png' | relative_url }}" alt="default">
        {% endif %}
      </div>
      
      <div class="post-content">
        <!-- Pozor: u kolekcí se datum musí v hlavičce souboru psát explicitně -->
        <span class="post-date">{{ clanek.date | date: "%d.%m.%Y" }}</span>
        <h2><a href="{{ clanek.url | relative_url }}">{{ clanek.title }}</a></h2>
        <p>{{ clanek.content | strip_html | truncatewords: 20 }}</p>
        <a href="{{ clanek.url | relative_url }}" class="read-more">Číst dál →</a>
      </div>
    </div>
  {% endfor %}
</div>