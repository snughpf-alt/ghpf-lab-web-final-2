---
layout: default
title: Ph.D. Students
---

{% include page-hero.html
  label="People"
  title="Ph.D. Students"
  desc="Doctoral students advancing our core research areas."
%}

<div class="container container--content">

{% if site.data.team.phd.size > 0 %}
<section class="section team-section" id="postdoc">
  <div class="section__head">
    <h2>Postdoctoral Researcher</h2>
  </div>
  {% include team-grid.html collection="phd" %}
</section>
{% endif %}

<section class="section team-section" id="phd">
  {% include team-grid.html collection="phd_students" show_note=true split_parttime=true %}
</section>

</div>
