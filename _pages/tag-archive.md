---
title: "My Astro-Photography Image Gallery"
permalink: /gallery/
layout: single
author_profile: true

gallery:
  - image: /assets/images/Image1.jpg
    alt: Milky Way
    caption: |
      Milky Way — 3-panel panorama  
      Camera: Canon 550D (modified)  
      Lens: Canon EF 8-15 mm — ISO 1600
  - image: /assets/images/Image2.jpg
    alt: Moon
    caption: |
      Telescope: 150 mm Skywatcher  
      Mount: EQ3-2
  - image: /assets/images/Image3.jpg
    alt: Perseid Meteor Showers
    caption: |
      Perseid Meteor Showers next to Venus  
      Date: 11 August 2020
  - image: /assets/images/Image4.jpg
    alt: Lunar Craters
    caption: |
      Telescope: Celestron 8" XLT  
      Camera: ZWO ASI290MC  
      Mount: HEQ5 PRO
  - image: /assets/images/Image5.jpg
    alt: Startrails 🌠
    caption: |
      Startrails — ~2 h Earth rotation  
      Camera: Canon 600D, 35 mm lens  
      Total shots: 928
  - image: /assets/images/Image6.jpg
    alt: Perseid Meteor Shower
    caption: |
      Perseid meteor shower at the National Observatory of Iran
  - image: /assets/images/Image7.jpg
    alt: Solar Eclipse
    caption: Solar Eclipse
  - image: /assets/images/Image8.jpg
    alt: Leiden Observatory
    caption: Leiden Observatory
  - image: /assets/images/Image9.jpg
    alt: Super Full Moon
    caption: |
      Super Full Moon — 17 Sep 2024
  - image: /assets/images/Image11.jpg
    alt: Lunar Crater
    caption: Newton's Lunar Crater
  - image: /assets/images/Image10.jpg
    alt: Radio Telescope
    caption: Westerbork Synthesis Radio Telescope
  - image: /assets/images/Image12.jpg
    alt: RT
    caption: Westerbork Synthesis Radio Telescope
---

<style>
/* Grid layout */
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;            /* more space between items */
}

/* Each figure */
.gallery-item {
  text-align: center;    /* center image + caption text */
}

.gallery-item img {
  width: 100%;
  height: auto;
  border-radius: 4px;
  display: block;
  margin-bottom: 0.5rem;  /* space between image and caption */
  transition: transform 0.3s ease;
}

.gallery-item img:hover {
  transform: scale(1.02); /* subtle zoom on hover */
}

/* Caption styling */
.gallery-item figcaption {
  font-size: 0.8rem;
  line-height: 1.4;
  color: #444;           /* dark grey text below image */
  background: #f8f8f8;   /* light background behind text */
  padding: 0.5rem 0.75rem;
  border-radius: 4px;
}
</style>

<div class="gallery-grid">
  {% for item in page.gallery %}
    <figure class="gallery-item">
      <img src="{{ item.image }}" alt="{{ item.alt }}" />
      <figcaption>{{ item.caption | markdownify }}</figcaption>
    </figure>
  {% endfor %}
</div>
