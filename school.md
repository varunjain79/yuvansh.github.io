---
layout: default
title: "What I Learned at School"
permalink: /school/
---

<div class="card">
  <h2>What I Learned at School</h2>
  <p>Things I understood or discovered in school.</p>
</div>

{% assign items = site.posts | where: "category", "school" | sort: "date" | reverse %}
{% for post in items %}
  <a class="post-link" href="{{ post.url | relative_url }}">
    <div class="card">
      <h3>{{ post.title }}</h3>
      <div class="meta">{{ post.date | date: "%B %d, %Y" }}</div>
      <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
    </div>
  </a>
{% endfor %}
