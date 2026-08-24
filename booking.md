---
layout: default
title: "Booking"
permalink: /booking/
---

<style>

.booking-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 80px 20px;
}

.booking-card {
  max-width: 600px;
  width: 100%;
  text-align: center;
  padding: 40px;
  border-radius: 20px;
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(16px);
  border: 1px solid rgba(255,255,255,0.08);
}

.booking-title {
  font-size: 32px;
  font-weight: 700;
}

.booking-sub {
  opacity: 0.7;
  margin: 15px 0 30px;
}

.booking-btn {
  display: inline-block;
  padding: 14px 22px;
  border-radius: 12px;
  text-decoration: none;
  font-weight: 600;
  background: #60a5fa;
  color: white;
  transition: 0.2s;
}

.booking-btn:hover {
  transform: translateY(-2px);
  background: #3b82f6;
}

</style>

<div class="booking-wrapper">

  <div class="booking-card">

    <h1 class="booking-title">Book a Call</h1>

    <p class="booking-sub">
      Schedule a 1 hoor session with me.
    </p>

    <a href="https://calendly.com/yuvanshvjain/yuvansh-meet" target="_blank" class="booking-btn">
      Book Now
    </a>

  </div>

</div>
