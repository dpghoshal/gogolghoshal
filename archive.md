---
layout: default
---

## Blog

<ul>
  {% for post in site.posts %}
    <li>
      <p>
      <a href="{{ post.url }}"><strong>{{ post.title }}</strong></a> <br>
      {{ post.date | date_to_long_string }}
      </p>
    </li>
  {% endfor %}
</ul>

* * *

[Back](./)
