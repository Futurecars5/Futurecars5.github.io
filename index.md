---
layout: default
title: Future Cars 2025–2045
description: "Cars 2025–2045: $15k EVs, 0–100 in 0.9 s, full autonomy, 6-min charging, flying taxis, zero road deaths. Facts only, zero hype."
---

<div class="home-hero">
  <h1>Future Cars<br><span>2025–2045</span></h1>
  <p class="subtitle">30 chapters • 20-year roadmap • Everything already funded and built</p>
</div>

<div class="posts-grid">
  {% for post in site.posts %}
    {% comment %}Ищем первую картинку в контенте поста{% endcomment %}
    {% assign first_image = post.content | split: 'src="' | slice: 1 | first | split: '"' | first %}

    <article class="post-card">
      <a href="{{ post.url }}" class="post-link">
        <div class="post-thumb-wrapper">
          {% if first_image %}
            <img src="{{ first_image }}" alt="{{ post.title }}" class="post-thumb">
          {% else %}
            <img src="/images/default.jpg" alt="Future car" class="post-thumb">
          {% endif %}
        </div>
        <div class="post-info">
          <h2>{{ post.title | remove: "00. " | remove: "01. " | remove: "02. " | remove: "03. " | remove: "04. " | remove: "05. " | remove: "06. " | remove: "07. " | remove: "08. " | remove: "09. " | remove: "10. " | remove: "11. " | remove: "12. " | remove: "13. " | remove: "14. " | remove: "15. " | remove: "16. " | remove: "17. " | remove: "18. " | remove: "19. " | remove: "20. " | remove: "21. " | remove: "22. " | remove: "23. " | remove: "24. " | remove: "25. " | remove: "26. " | remove: "27. " | remove: "28. " | remove: "29. " | remove: "30. " }}</h2>
          <p class="post-desc">{{ post.description }}</p>
          <span class="read-more">Read chapter →</span>
        </div>
      </a>
    </article>
  {% endfor %}
</div>

<div class="made-with">
</div>
