---
layout: default
title: Future Cars 2025–2045
description: "Cars 2025–2045: $15k EVs, 0–100 in 0.9s, full autonomy, 6-min charging, flying taxis, zero road deaths. Facts only, zero hype."
---

<div class="home-hero">
  <h1>Future Cars<br><span>2025–2045</span></h1>
  <p class="subtitle">Everything already funded and built</p>
</div>

<div class="posts-grid">
  {% assign sorted_chapters = site.chapters | sort: 'title' %}
  {% for post in sorted_chapters %}
    {% assign first_image = post.content | split:'src="' | slice:1 | first | split:'"' | first %}

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
