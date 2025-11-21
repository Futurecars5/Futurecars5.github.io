---
layout: default
title: "Future cars"
description: "Cars 2025–2045: $15k EVs, 0–100 in 0.9 s, full autonomy, 6-minute charging, flying taxis, zero road deaths. Facts only, zero hype."
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
