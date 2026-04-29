---
layout: default
title: 3D Plant Modeling & Light-Environment Simulation
---

<section class="page-hero">
  <div class="container page-hero__inner">
    <div class="page-hero__text">
      <p class="page-hero__label">Track 1 · Decoding Complexity</p>
      <h1 class="page-hero__title">3D Plant Modeling &<br>Light-Environment<br>Simulation</h1>
      <p class="page-hero__desc">Beyond observation — computing light at canopy scale</p>
    </div>
    <div class="page-hero__visual">
      <svg viewBox="0 0 340 280" fill="none" xmlns="http://www.w3.org/2000/svg" class="hero__diagram">
        <!-- Frame -->
        <rect x="20" y="10" width="300" height="260" rx="12" fill="rgba(255,255,255,.04)" stroke="rgba(255,255,255,.12)" stroke-width="1"/>

        <!-- ── Light Sources ── -->
        <text x="100" y="36" text-anchor="middle" fill="rgba(255,255,255,.6)" font-size="9" font-weight="600">Sun</text>
        <text x="170" y="36" text-anchor="middle" fill="rgba(255,255,255,.6)" font-size="9" font-weight="600">LED</text>
        <text x="240" y="36" text-anchor="middle" fill="rgba(255,255,255,.6)" font-size="9" font-weight="600">Etc.</text>
        <!-- Bracket lines -->
        <path d="M100,42 L100,48 L170,48" stroke="rgba(255,255,255,.3)" stroke-width="0.8" fill="none"/>
        <path d="M240,42 L240,48 L170,48" stroke="rgba(255,255,255,.3)" stroke-width="0.8" fill="none"/>
        <line x1="170" y1="42" x2="170" y2="48" stroke="rgba(255,255,255,.3)" stroke-width="0.8"/>
        <line x1="170" y1="48" x2="170" y2="58" stroke="rgba(255,255,255,.3)" stroke-width="0.8"/>

        <!-- ── Light Box ── -->
        <rect x="130" y="58" width="80" height="24" rx="4" fill="rgba(30,80,120,.7)" stroke="rgba(80,160,220,.5)" stroke-width="1"/>
        <text x="170" y="74" text-anchor="middle" fill="rgba(255,255,255,.9)" font-size="11" font-weight="700">Light</text>

        <!-- ── Photon paths ── -->
        <path d="M170,82 L170,115 L260,88" stroke="rgba(60,90,140,.55)" stroke-width="1" fill="none" stroke-linejoin="round"/>
        <polygon points="258,94 264,85 254,87" fill="rgba(60,90,140,.55)"/>
        <path d="M170,82 L162,115 L154,162 L265,135" stroke="rgba(60,90,140,.45)" stroke-width="1" fill="none" stroke-linejoin="round"/>
        <polygon points="263,141 269,132 259,134" fill="rgba(60,90,140,.45)"/>
        <path d="M170,82 L158,115 L146,162 L142,205" stroke="rgba(60,90,140,.4)" stroke-width="1" fill="none" stroke-linejoin="round"/>
        <polygon points="137,201 142,211 147,201" fill="rgba(60,90,140,.4)"/>

        <!-- ── Top Layer ── -->
        <ellipse cx="170" cy="115" rx="60" ry="12" fill="rgba(100,190,60,.35)" stroke="rgba(90,180,50,.6)" stroke-width="1"/>
        <text x="170" y="119" text-anchor="middle" fill="rgba(255,255,255,.7)" font-size="9" font-weight="600">Top</text>

        <!-- ── Mid Layer ── -->
        <ellipse cx="170" cy="162" rx="75" ry="14" fill="rgba(100,190,60,.3)" stroke="rgba(90,180,50,.5)" stroke-width="1"/>
        <text x="170" y="166" text-anchor="middle" fill="rgba(255,255,255,.7)" font-size="9" font-weight="600">Mid</text>

        <!-- ── Bot Layer ── -->
        <ellipse cx="170" cy="205" rx="90" ry="16" fill="rgba(100,190,60,.25)" stroke="rgba(90,180,50,.4)" stroke-width="1"/>
        <text x="170" y="209" text-anchor="middle" fill="rgba(255,255,255,.7)" font-size="9" font-weight="600">Bot</text>

        <!-- Label -->
        <text x="170" y="248" text-anchor="middle" fill="rgba(255,255,255,.5)" font-size="12" font-family="monospace" font-weight="600">Light Interception &amp; Photosynthesis</text>

        <!-- Animated photons -->
        <circle r="2.5" fill="rgba(255,220,80,.8)" opacity="0">
          <animateMotion dur="3s" repeatCount="indefinite" path="M170,82 L170,115 L260,88"/>
          <animate attributeName="opacity" begin="0s" to="1" dur="0.01s" fill="freeze"/>
        </circle>
        <circle r="2.5" fill="rgba(255,220,80,.65)" opacity="0">
          <animateMotion dur="4s" begin="0.8s" repeatCount="indefinite" path="M170,82 L162,115 L154,162 L265,135"/>
          <animate attributeName="opacity" begin="0.8s" to="1" dur="0.01s" fill="freeze"/>
        </circle>
        <circle r="2.5" fill="rgba(255,220,80,.5)" opacity="0">
          <animateMotion dur="4.5s" begin="1.6s" repeatCount="indefinite" path="M170,82 L158,115 L146,162 L142,205"/>
          <animate attributeName="opacity" begin="1.6s" to="1" dur="0.01s" fill="freeze"/>
        </circle>
      </svg>
    </div>
  </div>
