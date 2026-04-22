---
layout: default
title: Gallery
---

{% include page-hero.html
  label="Gallery"
  title="Browse the<br>Gallery"
  desc="Memorable moments from our lab — celebrations, retreats, and time spent together."
%}

<div class="container container--content">

<!-- Filter buttons -->
<div class="gallery-filters">
  <button class="gallery-filter-btn active" data-filter="all">All</button>
  {% assign seen_tags = "" %}
  {% for item in site.data.gallery %}
    {% unless seen_tags contains item.tag %}
      {% assign seen_tags = seen_tags | append: item.tag | append: "|" %}
      <button class="gallery-filter-btn" data-filter="{{ item.tag }}">
        {{ item.tag | escape }}
      </button>
    {% endunless %}
  {% endfor %}
</div>

<section class="section">
  <!-- Masonry grid -->
  <div class="gallery-grid">
    {% for item in site.data.gallery %}
      <figure class="card gallery-card" data-tag="{{ item.tag }}">
        <button class="gallery-btn" type="button"
          data-src="{{ item.src | relative_url }}"
          data-title="{{ item.title | escape }}"
          data-caption="{{ item.caption | escape }}"
          aria-label="Open image: {{ item.title | escape }}">
          <img class="gallery-img" src="{{ item.src | relative_url }}" alt="{{ item.title | escape }}" loading="lazy">
          <div class="gallery-overlay">
            {% if item.tag %}<span class="gallery-overlay__tag">{{ item.tag | escape }}</span>{% endif %}
            <h3 class="gallery-overlay__title">{{ item.title | escape }}</h3>
            {% if item.caption %}<p class="gallery-overlay__caption">{{ item.caption | escape }}</p>{% endif %}
          </div>
        </button>
      </figure>
    {% endfor %}
  </div>
</section>

</div>

<!-- Modal -->
<dialog class="gallery-modal" id="galleryModal">
  <div class="gallery-modal__inner card">
    <div class="gallery-modal__top">
      <div>
        <h2 id="gmTitle" style="margin:0; font-size:22px;">Title</h2>
        <p class="muted small" id="gmCaption" style="margin:8px 0 0;">Caption</p>
      </div>
      <button class="btn btn--ghost" type="button" id="gmClose">Close</button>
    </div>

    <div class="gallery-modal__imgwrap">
      <img id="gmImg" alt="Gallery image" src="" />
    </div>
  </div>
</dialog>

<style>
.gallery-img, #gmImg {
  -webkit-user-select: none;
  user-select: none;
  -webkit-touch-callout: none;
  pointer-events: none;
}
.gallery-btn, .gallery-modal__imgwrap {
  pointer-events: auto;
}
</style>

<script>
(() => {
  // Prevent right-click and drag on gallery images
  document.addEventListener('contextmenu', (e) => {
    if (e.target.closest('.gallery-grid') || e.target.closest('.gallery-modal')) {
      e.preventDefault();
    }
  });
  document.addEventListener('dragstart', (e) => {
    if (e.target.tagName === 'IMG' && (e.target.closest('.gallery-grid') || e.target.closest('.gallery-modal'))) {
      e.preventDefault();
    }
  });
  const modal = document.getElementById('galleryModal');
  const gmImg = document.getElementById('gmImg');
  const gmTitle = document.getElementById('gmTitle');
  const gmCaption = document.getElementById('gmCaption');
  const gmClose = document.getElementById('gmClose');

  // Modal
  document.querySelectorAll('.gallery-btn').forEach(b => {
    b.addEventListener('click', () => {
      gmImg.src = b.dataset.src;
      gmImg.alt = b.dataset.title || 'Gallery image';
      gmTitle.textContent = b.dataset.title || '';
      gmCaption.textContent = b.dataset.caption || '';
      modal.showModal();
    });
  });
  gmClose.addEventListener('click', () => modal.close());
  modal.addEventListener('click', (e) => { if (e.target === modal) modal.close(); });

  // Filter
  const filterBtns = document.querySelectorAll('.gallery-filter-btn');
  const cards = document.querySelectorAll('.gallery-card');

  filterBtns.forEach(btn => {
    btn.addEventListener('click', () => {
      filterBtns.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;

      cards.forEach(card => {
        if (filter === 'all' || card.dataset.tag === filter) {
          card.style.display = '';
        } else {
          card.style.display = 'none';
        }
      });
    });
  });
})();
</script>
