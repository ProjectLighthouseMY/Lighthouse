---
layout: default
title: Research
permalink: /research/
---

<p class="eyebrow">Research</p>

# Notes from Project Lighthouse

Short write-ups on security research, reviews, emerging risks and lessons from responsible disclosure.

{% for post in site.posts %}
<article class="post-row">
  <div>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    {% if post.summary %}<p>{{ post.summary }}</p>{% endif %}
  </div>
  <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d %b %Y" }}</time>
</article>
{% endfor %}
