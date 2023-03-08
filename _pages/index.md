---
layout: page
title: Home
id: home
permalink: /
---

# Welcome to my digital garden! 🌱

Hello, my name is [Jovina](https://jovina.online/about), UI/UX and graphic designer. 

When writer Iain Sinclair was asked if he did research for his books, he replied that his whole life was research. This digital garden is my way of collating all of that research - essentially, all that life. 


I built this digital garden through an open-source and free template [available on GitHub here](https://github.com/maximevaillancourt/digital-garden-jekyll-template) 

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes | limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
