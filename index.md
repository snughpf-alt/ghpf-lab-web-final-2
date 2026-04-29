---
layout: default
title: Home
---

{% include hero.html
  images="/assets/img/hero-plant-factory.jpg,/assets/img/hero-greenhouse.jpg,/assets/img/hero-photoconversion-film.jpg,/assets/img/hero-plant-led.jpg,/assets/img/hero-plant-led2.jpg,/assets/img/hero-phenotyping.jpg"
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

    <div class="grid grid--2">
      <a class="card highlight-card highlight-card--media" href="{{ '/research/growth-dynamics' | relative_url }}">
        <div class="highlight-card__media">
          <img src="{{ '/assets/img/research/flir-thermal-spectra.jpg' | relative_url }}" alt="FLIR thermal imaging of leaves under different light spectra" loading="lazy">
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
          <img src="{{ '/assets/img/research/scan-view.png' | relative_url }}" alt="3D plant mesh in Blender" loading="lazy">
        </div>
        <div class="highlight-card__body">
          <span class="highlight-card__label">Track 1 · Decoding Complexity</span>
          <h3>3D Plant Modeling</h3>
          <p class="muted">Beyond observation — computing light at canopy scale.</p>
          <span class="highlight-card__link">Learn more →</span>
        </div>
      </a>

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
