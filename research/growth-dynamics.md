---
layout: default
title: Plant Growth Dynamics
---

<section class="page-hero">
  <div class="container page-hero__inner">
    <div class="page-hero__text">
      <p class="page-hero__label">Track 1 · Decoding Complexity</p>
      <h1 class="page-hero__title">Plant Growth<br>Dynamics</h1>
      <p class="page-hero__desc">Translating biological complexity into efficient numerical models</p>
    </div>
    <div class="page-hero__visual">
      <svg viewBox="0 0 340 280" fill="none" xmlns="http://www.w3.org/2000/svg" class="hero__diagram">
        <!-- Frame -->
        <rect x="20" y="10" width="300" height="260" rx="12" fill="rgba(255,255,255,.04)" stroke="rgba(255,255,255,.12)" stroke-width="1"/>

        <!-- ── Left: Plant growing ── -->
        <line x1="100" y1="220" x2="300" y2="220" stroke="rgba(255,255,255,.08)" stroke-width="0.5"/>
        <!-- Stem -->
        <line x1="100" y1="220" x2="100" y2="80" stroke="rgba(80,190,80,.7)" stroke-width="2.5" stroke-linecap="round">
          <animate attributeName="y2" values="220;80" dur="2.5s" fill="freeze"/>
        </line>
        <!-- Leaves (appear sequentially) -->
        <path d="M100,185 Q115,172 135,178 Q117,166 100,185Z" fill="rgba(80,180,70,.3)" stroke="rgba(80,190,70,.6)" stroke-width="1" opacity="0">
          <animate attributeName="opacity" values="0;1" dur="0.4s" begin="0.8s" fill="freeze"/>
        </path>
        <path d="M100,160 Q82,145 62,152 Q80,138 100,160Z" fill="rgba(80,180,70,.3)" stroke="rgba(80,190,70,.6)" stroke-width="1" opacity="0">
          <animate attributeName="opacity" values="0;1" dur="0.4s" begin="1.2s" fill="freeze"/>
        </path>
        <path d="M100,138 Q118,120 142,128 Q120,112 100,138Z" fill="rgba(80,180,70,.25)" stroke="rgba(80,190,70,.55)" stroke-width="1" opacity="0">
          <animate attributeName="opacity" values="0;1" dur="0.4s" begin="1.6s" fill="freeze"/>
        </path>
        <path d="M100,115 Q78,98 58,108 Q80,92 100,115Z" fill="rgba(80,180,70,.25)" stroke="rgba(80,190,70,.55)" stroke-width="1" opacity="0">
          <animate attributeName="opacity" values="0;1" dur="0.4s" begin="2.0s" fill="freeze"/>
        </path>
        <path d="M100,95 Q115,78 132,85 Q117,72 100,95Z" fill="rgba(80,180,70,.2)" stroke="rgba(80,190,70,.5)" stroke-width="1" opacity="0">
          <animate attributeName="opacity" values="0;1" dur="0.4s" begin="2.4s" fill="freeze"/>
        </path>

        <!-- ── Dashed arrow: Plant → Model ── -->
        <line x1="148" y1="140" x2="175" y2="140" stroke="rgba(255,255,255,.25)" stroke-width="1" stroke-dasharray="3 3"/>
        <polygon points="173,136 180,140 173,144" fill="rgba(255,255,255,.25)"/>

        <!-- ── Right: Growth model chart ── -->
        <rect x="182" y="50" width="120" height="120" rx="6" fill="rgba(255,255,255,.03)" stroke="rgba(255,255,255,.15)" stroke-width="0.8"/>
        <!-- Mini axes -->
        <line x1="196" y1="155" x2="290" y2="155" stroke="rgba(255,255,255,.2)" stroke-width="0.6"/>
        <line x1="196" y1="155" x2="196" y2="62" stroke="rgba(255,255,255,.2)" stroke-width="0.6"/>
        <!-- Axis labels -->
        <text x="243" y="166" text-anchor="middle" fill="rgba(255,255,255,.3)" font-size="6.5">Time</text>
        <text x="190" y="108" text-anchor="middle" fill="rgba(255,255,255,.3)" font-size="6.5" transform="rotate(-90 190 108)">Growth</text>
        <!-- Sigmoid curve (draws itself) -->
        <path d="M198,152 C210,150 220,146 230,135 C240,118 250,90 260,78 C270,70 280,68 288,66"
          stroke="rgba(120,220,120,.7)" stroke-width="2" fill="none" stroke-linecap="round"
          stroke-dasharray="120" stroke-dashoffset="120">
          <animate attributeName="stroke-dashoffset" values="120;0" dur="3s" begin="1s" fill="freeze"/>
        </path>
        <!-- Data points (appear with curve) -->
        <circle cx="215" cy="148" r="2" fill="rgba(200,160,255,.7)" opacity="0">
          <animate attributeName="opacity" values="0;1" dur="0.3s" begin="1.5s" fill="freeze"/>
        </circle>
        <circle cx="235" cy="130" r="2" fill="rgba(200,160,255,.7)" opacity="0">
          <animate attributeName="opacity" values="0;1" dur="0.3s" begin="2s" fill="freeze"/>
        </circle>
        <circle cx="255" cy="85" r="2" fill="rgba(200,160,255,.7)" opacity="0">
          <animate attributeName="opacity" values="0;1" dur="0.3s" begin="2.5s" fill="freeze"/>
        </circle>
        <circle cx="275" cy="72" r="2" fill="rgba(200,160,255,.7)" opacity="0">
          <animate attributeName="opacity" values="0;1" dur="0.3s" begin="3s" fill="freeze"/>
        </circle>

        <!-- Dimension badges below chart -->
        <rect x="186" y="180" width="52" height="16" rx="8" fill="rgba(200,160,255,.1)" stroke="rgba(200,160,255,.3)" stroke-width="0.6" opacity="0">
          <animate attributeName="opacity" values="0;1" dur="0.4s" begin="3.8s" fill="freeze"/>
        </rect>
        <text x="212" y="191" text-anchor="middle" fill="rgba(200,160,255,.7)" font-size="6.5" opacity="0">Reduction
          <animate attributeName="opacity" values="0;1" dur="0.4s" begin="3.8s" fill="freeze"/>
        </text>
        <rect x="246" y="180" width="52" height="16" rx="8" fill="rgba(120,220,120,.1)" stroke="rgba(120,220,120,.3)" stroke-width="0.6" opacity="0">
          <animate attributeName="opacity" values="0;1" dur="0.4s" begin="4.1s" fill="freeze"/>
        </rect>
        <text x="272" y="191" text-anchor="middle" fill="rgba(120,220,120,.7)" font-size="6.5" opacity="0">Simulation
          <animate attributeName="opacity" values="0;1" dur="0.4s" begin="4.1s" fill="freeze"/>
        </text>

        <!-- Label -->
        <text x="170" y="248" text-anchor="middle" fill="rgba(255,255,255,.5)" font-size="12" font-family="monospace" font-weight="600">Biology → Numerical Model</text>
      </svg>
    </div>
  </div>
