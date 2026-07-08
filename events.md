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
  <ul class="dated-list">
    {% for t in site.data.talks %}
    <li>
      <span class="date">{{ t.date }}</span>
      <span class="row-content">
        <span class="venue-text">{{ t.venue }}</span>
        {% if t.role %}<span class="row-note">— {{ t.role }}</span>{% endif %}
        {% if t.url and t.url != "#" %}<a class="tag tag--paper" href="{{ t.url }}">group ↗</a>{% endif %}
      </span>
    </li>
    {% endfor %}
  </ul>
</section>

<section style="margin-top: 3.5rem;">
  <div class="section-heading"><h2>events</h2></div>
  <ul class="dated-list">
    {% for e in site.data.events %}
    <li>
      <span class="date">{{ e.date }}</span>
      <span class="row-content">
        <span class="venue-text">{{ e.venue }}</span>
        {% if e.role %}<span class="tag tag--video">{{ e.role }}</span>{% endif %}
        {% if e.note %}<span class="row-note">— {{ e.note }}</span>{% endif %}
        {% if e.url and e.url != "#" %}<a class="tag tag--paper" href="{{ e.url }}">visit ↗</a>{% endif %}
      </span>
    </li>
    {% endfor %}
  </ul>
</section>
