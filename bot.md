---
layout: default
title: "Bot"
permalink: /bot/
---

<div class="bot-page">
  <style>
    .bot-page {
      color: inherit;
    }

    .bot-page .bot-hero {
      display: grid;
      gap: 24px;
      align-items: center;
    }

    .bot-page .bot-panel {
      background: rgba(255, 255, 255, 0.04);
      border: 1px solid rgba(255, 255, 255, 0.08);
      border-radius: 22px;
      padding: 24px;
      box-shadow: 0 20px 50px rgba(0, 0, 0, 0.25);
      backdrop-filter: blur(14px);
    }

    .bot-page .bot-label {
      display: inline-flex;
      padding: 6px 12px;
      border-radius: 999px;
      background: rgba(56, 189, 248, 0.16);
      color: #dbeafe;
      font-size: 0.85rem;
      margin-bottom: 14px;
    }

    .bot-page .bot-title {
      font-size: clamp(2rem, 4vw, 3.4rem);
      line-height: 1.05;
      margin: 0 0 12px;
    }

    .bot-page .bot-lead {
      color: var(--text-muted);
      font-size: 1.05rem;
      max-width: 62ch;
      margin: 0;
    }

    .bot-page .bot-grid {
      display: grid;
      gap: 18px;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      margin-top: 24px;
    }

    .bot-page .bot-stat {
      padding: 18px;
      border-radius: 18px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.07);
    }

    .bot-page .bot-stat strong {
      display: block;
      font-size: 1.1rem;
      margin-bottom: 6px;
    }

    .bot-page .bot-stat span {
      color: var(--text-muted);
      font-size: 0.95rem;
    }

    .bot-page .bot-section {
      margin-top: 28px;
    }

    .bot-page .bot-section h2 {
      margin: 0 0 14px;
      font-size: 1.5rem;
    }

    .bot-page .bot-section p {
      color: var(--text-muted);
      line-height: 1.7;
    }

    .bot-page .bot-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 22px;
    }

    .bot-page .bot-actions a {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 12px 18px;
      border-radius: 999px;
      text-decoration: none;
      font-weight: 600;
      transition: transform 0.2s ease, opacity 0.2s ease;
    }

    .bot-page .bot-actions a:hover {
      transform: translateY(-2px);
      opacity: 0.92;
    }

    .bot-page .primary-btn {
      background: linear-gradient(90deg, var(--accent), var(--accent2));
      color: #04111d;
    }

    .bot-page .secondary-btn {
      background: rgba(255, 255, 255, 0.06);
      color: #eff6ff;
      border: 1px solid rgba(96, 165, 250, 0.18);
    }
  </style>

  <section class="bot-hero bot-panel">
    <div class="bot-label">WhatsApp Bot</div>
    <h1 class="bot-title">Chat with the bot in a fast, simple, friendly way.</h1>
    <p class="bot-lead">This page is now a proper Jekyll page, so the layout stays consistent with the rest of the site while keeping the bot’s interactive landing content intact.</p>

    <div class="bot-grid">
      <div class="bot-stat"><strong>Instant replies</strong><span>Quick answers with a clean interface.</span></div>
      <div class="bot-stat"><strong>Easy access</strong><span>One tap to open the chat flow.</span></div>
      <div class="bot-stat"><strong>Site-wide style</strong><span>Matches the blue-green Y theme.</span></div>
    </div>

    <div class="bot-actions">
      <a class="primary-btn" href="https://wa.me/917045159459" target="_blank" rel="noreferrer">Start Chatting Now</a>
      <a class="secondary-btn" href="/projects/">See Projects</a>
    </div>
  </section>

  <section class="bot-section bot-panel">
    <h2>What stays the same</h2>
    <p>The bot page still belongs on your website, but now it uses Jekyll front matter and the shared site layout. That means it can be managed like the rest of your pages without losing the special bot feel.</p>
  </section>
</div>