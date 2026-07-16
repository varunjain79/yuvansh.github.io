---
layout: default
title: "What I Learned at School"
permalink: /school/
---

- What I Learned at School
Things I understood or discovered in school.
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
#- Today in Math, I did calendar reading in my Mental Maths book.
#- Today in English, I wrote 6 words from a story on a sheet.
#- Yesterday in school my teacher told the class to find fair situations.
