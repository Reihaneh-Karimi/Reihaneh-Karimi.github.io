---
title: "My Astro-Photography Image Gallery"
permalink: /gallery/
layout: single
author_profile: true

gallery:
  - image: /assets/images/Image1.jpg
    alt: Milky Way
    caption: |
      Milky Way over Kharaqan-Qazvin Twin Towers  
      3-panel panorama  
      Canon 550D (modified) • EF 8-15 mm • ISO 1600
  - image: /assets/images/Image2.jpg
    alt: Moon
    caption: |
      Telescope: 150 mm Skywatcher  
      Mount: EQ3-2
  - image: /assets/images/Image3.jpg
    alt: Perseid Meteor Showers
    caption: |
      Perseid meteors next to Venus  
      11 Aug 2020
  - image: /assets/images/Image4.jpg
    alt: Lunar Craters
    caption: |
      Celestron 8" XLT • ZWO ASI290MC  
      Mount: HEQ5 PRO
  - image: /assets/images/Image5.jpg
    alt: Startrails
    caption: |
      ~2 h of Earth rotation (928 shots)  
      Canon 600D • 35 mm Samyang • 10 s • ISO 1600
  - image: /assets/images/Image6.jpg
    alt: Perseid Meteor Shower
    caption: |
      Perseid shower at the National Observatory of Iran
  - image: /assets/images/Image7.jpg
    alt: Solar Eclipse
    caption: Solar Eclipse
  - image: /assets/images/Image8.jpg
    alt: Leiden Observatory
    caption: Leiden Observatory
  - image: /assets/images/Image9.jpg
    alt: Super Full Moon
    caption: |
      Super Full Moon  
      17 Sep 2024
  - image: /assets/images/Image10.jpg
    alt: Radio Telescope
    caption: Westerbork Synthesis Radio Telescope
  - image: /assets/images/Image11.jpg
    alt: Lunar Crater
    caption: Newton’s Lunar Crater
---

<style>
/* --- Layout --- */
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1.5rem;
  align-items: start;
}

/* --- Each item --- */
.gallery-item {
  position: relative;
  overflow: hidden;
  border-radius: 6px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
  background: #000;
}

/* --- Image --- */
.gallery-item img {
  width: 100%;
  height: auto;
  display: block;
  transition: transform 0.4s ease;
}
.gallery-item:hover img {
  transform: scale(1.05);
}

/* --- Caption overlay --- */
.gallery-item figcaption {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 0.6rem 0.8rem;
  font-size: 0.8rem;
  line-height: 1.3;
  color: #fff;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.75), transparent);
  max-height: 4rem;        /* show a teaser by default */
  overflow: hidden;
  transition: max-height 0.4s ease, background 0.4s ease;
}

/* --- Hover: show full caption --- */
.gallery-item:hover figcaption {
  max-height: 12rem;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.9), transparent);
}

/* Optional: align left/center/right per row for a dynamic feel */
.gallery-item:nth-child(3n+1) { justify-self: start; }
.gallery-item:nth-child(3n+2) { justify-self: center; }
.gallery-item:nth-child(3n+3) { justify-self: end; }
</style>

<div class="gallery-grid">
  {% for item in page.gallery %}
    <figure class="gallery-item">
      <img src="{{ item.image }}" alt="{{ item.alt }}">
      <figcaption>{{ item.caption | markdownify }}</figcaption>
    </figure>
  {% endfor %}
</div>
