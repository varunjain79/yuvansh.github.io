---
layout: default
title: "Home"
---

<style>

/* ---------- NIGHT BACKGROUND ---------- */

body {
  background: radial-gradient(circle at 20% 10%, #111827, #020617 70%);
  color: #e5e7eb;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
}


/* ---------- HERO ---------- */

.hero-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  padding: 40px 20px;
  align-items: center;
}

.hero-title {
  font-size: 48px;
  font-weight: 800;
  line-height: 1.1;
  margin: 15px 0;
}

.gradient-text {
  background: linear-gradient(90deg, #60a5fa, #a78bfa, #34d399);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero-sub {
  font-size: 18px;
  opacity: 0.8;
  max-width: 520px;
}

.hero-badge {
  display: inline-block;
  padding: 6px 12px;
  background: rgba(255,255,255,0.08);
  border-radius: 999px;
  font-size: 13px;
  margin-bottom: 10px;
}


/* ---------- PILLS ---------- */

.hero-tags {
  margin-top: 20px;
}

.pill {
  display: inline-block;
  margin: 5px;
  padding: 6px 12px;
  border-radius: 999px;
  background: rgba(96,165,250,0.15);
  border: 1px solid rgba(96,165,250,0.3);
  font-size: 13px;
}


/* ---------- GLASS CARD ---------- */

.glass-card {
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(16px);
  border-radius: 20px;
  padding: 25px;
  border: 1px solid rgba(255,255,255,0.08);
  box-shadow: 0 20px 40px rgba(0,0,0,0.4);
}


/* ---------- HERO CHIPS ---------- */

.hero-visual-title {
  font-weight: 600;
  margin-bottom: 10px;
}

.hero-visual-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
  margin-top: 15px;
}

.hero-chip {
  background: rgba(255,255,255,0.05);
  padding: 12px;
  border-radius: 12px;
}

.hero-chip-label {
  font-size: 12px;
  opacity: 0.6;
}

.hero-chip-value {
  font-size: 15px;
  font-weight: 600;
}


/* ---------- PHOTOS ---------- */

.hero-photo-strip {
  display: flex;
  gap: 10px;
  margin-top: 20px;
}

.hero-photo-strip img {
  width: 70px;
  height: 70px;
  object-fit: cover;
  border-radius: 12px;
  border: 2px solid rgba(255,255,255,0.1);
}


/* ---------- POSTS ---------- */

.section-card {
  margin-top: 50px;
  padding: 30px;
  background: rgba(255,255,255,0.04);
  border-radius: 20px;
  border: 1px solid rgba(255,255,255,0.07);
}

.section-header h2 {
  margin: 0;
}

.post-card-link {
  text-decoration: none;
  color: inherit;
}

.post-card {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 18px;
  margin-top: 12px;
  border-radius: 14px;
  background: rgba(255,255,255,0.04);
  transition: 0.25s;
}

.post-card:hover {
  transform: translateY(-3px);
  background: rgba(96,165,250,0.1);
}

.post-title {
  font-weight: 600;
  margin: 0;
}

.post-meta {
  font-size: 13px;
  opacity: 0.6;
  margin: 4px 0 0 0;
}


/* ---------- MOBILE ---------- */

@media (max-width: 900px) {
  .hero-wrapper {
    grid-template-columns: 1fr;
  }

  .hero-title {
    font-size: 36px;
  }
}

</style>



<div class="hero-wrapper">

  <div class="hero-left">
    <div class="hero-badge">Yuvansh · Age 6 · New-gen learner</div>

    <h1 class="hero-title">
      Welcome to my <span class="gradient-text">Digital lab</span>.
    </h1>

    <p class="hero-sub">
      I explore school, coding, AI, YouTube, LEGO and random science ideas.
      This website is my notebook for everything I discover and build.
    </p>

    <div class="hero-tags">
      <span class="pill">🧮 School learning</span>
      <span class="pill">🕹️ Projects & games</span>
      <span class="pill">🤖 Custom AIs</span>
      <span class="pill">📷 Photos & videos</span>
    </div>

    <div class="hero-stats">
      New posts whenever I discover something cool ✨
    </div>
  </div>


  <div class="hero-right">

    <div class="glass-card">

      <div class="hero-visual-title">Today in my world</div>

      <div class="hero-visual-grid">

        <div class="hero-chip">
          <div class="hero-chip-label">Current mood</div>
          <div class="hero-chip-value">Thinking of designs 🎨</div>
        </div>

        <div class="hero-chip">
          <div class="hero-chip-label">Today’s focus</div>
          <div class="hero-chip-value">Math 🧮</div>
        </div>

        <div class="hero-chip">
          <div class="hero-chip-label">Working on</div>
          <div class="hero-chip-value">This website 💻</div>
        </div>

        <div class="hero-chip">
          <div class="hero-chip-label">Next idea</div>
          <div class="hero-chip-value">My language (YJ) 🚀</div>
        </div>

      </div>

      <div class="hero-photo-strip">
        <img src="{{ '/assets/profile/yuvansh-hero-1.jpg' | relative_url }}" alt="Yuvansh photo 1">
        <img src="{{ '/assets/profile/yuvansh-hero-2.jpg' | relative_url }}" alt="Yuvansh photo 2">
        <img src="{{ '/assets/profile/yuvansh-hero-3.jpg' | relative_url }}" alt="Yuvansh photo 3">
      </div>

    </div>

  </div>

</div>



<div class="section-card">

  <div class="section-header">
    <h2>Latest entries</h2>
    <span>New things I learned and built</span>
  </div>

  <div class="post-list">
    {% assign latest_posts = site.posts | sort: "date" | reverse | slice: 0, 6 %}
    {% for post in latest_posts %}
      {% assign cat = post.category | default: "updates" %}
      {% capture cat_class %}cat-{{ cat }}{% endcapture %}

      <a href="{{ post.url | relative_url }}" class="post-card-link">

        <div class="post-card">

          <div class="post-main">
            <p class="post-title">{{ post.title }}</p>
            <p class="post-meta">
              {{ post.date | date: "%b %d, %Y" }} · {{ cat | capitalize }}
            </p>
          </div>

          <span class="category-badge {{ cat_class }}">
            <span class="badge-dot"></span>
            {{ cat | capitalize }}
          </span>

        </div>

      </a>

    {% endfor %}
  </div>

</div>
