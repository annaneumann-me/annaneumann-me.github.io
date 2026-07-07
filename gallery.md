---
layout: default
title: gallery
permalink: /gallery/
---

<header class="page-header">
  <p class="kicker">📷</p>
  <h1><span class="leaf-underline">gallery</span></h1>
  <p>a few pictures — scroll sideways. drop a file into <code>assets/img/gallery/</code> to add one.</p>
</header>

{% assign gallery_images = site.static_files | where_exp: "f", "f.path contains '/assets/img/gallery/'" | sort: "name" %}
<div class="carousel">
  {% for img in gallery_images %}
  <div class="carousel-item">
    <figure>
      <img src="{{ img.path | relative_url }}" alt="{{ img.basename | replace: '-', ' ' | replace: '_', ' ' }}">
      <figcaption>{{ img.basename | replace: '-', ' ' | replace: '_', ' ' }}</figcaption>
    </figure>
  </div>
  {% endfor %}
</div>
