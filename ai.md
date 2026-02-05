---
layout: default
title: "My Custom AIs"
permalink: /ai/
---

<div class="card">
  <h2>My Custom AIs</h2>
  <p>Custom GPTs, Meta AIs and other bots I make or chat with.</p>
  <p>I made a GPT called Yuvansh Try it out</p> https://chatgpt.com/g/g-698346d71f94819185d8a8549441a81e-yuvansh
  and
  <p>I have also made YJ It is also a GPT Like Yuvansh Try it out<p> https://chatgpt.com/g/g-68f9db2ed5fc81919dc761a8087b7e65-yj
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
