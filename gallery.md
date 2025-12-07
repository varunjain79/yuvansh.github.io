---
layout: default
title: "Gallery"
permalink: /gallery/
---

<div class="card">
  <div class="section-header">
    <h2>Gallery</h2>
    <span>Photos and videos from my adventures.</span>
  </div>
  <p style="font-size:13px; color:var(--text-muted);">
    This is where I keep my favourite pictures and video moments – school, home, trips, experiments, and random fun.
  </p>
</div>

<div class="gallery-grid">
  {% assign items = site.gallery | sort: "date" | reverse %}
  {% for item in items %}
    <a href="{{ item.url | relative_url }}" style="text-decoration:none;">
      <div class="gallery-card">
        <div class="gallery-thumb">
          {% if item.image %}
            <img src="{{ item.image | relative_url }}" alt="{{ item.title }}">
          {% elsif item.video_thumb %}
            <img src="{{ item.video_thumb | relative_url }}" alt="{{ item.title }}">
          {% else %}
            <div style="position:absolute; inset:0; display:flex; align-items:center; justify-content:center; font-size:40px; opacity:0.15;">
              🎥
            </div>
          {% endif %}
        </div>
        <div class="gallery-label">
          <div class="gallery-label-title">{{ item.title }}</div>
          <div class="gallery-label-meta">
            {{ item.date | date: "%b %d, %Y" }}
            {% if item.type %}
              · <span class="chip">
                {% if item.type == "video" %}🎥 Video{% else %}📷 Photo{% endif %}
              </span>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  {% endfor %}
</div>
