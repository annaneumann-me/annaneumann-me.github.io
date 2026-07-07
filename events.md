---
layout: default
title: events
permalink: /events/
---

<header class="page-header">
  <p class="kicker">talks · events</p>
  <h1><span class="leaf-underline">out in the world</span></h1>
</header>

<section style="margin-top: 3.5rem;">
  <p class="kicker">🎤</p>
  <h2 style="margin-top: 0.5rem;">invited talks</h2>
  <ul class="entry-list" style="margin-top: 1.5rem;">
    {% for t in site.data.talks %}
    <li class="soft-card pub-card">
      <div class="top-row">
        <h3>{{ t.venue }}</h3>
        <span class="tag">{{ t.date }}</span>
      </div>
      {% if t.role %}<p class="meta" style="font-style: italic;">{{ t.role }}</p>{% endif %}
      {% if t.url and t.url != "#" %}
      <div class="links"><a class="tag tag--paper" href="{{ t.url }}">group ↗</a></div>
      {% endif %}
    </li>
    {% endfor %}
  </ul>
</section>

<section style="margin-top: 3.5rem;">
  <p class="kicker">📅</p>
  <h2 style="margin-top: 0.5rem;">events</h2>
  <ul class="entry-list" style="margin-top: 1.5rem;">
    {% for e in site.data.events %}
    <li class="soft-card pub-card">
      <div class="top-row">
        <h3>{{ e.venue }}</h3>
        <div style="display: flex; gap: 0.4rem; flex-wrap: wrap;">
          <span class="tag">{{ e.date }}</span>
          {% if e.role %}<span class="tag tag--video">{{ e.role }}</span>{% endif %}
        </div>
      </div>
      {% if e.note %}<p class="meta" style="font-style: italic;">{{ e.note }}</p>{% endif %}
      {% if e.url and e.url != "#" %}
      <div class="links"><a class="tag tag--paper" href="{{ e.url }}">visit ↗</a></div>
      {% endif %}
    </li>
    {% endfor %}
  </ul>
</section>
