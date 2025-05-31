---
layout: default
title: Book Notes
---

# 📚 Book Notes

<ul>
  {% for note in site.booknotes %}
    <li>
      <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
      <small>by {{ note.author }}</small>
      {% if note.categories.size > 0 %}
        — Categories:
        {% for cat in note.categories %}
          <a href="{{ '/categories/#' | append: cat | relative_url }}">{{ cat }}</a>{% unless forloop.last %}, {% endunless %}
        {% endfor %}
      {% endif %}
    </li>
  {% endfor %}
</ul>
