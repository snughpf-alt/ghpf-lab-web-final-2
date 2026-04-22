---
layout: default
title: Research
---

<!-- ===== HERO ===== -->
{% include page-hero.html
  label="Research"
  title="Decode &<br>Engineer"
  desc="We decode the complexity of plant-environment interactions through data and modeling, then engineer those insights into resilient, optimized cultivation systems."
%}

<!-- ===== RESEARCH BLOCKS (Google Research style) ===== -->
{% for track in site.data.research.tracks %}
<section class="rblock" style="--block-color:{{ track.color }}">
  <div class="container rblock__inner {% if forloop.index == 2 %}rblock__inner--reverse{% endif %}">

    <!-- Text side -->
    <div class="rblock__text">
      <span class="rblock__badge">Track {{ forloop.index }}</span>
      <h2 class="rblock__title">
        {{ track.title | escape }}
      </h2>
      <p class="rblock__desc">
        {{ track.description | escape }}
      </p>

      <!-- Area links -->
      <div class="rblock__areas">
        {% for area in track.areas %}
        <a href="{{ '/research/' | append: area.id | relative_url }}" class="rblock__area-link" style="--area-color:{{ area.color }}">
          <div class="rblock__area-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 48 48">
              {% if area.icon == 'phenotyping' %}
              <path d="M24 4v40M4 24h40"/><circle cx="24" cy="24" r="16"/><circle cx="24" cy="24" r="8"/>
              {% elsif area.icon == 'growth' %}
              <path d="M24 44V24"/><path d="M24 32C24 24 16 20 10 20c0 8 8 12 14 12z"/><path d="M24 24C24 16 32 12 38 12c0 8-8 12-14 12z"/>
              {% elsif area.icon == 'llm' %}
              <rect x="6" y="6" width="36" height="36" rx="4"/><path d="M14 18h20M14 24h16M14 30h12"/>
              {% elsif area.icon == 'energy' %}
              <path d="M26 4L12 28h12l-2 16 14-24H24z"/>
              {% endif %}
            </svg>
          </div>
          <div class="rblock__area-info">
            <span class="rblock__area-name">
              {{ area.title | escape }}
            </span>
            <span class="rblock__area-tagline">
              {{ area.tagline | escape }}
            </span>
          </div>
          <svg class="rblock__area-arrow" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>
        </a>
        {% endfor %}
      </div>
    </div>

    <!-- Visual side -->
    <div class="rblock__visual">
      {% if forloop.index == 1 %}
      <div class="rblock__mosaic rblock__mosaic--2">
        <img src="{{ '/assets/img/research/light-quality.png' | relative_url }}" alt="Plant factory with different LED spectra" loading="lazy">
      </div>
      {% else %}
      <div class="rblock__mosaic rblock__mosaic--2">
        <img src="{{ '/assets/img/research/energy-nexus.png' | relative_url }}" alt="Energy-Food Nexus" loading="lazy">
      </div>
      {% endif %}
    </div>

  </div>
</section>
{% endfor %}
