---
layout: default
title: "Home"
---

<div class="card">
  <h2>Hi, I'm Yuvansh 👋</h2>
  <p>I am 6 years old. I like computers, robots, AI and making things.</p>
  <p>This site is where I keep track of what I learn and build.</p>
</div>

<div class="card">
  <h3>Latest from my notebook</h3>
  {% assign latest_posts = site.posts | sort: "date" | reverse | slice: 0, 5 %}
  <ul>
    {% for post in latest_posts %}
      <li>
        <a class="post-link" href="{{ post.url | relative_url }}">
          <strong>{{ post.title }}</strong>
        </a>
        <span class="meta"> · {{ post.date | date: "%b %d, %Y" }} · {{ post.category | capitalize }}</span>
      </li>
    {% endfor %}
  </ul>
</div>

<div class="card">
  <h3>Sections</h3>
  <ul>
    <li><a href="{{ '/school/' | relative_url }}">What I Learned at School</a></li>
    <li><a href="{{ '/projects/' | relative_url }}">Projects</a></li>
    <li><a href="{{ '/ai/' | relative_url }}">My Custom AIs</a></li>
    <li><a href="{{ '/youtube/' | relative_url }}">My YouTube Stuff</a></li>
    <li><a href="{{ '/updates/' | relative_url }}">Updates</a></li>
  </ul>
</div>
