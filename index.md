---
layout: default
title: "Latest News"
---

<div class="articles">
  {% for post in site.posts %}
  <div class="card">
    <a href="{{ post.url }}">
      <img src="/images/{{ post.slug }}.jpg" class="preview">
      <h2>{{ post.title }}</h2>
      <p>{{ post.description }}</p>
    </a>
  </div>
  {% endfor %}
</div>
