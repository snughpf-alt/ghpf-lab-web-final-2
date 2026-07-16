---
layout: default
title: Home
---

{% include hero.html
  images="/assets/img/hero-plant-factory.jpg,/assets/img/hero-electric-field.jpg,/assets/img/hero-greenhouse.jpg,/assets/img/hero-photoconversion-film.jpg,/assets/img/hero-plant-led.jpg,/assets/img/hero-plant-led2.jpg,/assets/img/hero-phenotyping.jpg"
  pill="Greenhouse Horticulture and Plant Factory Lab"
  title="Decoding Plant-Environment Complexity<br>and Engineering Cultivation Systems"
  subtitle=""
  primary_text="Meet the Lab"
  primary_link="/team"
  secondary_text="Contact Us"
  secondary_link="/contact"
%}

<section class="section" id="content-start">
  <div class="container">
    <div class="section__head">
      <h2>Research Highlights</h2>
    </div>

    <div class="research-grid">
      <!-- Track 1 · Decoding Complexity (3) -->
      <a class="card highlight-card highlight-card--media" href="{{ '/research/growth-dynamics' | relative_url }}">
        <div class="highlight-card__media">
          <img src="{{ '/assets/img/research/seedling-tray.jpg' | relative_url }}" alt="Densely packed seedlings in a nursery tray" loading="lazy">
        </div>
        <div class="highlight-card__body">
          <span class="highlight-card__label">Track 1 · Decoding Complexity</span>
          <h3>Plant Growth Dynamics</h3>
          <p class="muted">Translating biological complexity into efficient numerical models.</p>
          <span class="highlight-card__link">Learn more →</span>
        </div>
      </a>

      <a class="card highlight-card highlight-card--media" href="{{ '/research/phenotyping' | relative_url }}">
        <div class="highlight-card__media">
          <img src="{{ '/assets/img/research/scan-model.png' | relative_url }}" alt="Reconstructed 3D plant canopy in Blender" loading="lazy">
        </div>
        <div class="highlight-card__body">
          <span class="highlight-card__label">Track 1 · Decoding Complexity</span>
          <h3>3D Plant Modeling</h3>
          <p class="muted">Beyond observation — computing light at canopy scale.</p>
          <span class="highlight-card__link">Learn more →</span>
        </div>
      </a>

      <a class="card highlight-card highlight-card--media" href="{{ '/research/electric-fields' | relative_url }}">
        <div class="highlight-card__media">
          <svg viewBox="0 0 320 220" fill="none" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMidYMid slice" style="width:100%;height:100%;display:block">
            <defs>
              <radialGradient id="ef-card-bg" cx="50%" cy="50%" r="60%">
                <stop offset="0%" stop-color="rgba(140,210,235,.22)"/>
                <stop offset="100%" stop-color="rgba(140,210,235,0)"/>
              </radialGradient>
            </defs>
            <rect x="0" y="0" width="320" height="220" fill="url(#ef-card-bg)"/>
            <!-- Concentric field rings -->
            <ellipse cx="160" cy="110" rx="125" ry="62" fill="none" stroke="rgba(140,210,235,.25)" stroke-width="1" stroke-dasharray="3 4"/>
            <ellipse cx="160" cy="110" rx="100" ry="50" fill="none" stroke="rgba(140,210,235,.32)" stroke-width="1" stroke-dasharray="3 4"/>
            <ellipse cx="160" cy="110" rx="75" ry="38" fill="none" stroke="rgba(140,210,235,.4)" stroke-width="1" stroke-dasharray="3 4"/>
            <!-- Charges -->
            <text x="22" y="115" fill="rgba(255,180,100,.85)" font-size="18" font-weight="700">+</text>
            <text x="288" y="115" fill="rgba(140,210,235,.95)" font-size="18" font-weight="700">−</text>
            <!-- Plant -->
            <line x1="160" y1="170" x2="160" y2="80" stroke="rgba(120,210,120,.85)" stroke-width="2" stroke-linecap="round"/>
            <path d="M160,140 Q140,128 124,135 Q146,118 160,140Z" fill="rgba(100,190,90,.5)" stroke="rgba(100,200,90,.85)" stroke-width="1"/>
            <path d="M160,140 Q180,128 196,135 Q174,118 160,140Z" fill="rgba(100,190,90,.5)" stroke="rgba(100,200,90,.85)" stroke-width="1"/>
            <path d="M160,112 Q140,100 124,107 Q146,86 160,112Z" fill="rgba(100,190,90,.45)" stroke="rgba(100,200,90,.75)" stroke-width="1"/>
            <path d="M160,112 Q180,100 196,107 Q174,86 160,112Z" fill="rgba(100,190,90,.45)" stroke="rgba(100,200,90,.75)" stroke-width="1"/>
            <path d="M160,84 Q152,80 148,72 Q157,66 160,84 Q163,66 172,72 Q168,80 160,84Z" fill="rgba(100,190,90,.55)" stroke="rgba(100,200,90,.85)" stroke-width="1"/>
          </svg>
        </div>
        <div class="highlight-card__body">
          <span class="highlight-card__label">Track 1 · Decoding Complexity</span>
          <h3>Electric Field Biology</h3>
          <p class="muted">An open frontier in plant–environment research — probing how electric fields and the plant's energy economy shape life.</p>
          <span class="highlight-card__link">Learn more →</span>
        </div>
      </a>

      <!-- Track 2 · Engineering Systems (2) -->
      <a class="card highlight-card highlight-card--media" href="{{ '/research/autonomous-control' | relative_url }}">
        <div class="highlight-card__media">
          <img src="{{ '/assets/img/research/strawberry-field-sensing.jpg' | relative_url }}" alt="In-field strawberry sensing with cameras and a tablet showing live data" loading="lazy">
        </div>
        <div class="highlight-card__body">
          <span class="highlight-card__label">Track 2 · Engineering Systems</span>
          <h3>LLM in Agriculture</h3>
          <p class="muted">Encoding expert knowledge into language models for agricultural decision-making.</p>
          <span class="highlight-card__link">Learn more →</span>
        </div>
      </a>

      <a class="card highlight-card highlight-card--media" href="{{ '/research/energy-food-nexus' | relative_url }}">
        <div class="highlight-card__media">
          <img src="{{ '/assets/img/research/plant-factory-chambers.jpg' | relative_url }}" alt="Plant factory cultivation chambers with WALZ photosynthesis instrument" loading="lazy">
        </div>
        <div class="highlight-card__body">
          <span class="highlight-card__label">Track 2 · Engineering Systems</span>
          <h3>Energy-Food Nexus</h3>
          <p class="muted">Maximizing the conversion of energy to biomass.</p>
          <span class="highlight-card__link">Learn more →</span>
        </div>
      </a>
    </div>
  </div>
</section>
