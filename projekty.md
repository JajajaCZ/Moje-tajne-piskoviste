---
layout: page
title: Projekty
permalink: /projekty/
order: 2
---
#Projekty

Tady se můžeš podívat, na jakých bábovičkách zrovna pracuju

<ul class="post-list">
  {% assign seřazené_projekty = site.projekty | sort: "date" | reverse %}
  {% for projekt in seřazené_projekty %}
    <li>
      <span class="post-meta">{{ projekt.date | date: "%b %d, %Y" }}</span>
      <h3>
        <a class="post-link" href="{{ projekt.url | relative_url }}">
          {{ projekt.title }}
        </a>
      </h3>
      <p>{{ projekt.excerpt }}</p>
    </li>
  {% endfor %}
</ul>