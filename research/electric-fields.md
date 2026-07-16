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
        <defs>
          <radialGradient id="ef-hero-glow" cx="50%" cy="55%" r="50%">
            <stop offset="0%" stop-color="rgba(120,210,120,.40)"/>
            <stop offset="100%" stop-color="rgba(120,210,120,0)"/>
          </radialGradient>
        </defs>

        <!-- Frame -->
        <rect x="20" y="10" width="320" height="260" rx="12" fill="rgba(255,255,255,.04)" stroke="rgba(255,255,255,.12)" stroke-width="1"/>

        <!-- Energy glow behind the plant (breathing) -->
        <circle cx="180" cy="162" r="52" fill="url(#ef-hero-glow)">
          <animate attributeName="r" values="46;60;46" dur="4.5s" repeatCount="indefinite"/>
          <animate attributeName="opacity" values=".55;1;.55" dur="4.5s" repeatCount="indefinite"/>
        </circle>

        <!-- Electrode plates -->
        <rect x="44" y="68" width="7" height="146" rx="3" fill="rgba(255,180,100,.9)"/>
        <rect x="309" y="68" width="7" height="146" rx="3" fill="rgba(140,210,235,.95)"/>
        <text x="47" y="58" text-anchor="middle" fill="rgba(255,180,100,.95)" font-size="18" font-weight="700">+</text>
        <text x="312" y="58" text-anchor="middle" fill="rgba(140,210,235,1)" font-size="18" font-weight="700">−</text>

        <!-- Uniform field lines (dashed, pulsing) -->
        <g stroke-dasharray="4 5" stroke-width="1" fill="none" stroke="rgba(140,210,235,.5)">
          <line x1="51" y1="90"  x2="309" y2="90"><animate attributeName="opacity" values=".22;.55;.22" dur="3s" begin="0s"    repeatCount="indefinite"/></line>
          <line x1="51" y1="124" x2="309" y2="124"><animate attributeName="opacity" values=".3;.7;.3"    dur="3s" begin="-0.6s" repeatCount="indefinite"/></line>
          <line x1="51" y1="158" x2="309" y2="158"><animate attributeName="opacity" values=".3;.7;.3"    dur="3s" begin="-1.2s" repeatCount="indefinite"/></line>
          <line x1="51" y1="192" x2="309" y2="192"><animate attributeName="opacity" values=".3;.7;.3"    dur="3s" begin="-1.8s" repeatCount="indefinite"/></line>
          <line x1="51" y1="214" x2="309" y2="214"><animate attributeName="opacity" values=".22;.55;.22" dur="3s" begin="-2.4s" repeatCount="indefinite"/></line>
        </g>

        <!-- Electrons drifting + → − (negative begin = no start flash) -->
        <g fill="rgba(185,232,255,.95)">
          <circle r="2.6"><animateMotion dur="3s"   begin="0s"    repeatCount="indefinite" path="M51,90 L309,90"/></circle>
          <circle r="2.6"><animateMotion dur="3s"   begin="-1.5s" repeatCount="indefinite" path="M51,90 L309,90"/></circle>
          <circle r="2.6"><animateMotion dur="2.6s" begin="-0.6s" repeatCount="indefinite" path="M51,124 L309,124"/></circle>
          <circle r="2.6"><animateMotion dur="2.6s" begin="-1.9s" repeatCount="indefinite" path="M51,124 L309,124"/></circle>
          <circle r="2.6"><animateMotion dur="2.8s" begin="-1s"   repeatCount="indefinite" path="M51,192 L309,192"/></circle>
          <circle r="2.6"><animateMotion dur="3.2s" begin="-0.4s" repeatCount="indefinite" path="M51,214 L309,214"/></circle>
        </g>

        <!-- Plant in the middle (gentle sway) -->
        <g>
          <animateTransform attributeName="transform" type="rotate" values="-1.6 180 216;1.6 180 216;-1.6 180 216" dur="6s" repeatCount="indefinite"/>
          <line x1="180" y1="216" x2="180" y2="112" stroke="rgba(120,210,120,.85)" stroke-width="2.5" stroke-linecap="round"/>
          <path d="M180,182 Q156,168 138,175 Q164,150 180,182Z" fill="rgba(100,190,90,.5)" stroke="rgba(100,200,90,.85)" stroke-width="1"/>
          <path d="M180,182 Q204,168 222,175 Q196,150 180,182Z" fill="rgba(100,190,90,.5)" stroke="rgba(100,200,90,.85)" stroke-width="1"/>
          <path d="M180,150 Q156,136 138,143 Q164,118 180,150Z" fill="rgba(100,190,90,.45)" stroke="rgba(100,200,90,.75)" stroke-width="1"/>
          <path d="M180,150 Q204,136 222,143 Q196,118 180,150Z" fill="rgba(100,190,90,.45)" stroke="rgba(100,200,90,.75)" stroke-width="1"/>
          <path d="M180,116 Q170,110 165,101 Q177,94 180,116 Q183,94 195,101 Q190,110 180,116Z" fill="rgba(100,190,90,.55)" stroke="rgba(100,200,90,.85)" stroke-width="1"/>
        </g>

        <!-- Label -->
        <text x="180" y="252" text-anchor="middle" fill="rgba(255,255,255,.55)" font-size="11" font-family="monospace" font-weight="600">field × electron flow × energy</text>
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
    <img src="{{ '/assets/img/research/electric-field-overview.png' | relative_url }}" alt="Exploring electric fields as a new conceptual angle on plant energy economy — traditional photosynthesis and respiration pathways, uniform electric field application, and the unknown growth mechanism" class="rd-overview-split__illustration" style="border-radius:12px;max-width:100%;max-height:none">
  </div>
</section>

<!-- ───── Research Topics (2-card layout) ───── -->
<section class="rd-band rd-band--dark">
  <div class="rd-band__inner">
    <h2>Research Topics</h2>
    <p class="rd-band__subtitle">From the mechanism of how plants sense an external electric field, to the energy economy that runs every cell — two angles on a single frontier.</p>

    <div class="rd-topics-grid rd-topics-grid--2col rd-topics-grid--light">
      <div class="rd-topics-grid__card">
        <img src="{{ '/assets/img/research/ef-growth.png' | relative_url }}" alt="Growth response to electric field — control (CT) vs electric-field (EF) plants showing larger leaf area, higher electron transport rate, and greater shoot fresh weight" style="object-fit:contain;object-position:50% 42%;background:#fff">
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
        <img src="{{ '/assets/img/research/ef-photosynthesis.png' | relative_url }}" alt="Photosynthetic electron transport under electric field — light and dark reaction scheme with chlorophyll fluorescence parameters (Fv/Fm, Y(II), ETR, NPQ) comparing control and electric-field treatments" style="object-fit:contain;object-position:50% 35%;background:#fff">
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
