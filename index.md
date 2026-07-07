---
layout: default
title: home
---

<section class="hero">
  <div>
    <p class="kicker">phd student · critical computing · responsible ai</p>
    <h1><span class="leaf-underline">anna neumann</span> <span aria-hidden="true">🌱</span></h1>
    <p class="affiliation">compliant and accountable systems group (led by jat singh) at the research center for trustworthy ai, germany</p>
    <p class="focus">examining how ai systems influence sociotechnical structures with a focus on responsible ai practices in algorithmic supply chains</p>

    <div class="links">
      <a class="tag" href="/assets/cv.pdf">cv ↗</a>
      <a class="tag" href="https://scholar.google.com/">google scholar ↗</a>
      <a class="tag" href="https://substack.com/">substack ↗</a>
      <a class="tag" href="#">affiliation ↗</a>
      <a class="tag" href="mailto:an@newmanconsulting.de">email ↗</a>
    </div>
  </div>

  <div class="aside">
    <div class="avatar">
      <img src="/assets/img/anna.jpg" alt="portrait of anna neumann">
    </div>
    <div class="soft-card aside-card">
      <p class="kicker">currently</p>
      <p style="margin-top: 0.5rem; font-family: var(--font-serif); font-size: 1.1rem; color: var(--primary); line-height: 1.4;">
        reading obscure feminist literature &amp; sipping matcha 🍵
      </p>
      <p style="margin-top: 0.75rem; font-size: 0.8rem; color: var(--muted-foreground); font-family: var(--font-mono);">( ˵ •̀ ᴗ •́˵ )</p>
    </div>
  </div>
</section>

<div class="two-col">
  <div class="soft-card media-card">
    <h2 style="font-size: 1.1rem;">media</h2>
    <ul>
      {% for m in site.data.media %}
      <li>
        <p class="date">{{ m.date }} · {{ m.outlet }}</p>
        <p class="title">{{ m.title }}</p>
        {% if m.url and m.url != "#" %}<a class="tag tag--paper" href="{{ m.url }}">read ↗</a>{% endif %}
      </li>
      {% endfor %}
    </ul>
  </div>

  <div class="soft-card">
    <h3>let's chat 🌿</h3>
    <p style="font-size: 0.9rem; color: var(--muted-foreground);">
      always up for a conversation about responsible ai, feminist tech critique, or matcha spots.
    </p>
    <div class="links" style="margin-top: 0.75rem;">
      <a class="tag" href="mailto:an@newmanconsulting.de">email ↗</a>
      <a class="tag" href="#">linkedin ↗</a>
      <a class="tag" href="#">bluesky ↗</a>
      <a class="tag" href="#">x ↗</a>
    </div>

    <hr>

    <h2 style="font-size: 1.1rem;">obsessed with</h2>
    <div class="links" style="margin-top: 1rem;">
      <span class="tag">obscure feminist literature</span>
      <span class="tag">thrifting</span>
      <span class="tag">good matcha 🍵</span>
    </div>
  </div>
</div>

<section style="margin-top: 3.5rem;">
  <p class="kicker">research threads</p>
  <h2 style="margin-top: 0.5rem; font-size: 1.6rem;"><span class="leaf-underline">what i'm thinking about</span></h2>
  <p style="color: var(--muted-foreground); max-width: 40rem;">overlapping threads that show up across my papers, talks, and teaching.</p>

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
</section>
