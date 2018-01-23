---
layout: default
---

## Blog

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> <br>
      {{ post.date | date_to_long_string }} <br>
    </li>
  {% endfor %}
</ul>

* * *

Follow [@gogolghoshal](https://twitter.com/gogolghoshal) on Twitter or like [Gogol Ghoshal](https://www.facebook.com/GogolGhoshal) on Facebook for blog (& other) updates

* * *

[Back](./)
