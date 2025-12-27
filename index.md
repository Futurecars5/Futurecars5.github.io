---
layout: default
title: Future Cars 2025–2045
description: "Cars 2025–2045: $15k EVs, 0–100 in 0.9s, full autonomy, 6-min charging, flying taxis, zero road deaths. Facts only, zero hype."
---


<div class="posts-grid">
  {% assign sorted_posts = site.posts | reverse %}
  {% for post in sorted_posts %}

    {% assign first_image = post.content
      | split:'<img'
      | slice:1
      | first
      | split:'src="'
      | slice:1
      | first
      | split:'"'
      | first %}

    <article class="post-card">
      <a href="{{ post.url }}">
        <div class="post-thumb-wrapper">
          <img src="{{ first_image }}" alt="{{ post.title }}" class="post-thumb">
        </div>
        <div class="post-info">
          <h2>{{ post.title | split: ". " | last }}</h2>
          <p class="post-desc">{{ post.description }}</p>
          <span class="read-more">Read chapter</span>
        </div>
      </a>
    </article>

  {% endfor %}
</div>

<div class="made-with">
  <p>All images • Full offline • No tracking • Built November 2025</p>
</div>
