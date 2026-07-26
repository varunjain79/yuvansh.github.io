---
layout: default
title: "Reviews"
permalink: /reviews/
---

<div class="reviews-page">
  <style>
    .reviews-page {
      display: grid;
      gap: 18px;
    }

    .reviews-header {
      padding: 24px;
      border-radius: 22px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.08);
      box-shadow: 0 20px 50px rgba(0, 0, 0, 0.25);
      backdrop-filter: blur(14px);
    }

    .reviews-header h1 {
      margin: 0 0 10px;
      font-size: clamp(2rem, 4vw, 3rem);
    }

    .reviews-header p {
      margin: 0;
      color: var(--text-muted);
      line-height: 1.7;
    }

    .review-grid {
      display: grid;
      gap: 16px;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    }

    .review-card {
      padding: 18px;
      border-radius: 18px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.08);
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.2);
    }

    .review-stars {
      color: #86efac;
      font-size: 1.1rem;
      margin-bottom: 8px;
      letter-spacing: 0.08em;
    }

    .review-card h2 {
      margin: 0 0 8px;
      font-size: 1.1rem;
    }

    .review-card p {
      margin: 0;
      color: var(--text-muted);
      line-height: 1.6;
    }

    .review-meta {
      margin-top: 12px;
      font-size: 0.9rem;
      color: #7dd3fc;
    }
  </style>

  <section class="reviews-header">
    <h1>⭐ Reviews</h1>
    <p>People can share what they think about the site, projects, or anything else you want to highlight here.</p>
  </section>

  <section class="review-grid">
    <article class="review-card">
      <div class="review-stars">★★★★★</div>
      <h2>Fast and fun</h2>
      <p>The website feels lively, easy to explore, and full of surprises. The secret pages are a great touch.</p>
      <div class="review-meta">— Example visitor</div>
    </article>

    <article class="review-card">
      <div class="review-stars">★★★★★</div>
      <h2>Really creative</h2>
      <p>I liked the blue-and-green theme and the playful design style. It feels unique and personal.</p>
      <div class="review-meta">— Example visitor</div>
    </article>

    <article class="review-card">
      <div class="review-stars">★★★★☆</div>
      <h2>Lots to discover</h2>
      <p>The hidden pages and puzzle-style features make it interesting to keep coming back and testing things.</p>
      <div class="review-meta">— Example visitor</div>
    </article>
  </section>
</div>