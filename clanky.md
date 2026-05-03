---
layout: default
title: "Moje Články"
permalink: /clanky/
---

## Seznam všech článků

<div class="post-grid">
  {% for post in site.posts %}
    <div class="post-card">
      <div class="post-thumbnail">
        {% if post.thumbnail %}
          <img src="{{ post.thumbnail | relative_url }}" alt="{{ post.title }}">
        {% else %}
          <img src="{{ '/img/default-thumb.png' | relative_url }}" alt="default">
        {% endif %}
      </div>
      
      <div class="post-content">
        <span class="post-date">{{ post.date | date: "%d.%m.%Y" }}</span>
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p>{{ post.content | strip_html | truncatewords: 20 }}</p>
        <a href="{{ post.url | relative_url }}" class="read-more">Číst dál →</a>
      </div>
    </div>
  {% endfor %}
</div>