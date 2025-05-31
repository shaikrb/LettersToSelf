---
layout: default
title: Blog
---

# Blog Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>({{ post.date | date: "%b %-d, %Y" }})</small>
      {% if post.categories.size > 0 %}
        — Categories: 
        {% for cat in post.categories %}
          <a href="{{ '/categories/#' | append: cat | relative_url }}">{{ cat }}</a>{% unless forloop.last %}, {% endunless %}
        {% endfor %}
      {% endif %}
    </li>
  {% endfor %}
</ul>
