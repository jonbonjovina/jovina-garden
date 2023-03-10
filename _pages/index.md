---
layout: page
title: Home
id: home
permalink: /
---

# Welcome to my digital garden! 🌱

Hello, my name is [Jovina](https://jovina.online/about), UI/UX and graphic designer. 

When writer Iain Sinclair was asked if he did research for his books, he replied that his whole life was research. Inspired by that, I decided to create this digital garden as my way of collating all of that research - essentially, all that life. Some may call it a personal knowledge management system, but I find the term digital garden 🪴 just a tad more endearing, don't you think?

My goal is to tend to this garden just like I would my actual garden. The notes you find here are never published, instead they are evergreen. I keep on adding things bits and pieces as time goes by. 

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
