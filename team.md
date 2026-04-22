---
layout: default
title: People
permalink: /team/
---

{% assign default_photo = '/assets/img/team/default.svg' | relative_url %}
{% assign pi = site.data.team.faculty | first %}
{% assign phd_a = site.data.team.phd %}
{% assign phd_b = site.data.team.phd_students %}
{% assign phd_count = phd_a.size | plus: phd_b.size %}
{% assign ms_all = site.data.team.ms_students %}
{% assign ug_all = site.data.team.interns %}
{% assign al_all = site.data.team.alumni %}

{% include page-hero.html
  label="People"
  title="Meet the Researchers"
  desc="The researchers and students of GHPF Lab."
%}

<div class="container container--content people-mosaic">

  <!-- PI -->
  <a href="{{ '/people/professor' | relative_url }}" class="mosaic-group">
    <div class="mosaic-group__head">
      <h2 class="mosaic-group__title">Principal Investigator</h2>
      <svg class="mosaic-group__arrow" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
    </div>
    <div class="mosaic-group__faces">
      <div class="mosaic-face">
        <img src="{{ pi.photo | relative_url }}" alt="{{ pi.name | escape }}" onerror="this.src='{{ default_photo }}'">
        <span class="mosaic-face__name">{{ pi.name | escape }}</span>
      </div>
    </div>
  </a>

  <!-- PhD -->
  <a href="{{ '/people/phd' | relative_url }}" class="mosaic-group">
    <div class="mosaic-group__head">
      <h2 class="mosaic-group__title">Ph.D. Students <span class="mosaic-group__count">{{ phd_count }}</span></h2>
      <svg class="mosaic-group__arrow" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
    </div>
    <div class="mosaic-group__faces">
      {% for m in phd_a %}{% unless m.photo contains '.svg' %}
      <div class="mosaic-face">
        <img src="{{ m.photo | relative_url }}" alt="{{ m.name | escape }}" onerror="this.src='{{ default_photo }}'">
        <span class="mosaic-face__name">{{ m.name | escape }}</span>
      </div>
      {% endunless %}{% endfor %}
      {% for m in phd_b %}{% unless m.photo contains '.svg' %}
      <div class="mosaic-face">
        <img src="{{ m.photo | relative_url }}" alt="{{ m.name | escape }}" onerror="this.src='{{ default_photo }}'">
        <span class="mosaic-face__name">{{ m.name | escape }}</span>
      </div>
      {% endunless %}{% endfor %}
    </div>
  </a>

  <!-- MS -->
  <a href="{{ '/people/ms' | relative_url }}" class="mosaic-group">
    <div class="mosaic-group__head">
      <h2 class="mosaic-group__title">M.S. Students <span class="mosaic-group__count">{{ ms_all | size }}</span></h2>
      <svg class="mosaic-group__arrow" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
    </div>
    <div class="mosaic-group__faces">
      {% for m in ms_all %}{% unless m.photo contains '.svg' %}
      <div class="mosaic-face">
        <img src="{{ m.photo | relative_url }}" alt="{{ m.name | escape }}" onerror="this.src='{{ default_photo }}'">
        <span class="mosaic-face__name">{{ m.name | escape }}</span>
      </div>
      {% endunless %}{% endfor %}
    </div>
  </a>

  <!-- Undergrad -->
  <a href="{{ '/people/undergrad' | relative_url }}" class="mosaic-group">
    <div class="mosaic-group__head">
      <h2 class="mosaic-group__title">Undergraduates <span class="mosaic-group__count">{{ ug_all | size }}</span></h2>
      <svg class="mosaic-group__arrow" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
    </div>
    <div class="mosaic-group__faces">
      {% for m in ug_all %}
      <div class="mosaic-face">
        <img src="{{ m.photo | relative_url }}" alt="{{ m.name | escape }}" onerror="this.src='{{ default_photo }}'">
        <span class="mosaic-face__name">{{ m.name | escape }}</span>
      </div>
      {% endfor %}
    </div>
  </a>

  <!-- Alumni -->
  <a href="{{ '/people/alumni' | relative_url }}" class="mosaic-group">
    <div class="mosaic-group__head">
      <h2 class="mosaic-group__title">Alumni <span class="mosaic-group__count">{{ al_all | size }}</span></h2>
      <svg class="mosaic-group__arrow" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
    </div>
    <div class="mosaic-group__faces">
      {% for m in al_all %}
      <div class="mosaic-face">
        <img src="{{ m.photo | relative_url }}" alt="{{ m.name | escape }}" onerror="this.src='{{ default_photo }}'">
        <span class="mosaic-face__name">{{ m.name | escape }}</span>
      </div>
      {% endfor %}
    </div>
  </a>

</div>
