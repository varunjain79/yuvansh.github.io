---
layout: default
title: "My YouTube Stuff"
permalink: /youtube/
---

<div class="card">
  <h2>My YouTube Stuff</h2>
  <p>My favourite channels, videos I like, and anything I post on YouTube.</p>
</div>

{% assign items = site.posts | where: "category", "youtube" | sort: "date" | reverse %}
{% for post in items %}
  <a class="post-link" href="{{ post.url | relative_url }}">
    <div class="card">
      <h3>{{ post.title }}</h3>
      <div class="meta">{{ post.date | date: "%B %d, %Y" }}</div>
      <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
    </div>
  </a>
{% endfor %}
