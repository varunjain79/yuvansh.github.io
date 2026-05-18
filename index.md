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
 <script>
(function() {
  const searchIndex = [
    {% for post in site.posts %}
    {
      title: {{ post.title | jsonify }},
      url: {{ post.url | relative_url | jsonify }},
      content: {{ post.content | strip_html | strip_newlines | truncatewords: 300 | jsonify }},
      date: {{ post.date | date: "%b %d, %Y" | jsonify }},
      type: "post",
      categories: {{ post.categories | jsonify }}
    }{% unless forloop.last %},{% endunless %}
    {% endfor %}
    {% if site.posts.size > 0 and site.pages.size > 0 %},{% endif %}
    {% for page in site.pages %}
    {% if page.title and page.url != "/" and page.url != "/404.html" %}
    {
      title: {{ page.title | jsonify }},
      url: {{ page.url | relative_url | jsonify }},
      content: {{ page.content | strip_html | strip_newlines | truncatewords: 300 | jsonify }},
      date: "",
      type: "page",
      categories: []
    }{% unless forloop.last %},{% endunless %}
    {% endif %}
    {% endfor %}
  ];

  const searchInput = document.getElementById('site-search');
  const searchBtn = document.getElementById('search-btn');
  const searchClear = document.getElementById('search-clear');
  const searchResults = document.getElementById('search-results');
  const searchResultsCard = document.getElementById('search-results-card');
  let debounceTimer;

  function highlightText(text, query) {
    if (!query) return text;
    const escaped = query.replace(/[.*+?^${}()|[\]\\]/g, '\\$&');
    return text.replace(new RegExp('(' + escaped + ')', 'gi'), '<span class="search-result-highlight">$1</span>');
  }

  function getSnippet(content, query, maxLen) {
    maxLen = maxLen || 160;
    if (!query) return content.substring(0, maxLen) + '…';
    const matchIndex = content.toLowerCase().indexOf(query.toLowerCase());
    if (matchIndex === -1) return content.substring(0, maxLen) + '…';
    const start = Math.max(0, matchIndex - 40);
    const end = Math.min(content.length, matchIndex + query.length + maxLen - 40);
    let snippet = '';
    if (start > 0) snippet += '…';
    snippet += content.substring(start, end);
    if (end < content.length) snippet += '…';
    return snippet;
  }

  function performSearch() {
    const query = searchInput.value.trim().toLowerCase();
    searchResultsCard.innerHTML = '';
    if (query.length > 0) { searchClear.classList.add('visible'); } else { searchClear.classList.remove('visible'); searchResults.classList.remove('active'); return; }
    if (query.length < 2) { searchResults.classList.remove('active'); return; }

    const results = searchIndex.map(item => {
      let score = 0;
      const titleLower = item.title.toLowerCase();
      const contentLower = item.content.toLowerCase();
      if (titleLower === query) score += 100;
      if (titleLower.startsWith(query)) score += 50;
      if (titleLower.includes(query)) score += 30;
      if (contentLower.includes(query)) score += 20;
      const occurrences = (contentLower.match(new RegExp(query.replace(/[.*+?^${}()|[\]\\]/g, '\\$&'), 'g')) || []).length;
      score += Math.min(occurrences * 3, 30);
      if (item.categories && item.categories.some(c => c.toLowerCase().includes(query))) score += 15;
      return { ...item, score };
    }).filter(item => item.score > 0).sort((a, b) => b.score - a.score);

    searchResults.classList.add('active');
    if (results.length === 0) {
      const div = document.createElement('div'); div.textContent = searchInput.value.trim();
      searchResultsCard.innerHTML = '<div class="search-no-results"><span>🔍</span>No results found for "' + div.innerHTML + '"</div>';
      return;
    }

    let html = '<div class="search-result-count">' + results.length + ' result' + (results.length === 1 ? '' : 's') + ' found</div>';
    results.forEach(item => {
      const snippet = getSnippet(item.content, searchInput.value.trim());
      const highlightedTitle = highlightText(item.title, searchInput.value.trim());
      const highlightedSnippet = highlightText(snippet, searchInput.value.trim());
      const metaParts = [];
      if (item.type === 'post') metaParts.push('Post'); else metaParts.push('Page');
      if (item.date) metaParts.push(item.date);
      if (item.categories && item.categories.length) metaParts.push(item.categories.join(', '));
      html += '<a href="' + item.url + '" class="search-result-item"><div class="search-result-title">' + highlightedTitle + '</div><div class="search-result-snippet">' + highlightedSnippet + '</div><div class="search-result-meta">' + metaParts.join(' · ') + '</div></a>';
    });
    searchResultsCard.innerHTML = html;
  }

  searchInput.addEventListener('input', function() {
    clearTimeout(debounceTimer);
    debounceTimer = setTimeout(performSearch, 200);
    if (this.value.length > 0) { searchClear.classList.add('visible'); } else { searchClear.classList.remove('visible'); searchResults.classList.remove('active'); }
  });
  searchInput.addEventListener('keydown', function(e) {
    if (e.key === 'Enter') { e.preventDefault(); clearTimeout(debounceTimer); performSearch(); }
    if (e.key === 'Escape') { searchInput.value = ''; searchClear.classList.remove('visible'); searchResults.classList.remove('active'); searchInput.blur(); }
  });
  searchBtn.addEventListener('click', function() { clearTimeout(debounceTimer); performSearch(); });
  searchClear.addEventListener('click', function() { searchInput.value = ''; searchClear.classList.remove('visible'); searchResults.classList.remove('active'); searchInput.focus(); });
  document.addEventListener('click', function(e) { if (!document.querySelector('.search-section').contains(e.target)) { searchResults.classList.remove('active'); } });
})();
</script>
  </div>
</div>
