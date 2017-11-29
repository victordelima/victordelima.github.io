---
layout: default
---

<div class="home">

  {{ content }}

  <h1 class="page-heading">Artigos</h1>

  <ul class="post-list">
    {% for post in site.posts %}
    <li>
      {% assign date_format = site.minima.date_format | default: "%-d %b de %Y" %}
      <span class="post-meta">{{ post.date | date: date_format }}</span>

      <p><img src="{{ post.img_cover }}"></p>
      <h2>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h2>
      {{ post.excerpt }}
      <hr>
    </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">assine <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p>

</div>
