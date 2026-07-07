---
layout: default
title: Stuff I Did
permalink: /research/
---

# Stuff I Did 𓂃🖊

## Papers (first author)

<ul class="entry-list">
{% for p in site.data.papers_first_author %}
  <li>
    {{ p.title }} — <span class="meta">{{ p.venue }}{% if p.status %}, {{ p.status }}{% endif %}</span>
    {% if p.award %}<span class="award">{{ p.award }}</span>{% endif %}
    {% if p.links %}<div class="links">{% for l in p.links %}<a href="{{ l.url }}">[{{ l.label }}]</a>{% endfor %}</div>{% endif %}
  </li>
{% endfor %}
</ul>

## Other papers

<ul class="entry-list">
{% for p in site.data.papers_other %}
  <li>{{ p.title }} — <span class="meta">{{ p.venue }}</span></li>
{% endfor %}
</ul>

## Invited talks

<ul class="entry-list">
{% for t in site.data.talks %}
  <li><span class="meta">{{ t.date }}</span> {{ t.title }}</li>
{% endfor %}
</ul>

## Posters

wip

## Media

<ul class="entry-list">
{% for m in site.data.media %}
  <li><span class="meta">{{ m.date }}</span> <a href="{{ m.url }}">{{ m.title }}</a> — <span class="meta">{{ m.outlet }}</span></li>
{% endfor %}
</ul>

## Academic service

### External

<ul class="entry-list">
{% for s in site.data.service.external %}
  <li><span class="meta">{{ s.year }}:</span> {{ s.venue }} [{{ s.role }}]</li>
{% endfor %}
</ul>

### Internal

<ul class="entry-list">
{% for s in site.data.service.internal %}
  <li><span class="meta">{{ s.year }}:</span> {{ s.role }}</li>
{% endfor %}
</ul>

## Events

<ul class="entry-list">
{% for e in site.data.events %}
  <li><span class="meta">{{ e.date }}:</span> {{ e.title }}{% if e.role %} [{{ e.role }}]{% endif %}</li>
{% endfor %}
</ul>

## Teaching

### Courses

<ul class="entry-list">
{% for c in site.data.teaching.courses %}
  <li>{{ c.title }} <span class="meta">({{ c.term }})</span></li>
{% endfor %}
</ul>

### Theses

<ul class="entry-list">
{% for th in site.data.teaching.theses %}
  <li>{{ th.year }}: {{ th.student }}{% if th.status %} ({{ th.status }}){% endif %}</li>
{% endfor %}
</ul>
