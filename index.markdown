---
layout: default
title: Home
---

# Welcome to {{ site.title }}

This is my personal blog where I write letters to myself. 🌿

## Recent Posts

<ul>
  {% for post in site.posts limit:5 %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%b %-d, %Y" }}</li>
  {% endfor %}
</ul>

## Recent books
<ul>
    {% for note in site.booknotes limit:5 %}
    <li><a href="{{ note.url | relative_url }}">{{ note.title }}</a> - {{ note.date | date: "%b %-d, %Y" }}</li>
  {% endfor %}
</ul>