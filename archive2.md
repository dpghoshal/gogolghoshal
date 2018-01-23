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

Follow [@gogolghoshal](https://twitter.com/gogolghoshal) on Twitter or like [Gogol Ghoshal](https://www.facebook.com/GogolGhoshal) on Facebook for blog (& other) updates

* * *

[Back](./)
