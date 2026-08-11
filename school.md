---
layout: default
title: "What I Learned at School"
permalink: /school/
---

- What I Learned at School
Things I understood or discovered in school.

<div class="card" style="border-color: rgba(34, 197, 94, 0.55);">
  <h3>📅 Today — August 11, 2026</h3>
  <p><strong>School Holiday</strong></p>
  <p>Today was a holiday, so I did not go to school.</p>
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
#- Today in Math, I did Asending order and Desending order.
#- Today in English, I did Spell Well.
