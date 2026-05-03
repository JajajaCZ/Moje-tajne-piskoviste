---
layout: page
title: "Moje Články"
permalink: /clanky/
---

## Seznam všech článků

<ul>
  {% for post in site.posts %}
    <li>
      <span style="color: #666;">{{ post.date | date: "%d.%m.%Y" }}</span> — 
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>