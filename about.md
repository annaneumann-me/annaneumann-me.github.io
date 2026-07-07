---
layout: default
title: about
permalink: /about/
---

<header class="page-header">
  <p class="kicker">(•ᴗ•)</p>
  <h1><span class="leaf-underline">a little about me</span></h1>
</header>

<div class="links" style="margin-top: 1.5rem;">
  <a class="tag tag--paper" href="/assets/cv.pdf" style="font-size: 0.8rem; padding: 0.4rem 1rem;">download cv ↗</a>
</div>

<ul class="about-list" style="margin-top: 2rem;">
  <li><span class="dot">·</span><span>bsc electrical engineering &amp; information technology @ rub — thesis on ai for speech and music separation.</span></li>
  <li><span class="dot">·</span><span>msc information &amp; communication technology @ rub — thesis on nlp &amp; ml strategies for detecting fake news.</span></li>
  <li><span class="dot">·</span><span>got into critical computing while doing my master's via ai bias seminars and philosophy courses.</span></li>
  <li><span class="dot">·</span><span>in my phd, i look at responsible ai through the lens of computer science, trying to further informed governance through meaningful auditing of systems and involvement of various stakeholders.</span></li>
</ul>

<section style="margin-top: 3.5rem;">
  <h2>academic service</h2>
  <div class="two-col" style="margin-top: 1rem;">
    <div class="soft-card">
      <p class="kicker">external</p>
      <ul class="about-list">
        {% for s in site.data.service.external %}<li><span class="dot">·</span><span>{{ s }}</span></li>{% endfor %}
      </ul>
    </div>
    <div class="soft-card">
      <p class="kicker">internal</p>
      <ul class="about-list">
        {% for s in site.data.service.internal %}<li><span class="dot">·</span><span>{{ s }}</span></li>{% endfor %}
      </ul>
    </div>
  </div>
</section>
