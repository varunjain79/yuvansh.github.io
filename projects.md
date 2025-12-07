---
layout: default
title: "Projects"
permalink: /projects/
---

<div class="card">
  <h2>Projects</h2>
  <p>Things I built: games, drawings, LEGO stuff, experiments.</p>
</div>

{% assign items = site.posts | where: "category", "projects" | sort: "date" | reverse %}
{% for post in items %}
  <a class="post-link" href="{{ post.url | relative_url }}">
    <div class="card">
      <h3>{{ post.title }}</h3>
      <div class="meta">{{ post.date | date: "%B %d, %Y" }}</div>
      <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
    </div>
  </a>
{% endfor %}
