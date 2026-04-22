---
layout: default
title: Energy-Food Nexus & System Optimization
---

<section class="page-hero">
  <div class="container page-hero__inner">
    <div class="page-hero__text">
      <p class="page-hero__label">Track 2 · Engineering Systems</p>
      <h1 class="page-hero__title">Energy-Food<br>Nexus & System<br>Optimization</h1>
      <p class="page-hero__desc">Maximizing the conversion of energy to biomass</p>
    </div>
    <div class="page-hero__visual">
      <svg viewBox="0 0 360 280" fill="none" xmlns="http://www.w3.org/2000/svg" class="hero__diagram">
        <!-- Vertical farm frame -->
        <rect x="100" y="20" width="160" height="220" rx="10" fill="rgba(255,255,255,.04)" stroke="rgba(255,255,255,.12)" stroke-width="1"/>
        <!-- Shelves with LEDs and plants -->
        <g>
          <line x1="115" y1="62" x2="245" y2="62" stroke="rgba(200,120,255,.45)" stroke-width="1.5"/>
          <rect x="112" y="64" width="136" height="32" rx="3" fill="rgba(255,255,255,.04)" stroke="rgba(255,255,255,.08)" stroke-width="0.6"/>
          <circle cx="132" cy="82" r="6" fill="rgba(100,200,100,.35)"/><circle cx="152" cy="80" r="7" fill="rgba(100,200,100,.3)"/>
          <circle cx="172" cy="82" r="6" fill="rgba(100,200,100,.35)"/><circle cx="192" cy="81" r="6.5" fill="rgba(100,200,100,.3)"/>
          <circle cx="212" cy="82" r="6" fill="rgba(100,200,100,.35)"/><circle cx="232" cy="80" r="5.5" fill="rgba(100,200,100,.3)"/>
        </g>
        <g>
          <line x1="115" y1="112" x2="245" y2="112" stroke="rgba(200,120,255,.45)" stroke-width="1.5"/>
          <rect x="112" y="114" width="136" height="32" rx="3" fill="rgba(255,255,255,.04)" stroke="rgba(255,255,255,.08)" stroke-width="0.6"/>
          <circle cx="132" cy="132" r="6" fill="rgba(100,200,100,.35)"/><circle cx="152" cy="130" r="7" fill="rgba(100,200,100,.3)"/>
          <circle cx="172" cy="132" r="6" fill="rgba(100,200,100,.35)"/><circle cx="192" cy="131" r="6.5" fill="rgba(100,200,100,.3)"/>
          <circle cx="212" cy="132" r="6" fill="rgba(100,200,100,.35)"/><circle cx="232" cy="130" r="5.5" fill="rgba(100,200,100,.3)"/>
        </g>
        <g>
          <line x1="115" y1="162" x2="245" y2="162" stroke="rgba(200,120,255,.45)" stroke-width="1.5"/>
          <rect x="112" y="164" width="136" height="32" rx="3" fill="rgba(255,255,255,.04)" stroke="rgba(255,255,255,.08)" stroke-width="0.6"/>
          <circle cx="132" cy="182" r="6" fill="rgba(100,200,100,.35)"/><circle cx="152" cy="180" r="7" fill="rgba(100,200,100,.3)"/>
          <circle cx="172" cy="182" r="6" fill="rgba(100,200,100,.35)"/><circle cx="192" cy="181" r="6.5" fill="rgba(100,200,100,.3)"/>
          <circle cx="212" cy="182" r="6" fill="rgba(100,200,100,.35)"/><circle cx="232" cy="180" r="5.5" fill="rgba(100,200,100,.3)"/>
        </g>
        <!-- Energy input arrow (left) -->
        <path d="M38,130 L96,130" stroke="rgba(255,200,60,.6)" stroke-width="1.5"/>
        <polygon points="94,126 100,130 94,134" fill="rgba(255,200,60,.6)"/>
        <text x="28" y="120" fill="rgba(255,200,60,.7)" font-size="9" font-weight="600">Energy</text>
        <text x="35" y="148" fill="rgba(255,200,60,.4)" font-size="7">Electrical</text>
        <text x="35" y="158" fill="rgba(255,200,60,.4)" font-size="7">Thermal</text>
        <!-- Biomass output arrow (right) -->
        <path d="M264,130 L322,130" stroke="rgba(120,220,120,.6)" stroke-width="1.5"/>
        <polygon points="320,126 326,130 320,134" fill="rgba(120,220,120,.6)"/>
        <text x="278" y="120" fill="rgba(120,220,120,.7)" font-size="9" font-weight="600">Biomass</text>
        <text x="285" y="148" fill="rgba(120,220,120,.4)" font-size="7">Crop Yield</text>
        <!-- Label -->
        <text x="180" y="258" text-anchor="middle" fill="rgba(255,255,255,.5)" font-size="12" font-family="monospace" font-weight="600">Energy-to-Biomass Conversion</text>
        <!-- Animated energy particle -->
        <circle r="2.5" fill="rgba(255,200,60,.8)">
          <animateMotion dur="2.5s" repeatCount="indefinite" path="M38,130 L180,130 L322,130"/>
        </circle>
      </svg>
    </div>
  </div>
</section>

<!-- ───── Overview (split) ───── -->
<section class="rd-overview-split">
  <div class="rd-overview-split__text">
    <h2 class="rd-overview-split__heading">Maximizing energy-to-biomass conversion</h2>
    <p class="rd-overview-split__desc">In high-density production systems such as vertical farms and smart greenhouses, optimizing the conversion of input electrical and thermal energy into crop biomass is critical for sustainable agriculture. Our research focuses on developing "active energy-agriculture systems" by seamlessly integrating plant physiological dynamics with comprehensive facility energy models.</p>
    <div class="research-detail__topics" style="margin-bottom:28px">
      {% for area in site.data.research.tracks[1].areas %}
        {% if area.id == 'energy-food-nexus' %}
          {% for topic in area.topics %}
          <span class="badge research-badge">{{ topic | escape }}</span>
          {% endfor %}
        {% endif %}
      {% endfor %}
    </div>
  </div>
  <div class="rd-overview-split__visual" style="background:transparent;padding:16px">
    <img src="{{ '/assets/img/research/energy-nexus.png' | relative_url }}" alt="Energy-Food Nexus system diagram" style="border-radius:12px;width:100%;display:block;" loading="lazy">
  </div>
</section>

<!-- ───── Research Topics (2-card layout) ───── -->
<section class="rd-band rd-band--dark">
  <div class="rd-band__inner">
    <h2>Research Topics</h2>
    <p class="rd-band__subtitle">From micro-level crop physiology to macro-level facility energy management — coupling two scales of models to achieve optimal energy-to-biomass conversion.</p>

    <div class="rd-topics-grid rd-topics-grid--2col">
      <div class="rd-topics-grid__card">
        <div class="rd-topics-grid__placeholder-img"><span>Photo</span></div>
        <h3>Leaf Temperature Model</h3>
        <p class="rd-topics-grid__desc">Energy balance models that simulate heat exchange between crop and microclimate to diagnose plant stress and predict photosynthesis</p>
      </div>

      <div class="rd-topics-grid__card">
        <div class="rd-topics-grid__placeholder-img"><span>Photo</span></div>
        <h3>Facility Energy Model</h3>
        <p class="rd-topics-grid__desc">Integrated energy models that track where and how much energy is consumed, enabling optimal operation with minimal energy input</p>
      </div>
    </div>
  </div>
</section>
