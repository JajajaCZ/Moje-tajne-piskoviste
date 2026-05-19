---
layout: page
title: "Projekty"
permalink: /projekty/
order: 2
---

# Moje projekty

<div class="piskoviste-grid">
  {% for projekt in site.projekty %}
    <div class="piskoviste-karta karta-projekt">
      <div class="karta-meta">
        <span class="karta-datum">{{ projekt.date | date: "%d. %m. %Y" }}</span>
        <span class="karta-tag">🛠️ Projekt</span>
      </div>
      
      <h3 class="karta-nadpis">
        <a class="karta-link" href="{{ projekt.url | relative_url }}">
          {{ projekt.title }}
        </a>
      </h3>
      
      <p class="karta-anotace">{{ projekt.excerpt | strip_html | truncatewords: 12 }}</p>
    </div>
  {% endfor %}
</div>