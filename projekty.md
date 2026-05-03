---
layout: default
title: "Projekty"
permalink: /projekty/
---

<div class="post-grid">
  {% for clanek in site.projekty %}
    <a href="{{ clanek.url | relative_url }}" class="post-card" style="background-image: url('{{ clanek.thumbnail | relative_url }}');">
      <div class="post-overlay">
        <div class="post-content">
          <span class="post-date">{{ clanek.date | date: "%d.%m.%Y" }}</span>
          <h2>{{ clanek.title }}</h2>
          <p>{{ clanek.content | strip_html | truncate: 100 }}</p>
          <span class="read-more">Zobrazit kartu →</span>
        </div>
      </div>
    </a>
  {% endfor %}
</div>
</div>