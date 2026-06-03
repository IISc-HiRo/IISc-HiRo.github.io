---
layout: main
title: Publications
permalink: /publications/
---

<div class="research-section">
  <h1>Publications</h1>

  <div class="filter-buttons">
    <button class="filter-btn active" data-filter="all">All</button>
    <button class="filter-btn" data-filter="conference">Conference</button>
    <button class="filter-btn" data-filter="journal">Journal</button>
    <button class="filter-btn" data-filter="workshop">Workshop</button>
  </div>

  <div class="publications-list">
    {%- assign years = site.data.publications | map: "year" | uniq | sort | reverse -%}
    {%- for year in years %}
    <h2 class="year-header">{{ year }}</h2>
    {%- assign year_pubs = site.data.publications | where: "year", year -%}
    {%- for pub in year_pubs %}
    <div class="publication-item" id="{{ pub.id }}" data-category="{{ pub.type }}">
      <div class="pub-thumbnail">
        <img src="/assets/img/publication_preview/{{ pub.image }}" alt="{{ pub.title | strip_html }}">
        <div class="pub-venue-tag">{{ pub.tag }}</div>
      </div>
      <div class="pub-content">
        <div class="pub-title">{{ pub.title }}</div>
        <div class="pub-authors">{{ pub.authors }}</div>
        <div class="pub-venue">{{ pub.venue }}</div>
        <div class="pub-links">
          {%- for link in pub.links %}
          {%- if link.url %}
          <a href="{{ link.url }}" target="_blank" class="pub-link-text">{{ link.label }}</a>
          {%- else %}
          <span class="pub-link-text">{{ link.label }}</span>
          {%- endif %}
          {%- endfor %}
        </div>
      </div>
    </div>
    {%- endfor %}
    {%- endfor %}
  </div>
</div>

<!-- Image Modal -->
<div id="imageModal" style="display:none; position:fixed; z-index:1000; left:0; top:0; width:100%; height:100%; background-color:rgba(0,0,0,0.9); cursor:pointer;">
  <span style="position:absolute; top:20px; right:40px; color:#fff; font-size:40px; font-weight:bold; cursor:pointer;">&times;</span>
  <img id="modalImage" style="display:block; width:92vw; height:90vh; object-fit:contain; position:absolute; top:50%; left:50%; transform:translate(-50%, -50%);">
</div>

<script>
  // Publication filtering functionality
  document.addEventListener('DOMContentLoaded', function() {
    const filterButtons = document.querySelectorAll('.filter-btn');
    const publications = document.querySelectorAll('.publication-item');
    const yearHeaders = document.querySelectorAll('.year-header');

    filterButtons.forEach(button => {
      button.addEventListener('click', function() {
        // Update active button
        filterButtons.forEach(btn => btn.classList.remove('active'));
        this.classList.add('active');

        const filterValue = this.getAttribute('data-filter');

        // Filter publications
        publications.forEach(pub => {
          if (filterValue === 'all') {
            pub.style.display = 'flex';
          } else {
            const category = pub.getAttribute('data-category');
            pub.style.display = category === filterValue ? 'flex' : 'none';
          }
        });

        // Show/hide year headers based on visible publications
        yearHeaders.forEach(header => {
          let nextElement = header.nextElementSibling;
          let hasVisiblePubs = false;
          
          while (nextElement && !nextElement.classList.contains('year-header')) {
            if (nextElement.classList.contains('publication-item') && nextElement.style.display !== 'none') {
              hasVisiblePubs = true;
              break;
            }
            nextElement = nextElement.nextElementSibling;
          }
          
          header.style.display = hasVisiblePubs || filterValue === 'all' ? 'block' : 'none';
        });
      });
    });

    // Image modal functionality
    const modal = document.getElementById('imageModal');
    const modalImg = document.getElementById('modalImage');
    const pubImages = document.querySelectorAll('.pub-thumbnail img');

    pubImages.forEach(img => {
      img.style.cursor = 'pointer';
      img.addEventListener('click', function(e) {
        e.preventDefault();
        modal.style.display = 'block';
        modalImg.src = this.src;
      });
    });

    // Close modal on click
    modal.addEventListener('click', function() {
      modal.style.display = 'none';
    });

    // Close modal on Escape key
    document.addEventListener('keydown', function(e) {
      if (e.key === 'Escape' && modal.style.display === 'block') {
        modal.style.display = 'none';
      }
    });
  });
</script>
