---
layout: default
---

## Blog

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> <br>
      {{ post.date | date_to_long_string }}
    </li>
  {% endfor %}
</ul>
