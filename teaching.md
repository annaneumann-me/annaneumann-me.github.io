---
layout: default
title: teaching
permalink: /teaching/
---

<header class="page-header">
  <p class="kicker">📚</p>
  <h1><span class="leaf-underline">teaching</span></h1>
</header>

<div class="two-col">
  <div class="soft-card">
    <h2>courses</h2>
    <ul class="about-list" style="margin-top: 1rem;">
      {% for c in site.data.teaching.courses %}
      <li style="display: block;">
        <p class="kicker" style="margin: 0;">{{ c.kind }} · {{ c.term }}</p>
        <p style="margin: 0.2rem 0 0; font-family: var(--font-serif);">{{ c.title }}</p>
      </li>
      {% endfor %}
    </ul>
  </div>

  <div class="soft-card">
    <h2>theses supervised</h2>
    <ul class="about-list" style="margin-top: 1rem;">
      {% for th in site.data.teaching.theses %}
      <li><span class="dot">·</span><span>20{{ th.year }} — {{ th.student }} <span style="font-style: italic; color: var(--muted-foreground);">({{ th.status }})</span></span></li>
      {% endfor %}
    </ul>
  </div>
</div>
