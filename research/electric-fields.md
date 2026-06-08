---
layout: default
title: Electric Field Biology
---

<section class="page-hero">
  <div class="container page-hero__inner">
    <div class="page-hero__text">
      <p class="page-hero__label">Track 1 · Decoding Complexity</p>
      <h1 class="page-hero__title">Electric Field<br>Biology</h1>
      <p class="page-hero__desc">An open frontier in plant–environment research</p>
    </div>
    <div class="page-hero__visual">
      <svg viewBox="0 0 360 280" fill="none" xmlns="http://www.w3.org/2000/svg" class="hero__diagram">
        <!-- Frame -->
        <rect x="20" y="10" width="320" height="260" rx="12" fill="rgba(255,255,255,.04)" stroke="rgba(255,255,255,.12)" stroke-width="1"/>

        <!-- Electric field lines (concentric ellipses, dashed) -->
        <ellipse cx="180" cy="155" rx="125" ry="62" fill="none" stroke="rgba(140,210,235,.18)" stroke-width="1" stroke-dasharray="3 4"/>
        <ellipse cx="180" cy="155" rx="100" ry="50" fill="none" stroke="rgba(140,210,235,.25)" stroke-width="1" stroke-dasharray="3 4"/>
        <ellipse cx="180" cy="155" rx="75" ry="38" fill="none" stroke="rgba(140,210,235,.32)" stroke-width="1" stroke-dasharray="3 4"/>

        <!-- Charge poles (+/-) -->
        <text x="46" y="160" fill="rgba(255,180,100,.75)" font-size="18" font-weight="700">+</text>
        <text x="304" y="161" fill="rgba(140,210,235,.85)" font-size="18" font-weight="700">−</text>

        <!-- Plant in the middle -->
        <line x1="180" y1="215" x2="180" y2="115" stroke="rgba(120,210,120,.7)" stroke-width="2" stroke-linecap="round"/>
        <!-- lower leaves -->
        <path d="M180,180 Q160,168 145,175 Q165,158 180,180Z" fill="rgba(100,190,90,.4)" stroke="rgba(100,200,90,.7)" stroke-width="1"/>
        <path d="M180,180 Q200,168 215,175 Q195,158 180,180Z" fill="rgba(100,190,90,.4)" stroke="rgba(100,200,90,.7)" stroke-width="1"/>
        <!-- mid leaves -->
        <path d="M180,150 Q158,138 142,146 Q164,126 180,150Z" fill="rgba(100,190,90,.35)" stroke="rgba(100,200,90,.6)" stroke-width="1"/>
        <path d="M180,150 Q202,138 218,146 Q196,126 180,150Z" fill="rgba(100,190,90,.35)" stroke="rgba(100,200,90,.6)" stroke-width="1"/>
        <!-- top sprout -->
        <path d="M180,118 Q172,113 168,106 Q177,100 180,118 Q183,100 192,106 Q188,113 180,118Z" fill="rgba(100,190,90,.45)" stroke="rgba(100,200,90,.7)" stroke-width="1"/>

        <!-- Animated electron particle along the middle field line -->
        <circle r="3" fill="rgba(170,225,255,.85)" opacity="0">
          <animateMotion dur="5s" repeatCount="indefinite" path="M280,155 A100,50 0 1,1 80,155 A100,50 0 1,1 280,155"/>
          <animate attributeName="opacity" begin="0s" to="1" dur="0.01s" fill="freeze"/>
        </circle>

        <!-- Label -->
        <text x="180" y="248" text-anchor="middle" fill="rgba(255,255,255,.5)" font-size="12" font-family="monospace" font-weight="600">Field × Energy × Life</text>
      </svg>
    </div>
  </div>
</section>

<!-- ───── Overview (split) ───── -->
<section class="rd-overview-split">
  <div class="rd-overview-split__text">
    <h2 class="rd-overview-split__heading">Questioning the given, exploring the unseen</h2>
    <p class="rd-overview-split__desc">We question the given, and venture into the unexplored, opening a new conceptual angle for plant science. Plants have evolved under physical fields that shape every aspect of their life: light, temperature, water, and gravity. We turn our attention to one long overlooked, the electric field.</p>
    <p class="rd-overview-split__desc">Exposure to electric fields has been reported to enhance plant growth and development, yet the mechanistic basis of these responses remains a black box — an open frontier in plant–environment research that we set out to explore.</p>
  </div>
  <div class="rd-overview-split__visual" style="background:transparent;padding:24px">
    <img src="{{ '/assets/img/research/Electric.png' | relative_url }}" alt="Exploring electric fields as a new conceptual angle on plant energy economy — traditional photosynthesis and respiration pathways, uniform electric field application, and the unknown growth mechanism" class="rd-overview-split__illustration" style="border-radius:12px;max-width:100%;max-height:none">
  </div>
</section>

<!-- ───── Research Topics (2-card layout) ───── -->
<section class="rd-band rd-band--dark">
  <div class="rd-band__inner">
    <h2>Research Topics</h2>
    <p class="rd-band__subtitle">From the mechanism of how plants sense an external electric field, to the energy economy that runs every cell — two angles on a single frontier.</p>

    <div class="rd-topics-grid rd-topics-grid--2col">
      <div class="rd-topics-grid__card">
        <div class="rd-topics-grid__placeholder-img"><span>Photo</span></div>
        <div class="rd-topics-grid__caption">
          <h3>Electric Field Responses</h3>
          <div class="rd-topics-grid__keywords">
            <span class="badge">Bioelectricity</span>
            <span class="badge">Plant Physiology</span>
            <span class="badge">Mechanistic Biology</span>
          </div>
        </div>
        <p class="rd-topics-grid__desc">Decoding the mechanistic basis by which plants sense applied electric fields, and how those signals translate into growth and developmental responses.</p>
      </div>

      <div class="rd-topics-grid__card">
        <div class="rd-topics-grid__placeholder-img"><span>Photo</span></div>
        <div class="rd-topics-grid__caption">
          <h3>Energy Economy of Plants</h3>
          <div class="rd-topics-grid__keywords">
            <span class="badge">Electron Flow</span>
            <span class="badge">Photosynthesis</span>
            <span class="badge">Respiration</span>
          </div>
        </div>
        <p class="rd-topics-grid__desc">At the heart of this exploration lies energy. Photosynthesis, respiration, and growth are the synthesis and conversion of chemical energy carried by the flow of electrons — we probe how that economy is built, balanced, and reshaped under an external physical field.</p>
      </div>
    </div>
  </div>
</section>
