---
layout: default
title: events
permalink: /events/
---

<header class="page-header">
  <p class="kicker">talks · events</p>
  <h1><span class="leaf-underline">out in the world</span></h1>
</header>

<section style="margin-top: 3rem;">
  <div class="section-heading"><h2>invited talks</h2></div>
  <ul class="entry-list">
    {% for t in site.data.talks %}
    <li class="soft-card pub-card">
      <p class="entry-date">{{ t.date }}</p>
      <div class="top-row">
        <h3>{{ t.venue }}</h3>
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
  <div class="section-heading"><h2>events</h2></div>
  <ul class="entry-list">
    {% for e in site.data.events %}
    <li class="soft-card pub-card">
      <div class="top-row">
        <p class="entry-date" style="margin: 0;">{{ e.date }}</p>
        {% if e.role %}<span class="tag tag--video">{{ e.role }}</span>{% endif %}
      </div>
      <h3 style="margin-top: 0.35rem;">{{ e.venue }}</h3>
      {% if e.note %}<p class="meta" style="font-style: italic;">{{ e.note }}</p>{% endif %}
      {% if e.url and e.url != "#" %}
      <div class="links"><a class="tag tag--paper" href="{{ e.url }}">visit ↗</a></div>
      {% endif %}
    </li>
    {% endfor %}
  </ul>
</section>
