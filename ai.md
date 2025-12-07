---
layout: default
title: "My Custom AIs"
permalink: /ai/
---

<div class="card">
  <h2>My Custom AIs</h2>
  <p>Custom GPTs, Meta AIs and other bots I make or chat with.</p>
</div>

{% assign items = site.posts | where: "category", "ai" | sort: "date" | reverse %}
{% for post in items %}
  <a class="post-link" href="{{ post.url | relative_url }}">
    <div class="card">
      <h3>{{ post.title }}</h3>
      <div class="meta">{{ post.date | date: "%B %d, %Y" }}</div>
      <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
    </div>
  </a>
{% endfor %}
