---
layout: default
title: "Redeem Center"
permalink: /redeem/
---

<div class="redeem-page">
  <style>
    .redeem-page {
      color: inherit;
      max-width: 900px;
      margin: 0 auto;
    }

    .redeem-hero {
      padding: 26px;
      border-radius: 22px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.08);
      box-shadow: 0 20px 50px rgba(0, 0, 0, 0.25);
      backdrop-filter: blur(14px);
    }

    .redeem-hero h1 {
      margin-top: 0;
      margin-bottom: 10px;
      font-size: clamp(2rem, 4vw, 3rem);
    }

    .redeem-hero p {
      color: var(--text-muted);
      line-height: 1.7;
      margin-bottom: 0;
    }

    .redeem-box {
      margin-top: 22px;
      display: grid;
      gap: 14px;
    }

    .redeem-row {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
    }

    .redeem-input {
      flex: 1 1 280px;
      padding: 14px 16px;
      border-radius: 14px;
      border: 1px solid rgba(96, 165, 250, 0.22);
      background: rgba(8, 18, 32, 0.82);
      color: #eff6ff;
      font-size: 1rem;
      outline: none;
    }

    .redeem-input:focus {
      border-color: rgba(34, 197, 94, 0.55);
      box-shadow: 0 0 0 3px rgba(56, 189, 248, 0.12);
    }

    .redeem-btn {
      border: none;
      border-radius: 14px;
      padding: 14px 18px;
      font-weight: 700;
      cursor: pointer;
      background: linear-gradient(90deg, var(--accent), var(--accent2));
      color: #04111d;
    }

    .redeem-result {
      min-height: 52px;
      padding: 16px;
      border-radius: 16px;
      background: rgba(255, 255, 255, 0.04);
      border: 1px solid rgba(255, 255, 255, 0.08);
      color: var(--text-main);
    }

    .code-list {
      margin-top: 22px;
      display: grid;
      gap: 12px;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    }

    .code-card {
      padding: 16px;
      border-radius: 16px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.07);
    }

    .code-card strong { display: block; margin-bottom: 6px; }
    .code-card span { color: var(--text-muted); font-size: 0.95rem; }
  </style>

  <section class="redeem-hero">
    <h1>🎁 Redeem Center</h1>
    <p>Enter a promo code to unlock a reward. Some codes are visible here, and some may be hidden somewhere else on the site.</p>

    <div class="redeem-box">
      <div class="redeem-row">
        <input id="redeemCode" class="redeem-input" type="text" placeholder="Enter code here" autocomplete="off" spellcheck="false" />
        <button class="redeem-btn" id="redeemBtn" type="button">Redeem</button>
      </div>
      <div class="redeem-result" id="redeemResult">Try a code below.</div>
    </div>
  </section>

  <section class="code-list" aria-label="Promo codes">
    <div class="code-card"><strong>YJ1108</strong><span>Unlocks a little surprise message.</span></div>
    <div class="code-card"><strong>BLUEGREEN</strong><span>Gives access to a colour-themed bonus.</span></div>
    <div class="code-card"><strong>ALOOYJ</strong><span>Points to the potato trail.</span></div>
    <div class="code-card"><strong>VAULTKEY</strong><span>Hints toward the secret vault.</span></div>
  </section>

  <script>
    (function() {
      const codes = {
        "YJ1108": "Code accepted! You unlocked a small hidden surprise.",
        "BLUEGREEN": "Nice! The blue-green theme is active.",
        "ALOOYJ": "Correct! Follow the Aloo trail next.",
        "VAULTKEY": "You found a vault hint. Keep exploring.",
        "YUVANSH": "Welcome, explorer. Secret paths are open.",
        "1108": "Special code accepted. More clues await.",
      };

      const input = document.getElementById('redeemCode');
      const button = document.getElementById('redeemBtn');
      const result = document.getElementById('redeemResult');

      function redeem() {
        const value = input.value.trim().toUpperCase();
        if (!value) {
          result.textContent = 'Please enter a code first.';
          return;
        }
        result.textContent = codes[value] || 'That code did not work. Try another one.';
      }

      button.addEventListener('click', redeem);
      input.addEventListener('keydown', function(e) {
        if (e.key === 'Enter') redeem();
      });
    })();
  </script>
</div>