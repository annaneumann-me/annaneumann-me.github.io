---
layout: default
title: papers
permalink: /publications/
---

<header class="page-header">
  <p class="kicker">𓂃🖊 papers</p>
  <h1><span class="leaf-underline">stuff i wrote</span></h1>
  <p>peer-reviewed papers, workshop contributions, and preprints — mostly first-authored, across FAccT, CHI, ICML workshops, and friends.</p>
</header>

{% assign pubs_by_year = site.data.publications | group_by: "year" | sort: "name" | reverse %}
{% for group in pubs_by_year %}
<div class="year-group">
  <div class="year-heading">
    <h2>{{ group.name }}</h2>
    <span class="rule"></span>
    <span class="count">{{ group.items.size }} {% if group.items.size == 1 %}paper{% else %}papers{% endif %}</span>
  </div>
  <ul class="entry-list">
    {% for p in group.items %}
    <li class="soft-card pub-card">
      <div class="top-row">
        <h3>{{ p.title }}</h3>
        {% if p.status %}<span class="tag">✦ {{ p.status }}</span>{% endif %}
      </div>
      <p class="meta"><span class="venue">{{ p.venue }}</span> · <span style="font-style: italic;">{{ p.role }}</span></p>
      {% if p.links %}
      <div class="links">
        {% for l in p.links %}<a class="tag" href="{{ l.url }}">{{ l.label }} ↗</a>{% endfor %}
      </div>
      {% endif %}
    </li>
    {% endfor %}
  </ul>
</div>
{% endfor %}
