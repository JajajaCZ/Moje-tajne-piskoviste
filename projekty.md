---
layout: page
title: "Projekty"
permalink: /projekty/
order: 2
---

# Moje rozpracované projekty

<ul class="post-list">
  {% for projekt in site.projekty %}
    <li>
      <span class="post-meta">{{ projekt.date | date: "%b %d, %Y" }}</span>
      <h3>
        <a class="post-link" href="{{ projekt.url | relative_url }}">
          {{ projekt.title }}
        </a>
      </h3>
    </li>
  {% endfor %}
</ul>