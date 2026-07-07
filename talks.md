---
layout: default
title: talks & service
permalink: /talks/
---

<header class="page-header">
  <p class="kicker">talks · service · teaching</p>
  <h1><span class="leaf-underline">out in the world</span></h1>
</header>

<section style="margin-top: 3.5rem;">
  <p class="kicker">🎤</p>
  <h2 style="margin-top: 0.5rem;">invited talks</h2>
  <ul class="dated-list" style="margin-top: 1.5rem;">
    {% for t in site.data.talks %}
    <li><span class="date">{{ t.date }}</span><span>{{ t.venue }}</span></li>
    {% endfor %}
  </ul>
</section>

<section style="margin-top: 3.5rem;">
  <p class="kicker">📅</p>
  <h2 style="margin-top: 0.5rem;">events</h2>
  <ul class="dated-list" style="margin-top: 1.5rem;">
    {% for e in site.data.events %}
    <li><span class="date">{{ e.date }}</span><span>{{ e.venue }}{% if e.role %} <span class="role">— {{ e.role }}</span>{% endif %}</span></li>
    {% endfor %}
  </ul>
</section>

<section style="margin-top: 3.5rem;">
  <p class="kicker">📰</p>
  <h2 style="margin-top: 0.5rem;">media</h2>
  <ul class="entry-list" style="margin-top: 1.5rem;">
    {% for m in site.data.media %}
    <li class="soft-card">
      <p class="meta" style="margin: 0; font-family: var(--font-mono); font-size: 0.8rem;">{{ m.date }} · {{ m.outlet }}</p>
      <p style="margin-top: 0.4rem; font-family: var(--font-serif); font-size: 1.1rem; color: var(--primary);">{{ m.title }}</p>
    </li>
    {% endfor %}
  </ul>
</section>

<div class="two-col">
  <div class="soft-card">
    <h2>academic service</h2>
    <p class="kicker" style="margin-top: 1rem;">external</p>
    <ul class="about-list">
      {% for s in site.data.service.external %}<li><span class="dot">·</span><span>{{ s }}</span></li>{% endfor %}
    </ul>
    <p class="kicker" style="margin-top: 1.25rem;">internal</p>
    <ul class="about-list">
      {% for s in site.data.service.internal %}<li><span class="dot">·</span><span>{{ s }}</span></li>{% endfor %}
    </ul>
  </div>

  <div class="soft-card">
    <h2>teaching</h2>
    <ul class="about-list" style="margin-top: 1rem;">
      {% for c in site.data.teaching.courses %}
      <li style="display: block;">
        <p class="kicker" style="margin: 0;">{{ c.kind }} · {{ c.term }}</p>
        <p style="margin: 0.2rem 0 0; font-family: var(--font-serif);">{{ c.title }}</p>
      </li>
      {% endfor %}
    </ul>

    <h3 style="margin-top: 1.5rem;">theses supervised</h3>
    <ul class="about-list">
      {% for th in site.data.teaching.theses %}
      <li><span class="dot">·</span><span>20{{ th.year }} — {{ th.student }} <span style="font-style: italic; color: var(--muted-foreground);">({{ th.status }})</span></span></li>
      {% endfor %}
    </ul>
  </div>
</div>