</section>

<!-- ───── Overview (split) ───── -->
<section class="rd-overview-split">
  <div class="rd-overview-split__text">
    <h2 class="rd-overview-split__heading">Translating biology into numerical models</h2>
    <p class="rd-overview-split__desc">We convert biological complexity — such as energy-use dynamics and input resource efficiency — into high-efficiency numerical models through dimensionality reduction, building the backbone of accurate growth simulators. This methodological approach bridges the gap between raw biological data and computationally tractable growth predictions.</p>
    <div class="research-detail__topics" style="margin-bottom:28px">
      {% for area in site.data.research.tracks[0].areas %}
        {% if area.id == 'growth-dynamics' %}
          {% for topic in area.topics %}
          <span class="badge research-badge">{{ topic | escape }}</span>
          {% endfor %}
        {% endif %}
      {% endfor %}
    </div>
  </div>
  <div class="rd-overview-split__visual" style="background:transparent;padding:24px">
    <img src="{{ '/assets/img/research/growth-dynamics-overview.png' | relative_url }}" alt="Plant Growth Dynamics - Finite Resource Budgets" class="rd-overview-split__illustration" style="border-radius:12px;max-width:100%;max-height:none">
  </div>
</section>

<!-- ───── Research Topics (3-card layout) ───── -->
<section class="rd-band rd-band--dark">
  <div class="rd-band__inner">
    <h2>Research Topics</h2>
    <p class="rd-band__subtitle">Three interconnected pillars that drive our understanding of plant growth dynamics and energy-use efficiency.</p>

    <div class="rd-topics-grid">
      <div class="rd-topics-grid__card">
        <img src="{{ '/assets/img/research/light-quality.png' | relative_url }}" alt="Light Quality - plant factory with different LED spectra">
        <div class="rd-topics-grid__caption">
          <h3>Light Quality</h3>
          <div class="rd-topics-grid__keywords">
            <span class="badge">Spectral Tuning</span>
            <span class="badge">Photoreceptors</span>
            <span class="badge">Light Recipe</span>
          </div>
        </div>
      </div>

      <div class="rd-topics-grid__card">
        <img src="{{ '/assets/img/research/photosynthesis-lab.png' | relative_url }}" alt="Photosynthesis measurement setup">
        <div class="rd-topics-grid__caption">
          <h3>Photosynthetic<br>Physiology</h3>
          <div class="rd-topics-grid__keywords">
            <span class="badge">Light Response</span>
            <span class="badge">Photoinhibition</span>
            <span class="badge">Gas Exchange</span>
          </div>
        </div>
      </div>

      <div class="rd-topics-grid__card">
        <img src="{{ '/assets/img/research/stomata.png' | relative_url }}" alt="Leaf stomata microscope view" style="object-fit:contain;background:rgba(0,0,0,.35)">
        <div class="rd-topics-grid__caption">
          <h3>Leaf Temperature<br>&amp; Evapotranspiration</h3>
          <div class="rd-topics-grid__keywords">
            <span class="badge">Stomatal Dynamics</span>
            <span class="badge">Evapotranspiration</span>
            <span class="badge">Energy Balance</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