</section>

<!-- ───── Overview (split) ───── -->
<section class="rd-overview-split" style="grid-template-columns:3fr 5fr">
  <div class="rd-overview-split__text">
    <h2 class="rd-overview-split__heading">Computing light at the canopy scale</h2>
    <p class="rd-overview-split__desc">Cultivation systems are designed without ever measuring what each leaf actually receives. We make the canopy's light environment computable — so light, photosynthesis, and energy become things we can analyze rather than estimate.</p>
  </div>
  <div class="rd-overview-split__visual" style="background:transparent;padding:16px">
    <video autoplay loop muted playsinline style="border-radius:12px;width:100%;display:block;">
      <source src="{{ '/assets/img/research/surface-curvature.mp4' | relative_url }}" type="video/mp4">
    </video>
  </div>
</section>

<!-- ───── Pipeline (3-card layout) ───── -->
<section class="rd-band rd-band--dark">
  <div class="rd-band__inner">
    <h2>Pipeline</h2>
    <p class="rd-band__subtitle">From physical crops to virtual light analysis — estimating supplemental lighting requirements and optimizing cultivation strategies</p>

    <div class="rd-topics-grid rd-topics-grid--pipeline">
      <div class="rd-topics-grid__card">
        <img src="{{ '/assets/img/research/3d-scanning.png' | relative_url }}" alt="3D scanning of plant with handheld scanner">
        <div class="rd-topics-grid__caption">
          <h3>3D Scanning</h3>
          <div class="rd-topics-grid__keywords">
            <span class="badge">Handheld Scanner</span>
            <span class="badge">Crop Architecture</span>
            <span class="badge">Multi-stage Capture</span>
          </div>
        </div>
        <p class="rd-topics-grid__desc">Reconstruct crop architecture at multiple growth stages using handheld 3D scanners</p>
      </div>

      <div class="rd-topics-grid__arrow">
        <svg viewBox="0 0 24 24" fill="none"><path d="M5 12h14m0 0l-5-5m5 5l-5 5" stroke="rgba(255,255,255,.5)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </div>

      <div class="rd-topics-grid__card">
        <img src="{{ '/assets/img/research/cucumber-3d-scan.png' | relative_url }}" alt="3D scanned cucumber plant mesh in Blender">
        <div class="rd-topics-grid__caption">
          <h3>3D Mesh</h3>
          <div class="rd-topics-grid__keywords">
            <span class="badge">Mesh Reconstruction</span>
            <span class="badge">Canopy Architecture</span>
            <span class="badge">Growth Archive</span>
          </div>
        </div>
        <p class="rd-topics-grid__desc">Accumulate scanned plant models across different growth stages for comparative analysis</p>
      </div>

      <div class="rd-topics-grid__arrow">
        <svg viewBox="0 0 24 24" fill="none"><path d="M5 12h14m0 0l-5-5m5 5l-5 5" stroke="rgba(255,255,255,.5)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </div>

      <div class="rd-topics-grid__card">
        <img src="{{ '/assets/img/research/scan-view-2.png' | relative_url }}" alt="Ray-tracing simulation in ANSYS" style="transform:scale(1.55);transform-origin:80% 80%">
        <div class="rd-topics-grid__caption">
          <h3>Light Simulation</h3>
          <div class="rd-topics-grid__keywords">
            <span class="badge">Ray Tracing</span>
            <span class="badge">Light Interception</span>
            <span class="badge">Photosynthesis</span>
          </div>
        </div>
        <p class="rd-topics-grid__desc">Simulate light interception and estimate photosynthesis to optimize supplemental lighting and energy costs</p>
      </div>
    </div>
  </div>
</section>
