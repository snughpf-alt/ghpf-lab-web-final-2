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
          <span class="rblock__area-number">{{ forloop.index | prepend: '0' | slice: -2, 2 }}</span>
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
        <img src="{{ '/assets/img/research/cucumber-3d-scan.png' | relative_url }}" alt="3D scanned plant mesh in Blender" loading="lazy">
      </div>
      {% else %}
      <div class="rblock__mosaic rblock__mosaic--2">
        <img src="{{ '/assets/img/hero-plant-factory.jpg' | relative_url }}" alt="Plant factory interior with multi-spectral LED lighting" loading="lazy">
      </div>
      {% endif %}
    </div>

  </div>
</section>
{% endfor %}
