---
layout: default
title: Former Professor
---

{% include page-hero.html
  label="People"
  title="Former Professor"
  desc="The professor who built the foundation of the GHPF Lab."
%}

<div class="container container--content pi-content">

{% assign default_photo = '/assets/img/team/default.svg' | relative_url %}
{% assign p = site.data.team.former_faculty[0] %}

<!-- ── Profile ── -->
<section class="pi-sect" id="former-profile">
  <div class="pi-profile">
    <div class="pi-profile__photo">
      <img src="{{ p.photo | default: 'assets/img/team/default.svg' | relative_url }}" alt="{{ p.name | escape }}" onerror="this.src='{{ default_photo }}'">
    </div>
    <div class="pi-profile__body">
      <h2 class="pi-profile__name">{{ p.name | escape }}</h2>
      <p class="pi-profile__name-en">{{ p.name_en | escape }}</p>
      <p class="pi-profile__role">{{ p.title | escape }}</p>
      <p class="pi-profile__role">{{ p.subtitle | escape }}</p>
    </div>
  </div>
</section>

<!-- ── Education ── -->
{% if p.education.size > 0 %}
<section class="pi-sect" id="education">
  <h2 class="pi-sect__title">Education</h2>
  <div class="pi-edu">
    {% for e in p.education %}
    <div class="pi-edu__item">
      <div class="pi-edu__detail">
        <span class="pi-edu__univ">
          {{ e.university | escape }}
        </span>
        <span class="pi-edu__field">
          {{ e.degree | escape }}
        </span>
      </div>
    </div>
    {% endfor %}
  </div>
</section>
{% endif %}

<!-- ── Career ── -->
{% if p.career.size > 0 %}
<section class="pi-sect" id="career">
  <h2 class="pi-sect__title">Career</h2>
  <ul class="pi-list">
    {% for c in p.career %}
    <li>
      {{ c.text | escape }}
    </li>
    {% endfor %}
  </ul>
</section>
{% endif %}

<!-- ── Awards ── -->
{% if p.awards.size > 0 %}
<section class="pi-sect" id="awards">
  <h2 class="pi-sect__title">Awards</h2>
  <div class="pi-chips">
    {% for a in p.awards %}
    <div class="pi-chip">
      {{ a.text | escape }}
    </div>
    {% endfor %}
  </div>
</section>
{% endif %}

</div>
