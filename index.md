---
layout: default
title: "Latest News"
description: "Новости технологий будущего"
permalink: /
---

<div class="articles">
{% assign posts_sorted = site.posts | sort: 'date' | reverse %}
{% for post in posts_sorted %}
  {% assign slug = post.slug %}
  <article class="card">
    <a href="{{ post.url | relative_url }}">
      <img src="/{{ site.image_dir }}/{{ slug }}.jpg" alt="{{ post.title }}" class="preview">
      <h2>{{ post.title }}</h2>
      <p>{{ post.description }}</p>
    </a>
  </article>
{% endfor %}
</div>
