---
layout: page
title: Home
id: home
permalink: /
---

# Welcome to my digital garden! 🌱
<p>
   <span style="font-weight: bold">Joe Hisaishi</span> One Summer's Day 
   <br>
      <audio controls>
    <source src="/assets/summerday.mp3" type="audio/mpeg">
    </audio>
</p>

When writer Iain Sinclair was asked if he did research for his books, he replied that his whole life was research. Inspired by that, I decided to create this digital garden as my way of collating all of that research - essentially, all that life. Some may call it a personal knowledge management system, but I find the term [[digital-garden|digital garden]]🪴 just a tad more endearing, don't you think?

My goal is to tend to this garden just like I would my actual garden. The notes you find here are never published, instead they are evergreen. In other words, I keep on adding bits and pieces to the notes as time goes by. Feel free to take a look around!  

<strong>Curated notes </strong>
Notes in essay formats, may be year-in-reviews, or more 
<ul> 
<li> [[research|How research builds the designer]] </li>
<li> [[Where I'm at, where I'm going]]</li>
<li> TBA for now! </li> </ul>


<strong>Site notes </strong>
My toolkit as of now consists of Obsidian, Github and Jekyll. This is pretty challenging for me considering I'm not from a technical background, but I'm having fun nerding out 🤓. I built this digital garden through an open-source and free template [available on GitHub here](https://github.com/maximevaillancourt/digital-garden-jekyll-template). 

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
