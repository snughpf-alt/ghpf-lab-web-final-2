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
      <h2 class="pi-profile__name">{{ p.name_en | default: p.name | escape }}</h2>
      <p class="pi-profile__name-en">{{ p.name | escape }}</p>
      <p class="pi-profile__role">{{ p.title | escape }}</p>
      <p class="pi-profile__role">{{ p.subtitle | escape }}</p>
    </div>
  </div>
</section>

</div>
