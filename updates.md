---
layout: default
title: "Updates"
permalink: /updates/
---

<style>
  .updates-shell {
    position: relative;
    overflow: hidden;
    padding: 10px;
  }

  .updates-hero {
    text-align: center;
    padding: 34px 18px 28px;
    border-radius: 22px;
    border: 1px solid rgba(56, 189, 248, 0.25);
    background: linear-gradient(145deg, rgba(7, 24, 43, 0.94), rgba(10, 34, 54, 0.78));
    box-shadow: inset 0 0 40px rgba(56, 189, 248, 0.04);
  }

  .updates-hero .eyebrow {
    display: inline-block;
    padding: 6px 10px;
    border-radius: 999px;
    font-size: .78rem;
    letter-spacing: .12em;
    text-transform: uppercase;
    color: #86efac;
    border: 1px solid rgba(134, 239, 172, .22);
    background: rgba(34, 197, 94, .08);
  }

  .updates-hero h1 {
    margin: 14px 0 10px;
    font-size: clamp(2rem, 6vw, 4.2rem);
    line-height: 1;
    background: linear-gradient(90deg, #7dd3fc, #86efac, #60a5fa);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
  }

  .updates-hero p {
    max-width: 700px;
    margin: 0 auto;
    color: #a7c0da;
    font-size: 1.05rem;
  }

  .update-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 16px;
    margin-top: 18px;
  }

  .update-card {
    position: relative;
    padding: 22px;
    border-radius: 20px;
    border: 1px solid rgba(96, 165, 250, .2);
    background: rgba(5, 18, 32, .72);
    transition: transform .2s ease, border-color .2s ease, box-shadow .2s ease;
  }

  .update-card:hover {
    transform: translateY(-3px);
    border-color: rgba(56, 189, 248, .45);
    box-shadow: 0 18px 45px rgba(0,0,0,.25);
  }

  .update-card h2 { margin-top: 0; }
  .update-card p { color: #a7c0da; }

  .portal-button, .computer-button, .giveaway-button {
    border: 0;
    border-radius: 12px;
    padding: 11px 15px;
    color: #06121f;
    font-weight: 800;
    cursor: pointer;
    background: linear-gradient(90deg, #7dd3fc, #86efac);
    transition: transform .18s ease, filter .18s ease;
  }

  .portal-button:hover, .computer-button:hover, .giveaway-button:hover {
    transform: translateY(-2px) scale(1.01);
    filter: brightness(1.08);
  }

  .secret-panel {
    display: none;
    margin-top: 16px;
    padding: 18px;
    border-radius: 16px;
    border: 1px solid rgba(134, 239, 172, .25);
    background: rgba(2, 10, 18, .9);
  }

  .secret-panel.visible { display: block; animation: reveal .35s ease; }

  @keyframes reveal {
    from { opacity: 0; transform: translateY(8px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .fake-computer {
    margin-top: 16px;
    border-radius: 16px;
    overflow: hidden;
    border: 1px solid rgba(96, 165, 250, .3);
    background: #030b13;
    font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
  }

  .computer-top {
    padding: 10px 14px;
    color: #a7c0da;
    background: #071522;
    border-bottom: 1px solid rgba(96, 165, 250, .18);
  }

  .computer-body { padding: 18px; }

  .storage {
    height: 13px;
    border-radius: 999px;
    overflow: hidden;
    background: #102235;
    margin: 10px 0 6px;
  }

  .storage span {
    display: block;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, #38bdf8, #22c55e);
  }

  .file-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 8px;
    margin-top: 16px;
  }

  .fake-file {
    padding: 10px;
    border: 1px solid rgba(96, 165, 250, .16);
    border-radius: 10px;
    background: rgba(8, 26, 46, .75);
    color: #cfe5fa;
    cursor: pointer;
  }

  .fake-file:hover { border-color: rgba(56, 189, 248, .45); }

  .giveaway {
    margin-top: 18px;
    padding: 24px;
    border-radius: 20px;
    border: 1px solid rgba(34, 197, 94, .28);
    background: linear-gradient(145deg, rgba(8, 36, 31, .76), rgba(5, 20, 29, .84));
  }

  .giveaway strong { color: #86efac; }

  .tiny-note {
    margin-top: 10px;
    color: #7895ad;
    font-size: .86rem;
  }

  .reality-note {
    margin-top: 18px;
    padding: 14px 16px;
    border-radius: 14px;
    background: rgba(96, 165, 250, .07);
    border: 1px solid rgba(96, 165, 250, .15);
    color: #a7c0da;
    font-size: .9rem;
  }

  @media (max-width: 760px) {
    .update-grid { grid-template-columns: 1fr; }
  }
</style>

<div class="updates-shell">
  <section class="updates-hero">
    <span class="eyebrow">Website Updates</span>
    <h1>Wait... what is this website?</h1>
    <p>This used to be a normal updates page. Then the hidden stuff started escaping. Explore carefully. 🌀</p>
  </section>

  <div class="update-grid">
    <section class="update-card">
      <h2>🌀 Secret Portal</h2>
      <p>It looks like a completely ordinary update. Probably. Definitely don't click the button.</p>
      <button class="portal-button" type="button" onclick="openSecretPortal()">Open the ordinary thing</button>
      <div id="portal" class="secret-panel">
        <h3>PORTAL UNLOCKED</h3>
        <p>You found the first layer. This page is no longer behaving like a normal portfolio.</p>
        <p><strong>Portal status:</strong> active</p>
        <button class="computer-button" type="button" onclick="openComputer()">Enter hidden computer</button>
      </div>
    </section>

    <section class="update-card">
      <h2>🖥️ The Impossible Computer</h2>
      <p>A tiny computer hidden inside the updates page. The storage display is part of the site's fictional mystery.</p>
      <button class="computer-button" type="button" onclick="openComputer()">Boot computer</button>
      <div id="computer" class="secret-panel">
        <div class="fake-computer">
          <div class="computer-top">YJ COMPUTER · SECRET BUILD · ONLINE</div>
          <div class="computer-body">
            <div>Storage: <strong>11 PB / 11 PB</strong></div>
            <div class="storage"><span></span></div>
            <div class="tiny-note">This is a simulated storage display, not actual 11 PB of browser storage.</div>
            <div class="file-grid">
              <div class="fake-file" onclick="fileMessage('PROJECT_INFINITY')">📁 PROJECT_INFINITY</div>
              <div class="fake-file" onclick="fileMessage('SECRET_ARCHIVE')">📁 SECRET_ARCHIVE</div>
              <div class="fake-file" onclick="fileMessage('FUTURE_BUILD')">🧪 FUTURE_BUILD</div>
              <div class="fake-file" onclick="fileMessage('UNKNOWN')">❓ UNKNOWN</div>
            </div>
            <div id="file-output" class="secret-panel"></div>
          </div>
        </div>
      </div>
    </section>
  </div>

  <section class="giveaway">
    <h2>🎁 Limited-Time Free Website Giveaway</h2>
    <p><strong>For young people who want to learn coding.</strong></p>
    <p>I'm opening a limited-time opportunity to help selected young coders get a website and start building on the web.</p>
    <p>More details and eligibility information will be announced here. No passwords, payment details, or unnecessary private information are needed to explore this page.</p>
    <button class="giveaway-button" type="button" onclick="showGiveaway()">Show giveaway info</button>
    <div id="giveaway-info" class="secret-panel">
      <h3>Giveaway status: LIMITED TIME</h3>
      <p>Applications are not open from this button yet. Check this page for the official opening details and deadline.</p>
      <p class="tiny-note">Because this is for young people, participation should use a parent/guardian or another appropriate adult where required.</p>
    </div>
  </section>

  <div class="reality-note">
    <strong>Layer 5:</strong> Some projects shown by the hidden computer can be fictional or future concepts. If you find one that doesn't exist, that's the joke. 😄
  </div>
</div>

<script>
  function reveal(id) {
    document.getElementById(id).classList.add('visible');
  }

  function openSecretPortal() {
    reveal('portal');
  }

  function openComputer() {
    reveal('computer');
    document.getElementById('computer').scrollIntoView({ behavior: 'smooth', block: 'center' });
  }

  function showGiveaway() {
    reveal('giveaway-info');
  }

  function fileMessage(name) {
    const output = document.getElementById('file-output');
    output.classList.add('visible');
    if (name === 'PROJECT_INFINITY') {
      output.innerHTML = '<strong>PROJECT_INFINITY</strong><br>Status: does not exist.<br>Reason: you found a fictional project. 😂';
    } else if (name === 'SECRET_ARCHIVE') {
      output.innerHTML = '<strong>SECRET_ARCHIVE</strong><br>Access granted.<br>Contents: more questions than answers.';
    } else if (name === 'FUTURE_BUILD') {
      output.innerHTML = '<strong>FUTURE_BUILD</strong><br>Status: someday, maybe.<br>Last modified: apparently the future.';
    } else {
      output.innerHTML = '<strong>UNKNOWN</strong><br>Error 404: even the computer doesn't know what this is.';
    }
  }
</script>

## Older Updates

{% assign items = site.posts | where: "category", "updates" | sort: "date" | reverse %}
{% for post in items %}
<a class="post-link" href="{{ post.url | relative_url }}">
  <div class="card">
    <h3>{{ post.title }}</h3>
    <div class="meta">{{ post.date | date: "%B %d, %Y" }}</div>
    <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
  </div>
</a>
{% endfor %}
