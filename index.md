---
layout: default
title:
description: Project Lighthouse conducts focused security research and practical security reviews.
---
<section class="hero-shell">
  <svg class="hero-scene" viewBox="0 0 1600 760" preserveAspectRatio="xMidYMid slice" aria-hidden="true" focusable="false">
    <defs>
      <linearGradient id="beam-left-gradient" x1="0" y1="0" x2="1" y2="0"><stop offset="0" stop-color="#d2e1de" stop-opacity="0"/><stop offset=".45" stop-color="#e1ece9" stop-opacity=".11"/><stop offset="1" stop-color="#f2f7f5" stop-opacity=".28"/></linearGradient>
      <linearGradient id="beam-right-gradient" x1="0" y1="0" x2="1" y2="0"><stop offset="0" stop-color="#f2f7f5" stop-opacity=".26"/><stop offset=".55" stop-color="#e1ece9" stop-opacity=".1"/><stop offset="1" stop-color="#d2e1de" stop-opacity="0"/></linearGradient>
      <radialGradient id="lantern-gradient"><stop offset="0" stop-color="#f5f9f7" stop-opacity=".38"/><stop offset=".42" stop-color="#cde0da" stop-opacity=".1"/><stop offset=".72" stop-color="#cde0da" stop-opacity="0"/></radialGradient>
      <filter id="beam-blur" x="-10%" y="-60%" width="120%" height="220%"><feGaussianBlur stdDeviation="7"/></filter>
      <filter id="glow-blur" x="-80%" y="-80%" width="260%" height="260%"><feGaussianBlur stdDeviation="4"/></filter>
    </defs>
    <image class="hero-photo" href="{{ '/assets/images/lighthouse-hero-clean.png' | relative_url }}" x="0" y="0" width="1600" height="760"/>
    <g class="svg-beacon">
      <path class="svg-beam svg-beam-left" d="M 890 198 L 0 145 L 0 267 L 890 214 Z" fill="url(#beam-left-gradient)" filter="url(#beam-blur)"/>
      <path class="svg-beam svg-beam-right" d="M 890 198 L 1600 145 L 1600 267 L 890 214 Z" fill="url(#beam-right-gradient)" filter="url(#beam-blur)"/>
      <circle class="svg-lantern-glow" cx="890" cy="206" r="34" fill="url(#lantern-gradient)" filter="url(#glow-blur)"/>
    </g>
  </svg>
  <div class="hero-overlay"></div>
  <div class="page-width hero-content">
    <p class="eyebrow light">Security Research</p><h1>Project Lighthouse</h1>
    <p class="lead">Finding weak signals before they become incidents.</p><span class="blue-rule"></span>
    <p class="hero-intro">Project Lighthouse conducts focused security research and practical security reviews, with an emphasis on clear findings, responsible disclosure and useful remediation.</p>
  </div>
</section>
<section class="page-width pillars">
  <article class="pillar"><span class="icon-disc"><img src="{{ '/assets/icons/search.svg' | relative_url }}" alt=""></span><h2>Research</h2><p>We explore security weaknesses, attack surfaces and emerging risks across technologies and systems.</p></article>
  <article class="pillar"><span class="icon-disc"><img src="{{ '/assets/icons/shield.svg' | relative_url }}" alt=""></span><h2>Review</h2><p>We perform security reviews of applications, architectures and exposed services to identify and mitigate risk.</p></article>
  <article class="pillar"><span class="icon-disc"><img src="{{ '/assets/icons/paper-plane.svg' | relative_url }}" alt=""></span><h2>Disclose</h2><p>We communicate verified issues responsibly and support remediation to improve security for everyone.</p></article>
</section>
<section class="page-width split-section">
  <div class="panel"><p class="section-label">Latest Research</p><span class="small-rule"></span>{% for post in site.posts limit:3 %}<article class="research-row"><div><h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d %b %Y" }}</time></div><a class="arrow" aria-label="Read {{ post.title }}" href="{{ post.url | relative_url }}">→</a></article>{% endfor %}<a class="outline-button" href="{{ '/research/' | relative_url }}">View all research</a></div>
  <div class="panel"><p class="section-label">Operating Principles</p><span class="small-rule"></span>
    <div class="principle"><img src="{{ '/assets/icons/user.svg' | relative_url }}" alt=""><div><h3>Publicly Available</h3><p>We assess publicly available systems and attack surfaces using safe, non-intrusive methods.</p></div></div>
    <div class="principle"><img src="{{ '/assets/icons/heartbeat.svg' | relative_url }}" alt=""><div><h3>Minimal Impact</h3><p>We prioritise safe testing methods and minimise impact on systems and users.</p></div></div>
    <div class="principle"><img src="{{ '/assets/icons/lock.svg' | relative_url }}" alt=""><div><h3>Responsible Disclosure</h3><p>We work with organisations to communicate and remediate verified issues responsibly.</p></div></div>
  </div>
</section>
