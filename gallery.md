---
layout: default
title: gallery
permalink: /gallery/
---

<header class="page-header">
  <p class="kicker">📷</p>
  <h1><span class="leaf-underline">gallery</span></h1>
  <p>a few pictures. drop a file into <code>assets/img/gallery/</code> to add one.</p>
</header>

{% assign gallery_images = site.static_files | where_exp: "f", "f.path contains '/assets/img/gallery/'" | sort: "name" %}
<div class="photo-gallery">
  {% for img in gallery_images %}
  <figure>
    <img src="{{ img.path | relative_url }}" alt="{{ img.basename | replace: '-', ' ' | replace: '_', ' ' }}">
  </figure>
  {% endfor %}
</div>
