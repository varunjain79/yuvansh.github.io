---
layout: default
title: "Updates"
permalink: /updates/
---

- Updates
  News about me, my life and changes on this website.

{% assign items = site.posts | where: "category", "updates" | sort: "date" | reverse %}
{% for post in items %}
 <a class="post-link" href="{{ post.url | relative_url }}">
    <div class="card">
      <h3>{{ post.title }}</h3>
      <div class="meta">{{ post.date | date: "%B %d, %Y" }}</div>
      <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
    </div>
  </a>
{% endfor %}
