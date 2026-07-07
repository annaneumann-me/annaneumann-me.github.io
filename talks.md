---
layout: default
title: talks
permalink: /talks/
---

<header class="page-header">
  <p class="kicker">talks · events</p>
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
