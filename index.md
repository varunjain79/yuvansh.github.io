---
layout: default
title: "Home"
---

<div class="card hero">
  <div>
    <div class="hero-badge">Yuvansh · Age 6 · New-gen learner</div>
    <h1 class="hero-title">Welcome to my lab on the internet.</h1>
    <p class="hero-sub">
      I explore school, code, AI, YouTube, LEGO and random science ideas.
      This website is my notebook for all of it.
    </p>
    <div class="hero-tags">
      <span class="pill">🧮 School learning</span>
      <span class="pill">🕹️ Projects & games</span>
      <span class="pill">🤖 Custom AIs</span>
      <span class="pill">📷 Photos & videos</span>
    </div>
    <div class="hero-stats">
      <span>New posts whenever I discover or build something cool.</span>
    </div>
  </div>
  <div class="hero-visual">
    <div class="hero-orbit"></div>
    <div class="hero-visual-title">Today in my world</div>
    <div class="hero-visual-grid">
      <div class="hero-chip">
        <div class="hero-chip-label">Current mood</div>
        <div class="hero-chip-value">Curious 🔍</div>
      </div>
      <div class="hero-chip">
        <div class="hero-chip-label">Today’s focus</div>
        <div class="hero-chip-value">Math & code</div>
      </div>
      <div class="hero-chip">
        <div class="hero-chip-label">Working on</div>
        <div class="hero-chip-value">Scratch game</div>
      </div>
      <div class="hero-chip">
        <div class="hero-chip-label">Next idea</div>
        <div class="hero-chip-value">New AI buddy</div>
      </div>
    </div>

    <div class="hero-photo-strip">
      <div class="hero-photo">
        <img src="{{ '/assets/profile/yuvansh-hero-1.jpg' | relative_url }}" alt="Yuvansh photo 1">
      </div>
      <div class="hero-photo">
        <img src="{{ '/assets/profile/yuvansh-hero-2.jpg' | relative_url }}" alt="Yuvansh photo 2">
      </div>
      <div class="hero-photo">
        <img src="{{ '/assets/profile/yuvansh-hero-3.jpg' | relative_url }}" alt="Yuvansh photo 3">
      </div>
    </div>
  </div>
</div>

<div class="card">
  <div class="section-header">
    <h2>Latest entries</h2>
    <span>New things I learned and built</span>
  </div>
  <div class="post-list">
    {% assign latest_posts = site.posts | sort: "date" | reverse | slice: 0, 6 %}
    {% for post in latest_posts %}
      {% assign cat = post.category | default: "updates" %}
      {% capture cat_class %}cat-{{ cat }}{% endcapture %}
      <a href="{{ post.url | relative_url }}" style="text-decoration:none;">
        <div class="post-card">
          <div class="post-main">
            <p class="post-title">{{ post.title }}</p>
            <p class="post-meta">
              {{ post.date | date: "%b %d, %Y" }} · {{ cat | capitalize }}
            </p>
          </div>
          <div>
            <span class="category-badge {{ cat_class }}">
              <span class="badge-dot"></span>
              {{ cat | capitalize }}
            </span>
          </div>
        </div>
      </a>
    {% endfor %}
  </div>
</div>
