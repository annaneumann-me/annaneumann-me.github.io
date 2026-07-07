---
layout: default
title: research
permalink: /projects/
---

<header class="page-header">
  <p class="kicker">research threads</p>
  <h1><span class="leaf-underline">what i'm thinking about</span></h1>
  <p>overlapping threads that show up across my papers, talks, and teaching.</p>
</header>

<div class="project-grid">
  {% for p in site.data.projects %}
  <article class="soft-card">
    <h2>{{ p.title }}</h2>
    <p style="margin-top: 0.75rem; font-size: 0.9rem; color: var(--foreground); line-height: 1.6;">{{ p.summary }}</p>
    <div class="tags">
      {% for t in p.tags %}<span class="tag">{{ t }}</span>{% endfor %}
    </div>
  </article>
  {% endfor %}
</div>
