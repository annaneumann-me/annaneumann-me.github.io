---
layout: default
title: gallery
permalink: /gallery/
---

<header class="page-header">
  <p class="kicker">📷</p>
  <h1><span class="leaf-underline">gallery</span></h1>
  <p>a few pictures — scroll sideways.</p>
</header>

<div class="carousel">
  {% for img in site.data.gallery %}
  <div class="carousel-item">
    <figure>
      <img src="{{ img.src }}" alt="{{ img.caption }}">
      <figcaption>{{ img.caption }}</figcaption>
    </figure>
  </div>
  {% endfor %}
</div>
