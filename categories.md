---
layout: default
title: Categories
---

# Categories

<ul>
  {% assign cats = site.categories | sort %}
  {% for cat in cats %}
    <li>
      <a href="#{{ cat[0] }}">{{ cat[0] }}</a> ({{ cat[1].size }})
    </li>
  {% endfor %}
</ul>

---

{% for cat in cats %}
  <h2 id="{{ cat[0] }}">{{ cat[0] }}</h2>
  <ul>
    {% for post in cat[1] %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
