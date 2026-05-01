---
layout: default
title: "Home"
---

<style>

/* ---------- GLOBAL ---------- */

body {
  background: radial-gradient(circle at 30% 20%, #0f172a, #020617 75%);
  color: #e5e7eb;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  letter-spacing: 0.2px;
}


/* ---------- HERO ---------- */

.hero-wrapper {
  display: grid;
  grid-template-columns: 1.2fr 1fr;
  gap: 50px;
  padding: 60px 25px;
  align-items: center;
}

.hero-title {
  font-size: 52px;
  font-weight: 900;
  line-height: 1.05;
  margin: 15px 0;
}

.gradient-text {
  background: linear-gradient(90deg, #60a5fa, #a78bfa, #34d399);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero-sub {
  font-size: 18px;
  opacity: 0.75;
  max-width: 540px;
}

.hero-badge {
  display: inline-block;
  padding: 6px 14px;
  background: rgba(255,255,255,0.08);
  border-radius: 999px;
  font-size: 13px;
  margin-bottom: 10px;
  backdrop-filter: blur(10px);
}


/* ---------- PILLS ---------- */

.hero-tags {
  margin-top: 25px;
}

.pill {
  display: inline-block;
  margin: 6px;
  padding: 7px 14px;
  border-radius: 999px;
  background: rgba(96,165,250,0.12);
  border: 1px solid rgba(96,165,250,0.25);
  font-size: 13px;
  transition: 0.2s;
}

.pill:hover {
  transform: scale(1.05);
  background: rgba(96,165,250,0.2);
}


/* ---------- GLASS CARD ---------- */

.glass-card {
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(18px);
  border-radius: 22px;
  padding: 28px;
  border: 1px solid rgba(255,255,255,0.08);
  box-shadow: 0 25px 50px rgba(0,0,0,0.5);
  transition: 0.3s;
}

.glass-card:hover {
  transform: translateY(-5px);
}


/* ---------- HERO CHIPS ---------- */

.hero-visual-title {
  font-weight: 600;
  margin-bottom: 12px;
}

.hero-visual-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 14px;
  margin-top: 15px;
}

.hero-chip {
  background: rgba(255,255,255,0.04);
  padding: 14px;
  border-radius: 14px;
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
  gap: 12px;
  margin-top: 20px;
}

.hero-photo-strip img {
  width: 75px;
  height: 75px;
  object-fit: cover;
  border-radius: 14px;
  border: 2px solid rgba(255,255,255,0.1);
  transition: 0.3s;
}

.hero-photo-strip img:hover {
  transform: scale(1.08);
}


/* ---------- POSTS ---------- */

.section-card {
  margin-top: 60px;
  padding: 35px;
  background: rgba(255,255,255,0.04);
  border-radius: 22px;
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
  padding: 20px;
  margin-top: 14px;
  border-radius: 16px;
  background: rgba(255,255,255,0.04);
  transition: 0.25s;
}

.post-card:hover {
  transform: translateY(-4px);
  background: rgba(96,165,250,0.12);
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


/* ---------- SEARCH BAR ---------- */

.search-section {
  margin: 48px 25px 0;
}

.search-label {
  text-align: center;
  font-size: 13px;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  opacity: 0.5;
  margin-bottom: 14px;
}

.search-wrapper {
  position: relative;
  max-width: 620px;
  margin: 0 auto;
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(96,165,250,0.25);
  border-radius: 999px;
  padding: 6px 10px 6px 20px;
  box-shadow: 0 0 0 0 rgba(96,165,250,0), 0 8px 32px rgba(0,0,0,0.4);
  transition: box-shadow 0.3s, border-color 0.3s;
}

.search-wrapper:focus-within {
  border-color: rgba(96,165,250,0.6);
  box-shadow: 0 0 0 3px rgba(96,165,250,0.15), 0 8px 32px rgba(0,0,0,0.4);
}

/* Override Google CSE styles to blend in */
.gsc-control-cse {
  background: transparent !important;
  border: none !important;
  padding: 0 !important;
  font-family: inherit !important;
}

.gsc-search-box {
  margin: 0 !important;
}

.gsc-search-box-tools .gsc-search-box .gsc-input {
  padding: 0 !important;
}

.gsc-input-box {
  background: transparent !important;
  border: none !important;
  border-radius: 0 !important;
  box-shadow: none !important;
}

.gsc-input-box input.gsc-input {
  background: transparent !important;
  color: #e5e7eb !important;
  font-size: 15px !important;
  padding: 10px 0 !important;
}

.gsc-input-box input.gsc-input::placeholder {
  color: rgba(229,231,235,0.4) !important;
}

.gsc-search-button {
  margin: 0 !important;
}

.gsc-search-button-v2 {
  background: linear-gradient(135deg, #60a5fa, #a78bfa) !important;
  border: none !important;
  border-radius: 999px !important;
  padding: 8px 20px !important;
  cursor: pointer !important;
  transition: opacity 0.2s !important;
}

.gsc-search-button-v2:hover {
  opacity: 0.85 !important;
}

.gsc-search-button-v2 svg {
  fill: #fff !important;
  width: 16px !important;
  height: 16px !important;
}

.gsc-results-wrapper-overlay {
  border-radius: 16px !important;
  background: rgba(15,23,42,0.95) !important;
  backdrop-filter: blur(20px) !important;
  border: 1px solid rgba(255,255,255,0.1) !important;
  box-shadow: 0 20px 60px rgba(0,0,0,0.6) !important;
  margin-top: 8px !important;
}

.gs-result .gs-title, .gs-result .gs-title * {
  color: #60a5fa !important;
}

.gs-result .gs-snippet {
  color: rgba(229,231,235,0.7) !important;
}

.gsc-webResult.gsc-result {
  border-bottom: 1px solid rgba(255,255,255,0.06) !important;
}


/* ---------- MOBILE ---------- */

@media (max-width: 900px) {
  .hero-wrapper {
    grid-template-columns: 1fr;
  }

  .hero-title {
    font-size: 38px;
  }
}

</style>


<div class="hero-wrapper">

  <div class="hero-left">

    <div class="hero-badge">Yuvansh · Creator</div>

    <h1 class="hero-title">
      Welcome to my <span class="gradient-text">Digital Lab</span>
    </h1>

    <p class="hero-sub">
      I build things, explore ideas, and document everything I learn —
      from coding and AI to school and creative experiments.
    </p>

    <div class="hero-tags">
      <span class="pill">🧠 Learning</span>
      <span class="pill">💻 Coding</span>
      <span class="pill">🤖 AI</span>
      <span class="pill">🚀 Projects</span>
    </div>

  </div>


  <div class="hero-right">

    <div class="glass-card">

      <div class="hero-visual-title">Live Status</div>

      <div class="hero-visual-grid">

        <div class="hero-chip">
          <div class="hero-chip-label">Focus</div>
          <div class="hero-chip-value">Building UI 🎨</div>
        </div>

        <div class="hero-chip">
          <div class="hero-chip-label">Learning</div>
          <div class="hero-chip-value">Math 🧮</div>
        </div>

        <div class="hero-chip">
          <div class="hero-chip-label">Project</div>
          <div class="hero-chip-value">This Website 💻</div>
        </div>

        <div class="hero-chip">
          <div class="hero-chip-label">Next</div>
          <div class="hero-chip-value">YJ Language 🚀</div>
        </div>

        <div class="hero-chip">
          <div class="hero-chip-label">...</div>
          <div class="hero-chip-value">More</div>
          <a href="/privacy/" style="font-size:11px; opacity:0.5; display:block; margin-top:4px;">Privacy Policy</a>
        </div>

      </div>

    </div>

  </div>

</div>


<!-- Search Bar -->
<div class="search-section">
  <div class="search-label">Search this site</div>
  <div class="search-wrapper">
    <script async src="https://cse.google.com/cse.js?cx=f2e93a617b5134b79"></script>
    <div class="gcse-search"></div>
  </div>
</div>
