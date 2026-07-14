---
layout: default
title: "What I Learned at School"
permalink: /school/
---

- What I Learned at School
Things I understood or discovered in school.
#- Today in Maths i did Addition and subtraction sums in my practice notebook.
#- I wrote Senteces in Hindi.
#- I learnt about lawyers and judges in my Blossoms book.
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
