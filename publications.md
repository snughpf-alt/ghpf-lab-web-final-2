---
layout: default
title: Publications
---

{% include page-hero.html
  label="Publications"
  title="Explore Our<br>Publications"
  desc="Selected peer-reviewed publications and research outputs from our&nbsp;lab, spanning plant physiology, greenhouse engineering, and data&#8209;driven&nbsp;agriculture."
%}

<div class="container container--content">

<!-- Tag filter bar -->
{% assign all_tags = "" %}
{% for pub in site.data.publications %}
  {% for tag in pub.tags %}
    {% unless all_tags contains tag %}
      {% if all_tags == "" %}
        {% assign all_tags = tag %}
      {% else %}
        {% assign all_tags = all_tags | append: "," | append: tag %}
      {% endif %}
    {% endunless %}
  {% endfor %}
{% endfor %}
{% assign tag_list = all_tags | split: "," | sort %}

<div class="pub-filter" id="pub-filter">
  <button class="pub-filter__btn active" data-tag="all">All</button>
  {% for tag in tag_list %}
  <button class="pub-filter__btn" data-tag="{{ tag | escape }}">{{ tag | escape }}</button>
  {% endfor %}
</div>

{% assign pubs = site.data.publications | sort: "year" | reverse %}
{% assign current_year = "" %}

{% for pub in pubs %}
  {% if pub.year != current_year %}
    {% if current_year != "" %}
      </div>
    </section>
    {% endif %}

    <section class="section team-section pub-year-section" data-year="{{ pub.year }}">
      <div class="section__head">
        <h2>{{ pub.year }}</h2>
      </div>
      <div class="pub-grid">
    {% assign current_year = pub.year %}
  {% endif %}

    <div class="card pub-card" data-tags="{{ pub.tags | join: ',' }}">
      <h3 class="pub-card__title">{{ pub.title | escape }}</h3>
      {% if pub.tags.size > 0 %}
      <div class="pub-card__tags">
        {% for tag in pub.tags %}<span class="badge">{{ tag | escape }}</span>{% endfor %}
      </div>
      {% endif %}
      <p class="pub-card__authors">{{ pub.authors | escape }}</p>
      <p class="pub-card__venue">{{ pub.venue | escape }}</p>
      {% if pub.doi and pub.doi != "" %}
        <p class="pub-card__link">
          <a class="link" href="https://doi.org/{{ pub.doi | escape }}" target="_blank" rel="noopener noreferrer">View Paper &rarr;</a>
        </p>
      {% elsif pub.arxiv and pub.arxiv != "" %}
        <p class="pub-card__link">
          <a class="link" href="https://doi.org/10.48550/arXiv.{{ pub.arxiv | escape }}" target="_blank" rel="noopener noreferrer">View Paper &rarr;</a>
        </p>
      {% endif %}
    </div>

{% endfor %}

{% if current_year != "" %}
  </div>
</section>
{% endif %}

</div>

<script>
(function(){
  var btns = document.querySelectorAll('.pub-filter__btn');
  btns.forEach(function(btn){
    btn.addEventListener('click', function(){
      btns.forEach(function(b){ b.classList.remove('active'); });
      btn.classList.add('active');
      var tag = btn.getAttribute('data-tag');
      var cards = document.querySelectorAll('.pub-card');
      cards.forEach(function(card){
        if(tag === 'all'){
          card.style.display = '';
        } else {
          var tags = card.getAttribute('data-tags').split(',');
          card.style.display = tags.indexOf(tag) !== -1 ? '' : 'none';
        }
      });
      // Hide year sections with no visible cards
      document.querySelectorAll('.pub-year-section').forEach(function(sec){
        var visible = sec.querySelectorAll('.pub-card:not([style*="display: none"])');
        sec.style.display = visible.length ? '' : 'none';
      });
    });
  });
})();
</script>
