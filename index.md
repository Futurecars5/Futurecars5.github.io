---
layout: default
title: "Latest Articles"
---

<h1>Latest Articles</h1>

<ul class="posts">

{% for post in site.posts %}
  {% assign img_regex = '<img.*src="([^"]*)"' %}
  {% assign first_image = post.content | regex_scan: img_regex | first %}
  {% if first_image %}
    {% assign card_image = first_image[1] %}
  {% else %}
    {% assign card_image = '/images/default.jpg' %}
  {% endif %}

  <li class="post-item">
    <a href="{{ post.url | relative_url }}">
      <img src="{{ card_image }}" alt="" class="post-thumb">
      <h2>{{ post.title }}</h2>
      <p>{{ post.description }}</p>
    </a>
  </li>

{% endfor %}

</ul>
