---
layout: default
title: PI
---

{% assign default_photo = '/assets/img/team/default.svg' | relative_url %}
{% assign p = site.data.team.faculty[0] %}

{% include page-hero.html
  label="People"
  title="Principal Investigator (PI)"
  desc="Faculty leading the GHPF Lab's research."
%}

<div class="container container--content pi-content">

<!-- ── Profile ── -->
<section class="pi-sect" id="pi-profile">
  <div class="pi-profile">
    <div class="pi-profile__photo">
      <img src="{{ p.photo | default: 'assets/img/team/default.svg' | relative_url }}" alt="{{ p.name | escape }}" onerror="this.src='{{ default_photo }}'">
    </div>
    <div class="pi-profile__body">
      <h2 class="pi-profile__name">{{ p.name | escape }}</h2>
      <p class="pi-profile__name-en">{{ p.name_en | escape }}</p>
      <p class="pi-profile__role">{{ p.role | escape }}</p>

      <div class="pi-profile__contact">
        <div class="pi-profile__contact-item">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
          <a href="mailto:{{ p.email | escape }}">{{ p.email | escape }}</a>
        </div>
        <div class="pi-profile__contact-item">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
          <span>{{ p.phone | escape }}</span>
        </div>
        <div class="pi-profile__contact-item">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"/><circle cx="12" cy="10" r="3"/></svg>
          <span>{{ p.office | escape }}</span>
        </div>
        <div class="pi-profile__contact-item">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M9.5 2A2.5 2.5 0 0 1 12 4.5v15a2.5 2.5 0 0 1-4.96.44 2.5 2.5 0 0 1-2.96-3.08 3 3 0 0 1-.34-5.58 2.5 2.5 0 0 1 1.32-4.24 2.5 2.5 0 0 1 1.98-3A2.5 2.5 0 0 1 9.5 2Z"/><path d="M14.5 2A2.5 2.5 0 0 0 12 4.5v15a2.5 2.5 0 0 0 4.96.44 2.5 2.5 0 0 0 2.96-3.08 3 3 0 0 0 .34-5.58 2.5 2.5 0 0 0-1.32-4.24 2.5 2.5 0 0 0-1.98-3A2.5 2.5 0 0 0 14.5 2Z"/></svg>
          <span>{{ p.major | escape }}</span>
        </div>
        <div class="pi-profile__contact-item">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M15 3v4a2 2 0 0 0 2 2h4"/><path d="M18 17h-7a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h4l5 5v7a2 2 0 0 1-2 2z"/><path d="M16 17v2a2 2 0 0 1-2 2H7a2 2 0 0 1-2-2V9a2 2 0 0 1 2-2h2"/></svg>
          <span>{{ p.lab | escape }}</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── Education & Career (2-column) ── -->
<div class="pi-duo">

  {% if p.education.size > 0 %}
  <section class="pi-duo__col" id="education">
    <h2 class="pi-sect__title">Education</h2>
    <div class="pi-edu">
      {% for e in p.education %}
      <div class="pi-edu__item">
        <div class="pi-edu__year">{{ e.year | escape }}</div>
        <div class="pi-edu__detail">
          <span class="pi-edu__univ">
            {{ e.university | escape }}
          </span>
          <span class="pi-edu__field">
            {{ e.field | escape }} ({{ e.degree | escape }})
          </span>
        </div>
      </div>
      {% endfor %}
    </div>
  </section>
  {% endif %}

  {% if p.career.size > 0 %}
  <section class="pi-duo__col" id="career">
    <h2 class="pi-sect__title">Career</h2>
    <div class="pi-timeline">
      {% assign prev_year = 0 %}
      {% for c in p.career %}
        {% if c.year != prev_year %}
        <div class="pi-timeline__item{% if c.ongoing %} pi-timeline__item--active{% endif %}">
          <div class="pi-timeline__marker"></div>
          <div class="pi-timeline__body">
            <div class="pi-timeline__year">{{ c.year | escape }}{% if c.ongoing %}<span class="pi-timeline__present"> ~ Present</span>{% endif %}</div>
            <div class="pi-timeline__entries">
              {% for c2 in p.career %}
                {% if c2.year == c.year %}
                <p class="pi-timeline__text">
                  {{ c2.text | escape }}
                </p>
                {% endif %}
              {% endfor %}
            </div>
          </div>
        </div>
        {% assign prev_year = c.year %}
        {% endif %}
      {% endfor %}
    </div>
  </section>
  {% endif %}

</div>

<!-- ── Research Activities ── -->
{% if p.research_activities.size > 0 %}
<section class="pi-sect" id="research">
  <h2 class="pi-sect__title">Research Activities</h2>
  <ul class="pi-list">
    {% for r in p.research_activities %}
    <li>
      {{ r.text | escape }}
    </li>
    {% endfor %}
  </ul>
</section>
{% endif %}

<!-- ── External Activities ── -->
{% if p.external_activities.size > 0 %}
<section class="pi-sect" id="external">
  <h2 class="pi-sect__title">External Activities</h2>
  <div class="pi-chips">
    {% for e in p.external_activities %}
    <div class="pi-chip">
      {{ e.text | escape }}
    </div>
    {% endfor %}
  </div>
</section>
{% endif %}

<!-- ── Former Professor ── -->
<section class="pi-sect" id="former">
  <h2 class="pi-sect__title">Former Professor</h2>
  <p>
    <a class="pi-former-link" href="{{ '/people/former-professor' | relative_url }}">
      View
      <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
    </a>
  </p>
</section>

</div>
