---
layout: default
title: "What I Learned at School"
permalink: /school/
---

- What I Learned at School
Things I understood or discovered in school
#- Today in Mental Math I did Mental Maths questions (05.02.2026) 1. A bag weighs 2 kg and another weighs 1 kg. What is the total weight of both the bags in kgs? 2. Which is the 6th month of the year? 3. ⁠What is the place value of 6 in 16? 4. I am more than 20 but less than 25.I am ___. 5. Write any even number that comes after 11. And I got 2 stars
#- Aaj Main Ne हिंदी me मात्रा ज्ञान में से कहानी pari thi.
#- On 11 Feb It is My Class Presintaion So Must Know.
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
