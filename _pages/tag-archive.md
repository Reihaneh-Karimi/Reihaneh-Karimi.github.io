---
title: "My Astro-Photography Image Gallery"
permalink: /gallery/
layout: single
author_profile: true

gallery:
  - image: /assets/images/Image1.jpg
    alt: Milky Way
    caption: |
      Exif: Milky Way among Kharaqan-Qazvin Twin Tower
      3 panorama panels
      Camera: Canon 550D modified
      Lens: Canon EF 8-15mm fisheye
      ISO: 1600, f/4
  - image: /assets/images/Image2.jpg
    alt: Moon
    caption: |
      Telescope: 150mm Skywatcher
      Mount: EQ3_2
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
      Mount: HEQ5PRO
  - image: /assets/images/Image5.jpg
    alt: Startrails 🌠
    caption: |
      Startrails 🌠: half & two hours Earth's rotation
      Camera: Canon 600D
      Lens: 35mm Samyang
      Exposure: 10s, ISO: 1600
      Total shots: 928
  - image: /assets/images/Image6.jpg
    alt: BPerseid Meteor Shower
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
      Super Full Moon
      Date: Sep 17, 2024
---

<style>
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
}

.gallery-item {
  position: relative;
  overflow: hidden;
  text-align: center;
  border-radius: 4px;
}

.gallery-item img {
  width: 100%;
  height: auto;
  display: block;
  transition: transform 0.3s ease;
}

.gallery-item:hover img {
  transform: scale(1.05);
}

/* Caption: partially visible by default */
.gallery-item figcaption {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: rgba(0, 0, 0, 0.5); /* partially visible */
  color: #fff;
  padding: 0.5rem;
  font-size: 0.85rem;
  line-height: 1.3;
  max-height: 3rem; /* show only first line or two */
  overflow: hidden;
  transition: max-height 0.4s ease, background 0.4s ease, padding 0.4s ease;
  text-align: left;
  cursor: pointer;
}

/* On hover: expand caption fully */
.gallery-item:hover figcaption {
  background: rgba(0, 0, 0, 0.8);
  max-height: 15rem; /* expand to full caption */
  padding: 0.75rem;
}

/* Automatic alignment left/center/right per row */
.gallery-item:nth-child(3n+1) { justify-self: start; }
.gallery-item:nth-child(3n+2) { justify-self: center; }
.gallery-item:nth-child(3n+3) { justify-self: end; }
</style>

<div class="gallery-grid">
  {% for item in page.gallery %}
    <figure class="gallery-item">
      <img src="{{ item.image }}" alt="{{ item.alt }}" />
      <figcaption>{{ item.caption | markdownify }}</figcaption>
    </figure>
  {% endfor %}
</div>
