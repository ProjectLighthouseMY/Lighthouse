---
layout: default
title:
description: Project Lighthouse conducts focused security research and practical security reviews.
---
<section class="hero-shell">
  <div class="hero-image" aria-hidden="true"></div>
  <div class="hero-beacon" aria-hidden="true"><span class="beam beam-left"></span><span class="beam beam-right"></span><span class="lantern-glow"></span></div>
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
