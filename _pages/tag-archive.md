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
      Perseid meteor shower at Nthe ational Observatory of Iran
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
  text-align: center;
}

.gallery-item img {
  max-width: 100%;
  height: auto;
  border-radius: 4px;
}

.gallery-item figcaption {
  margin-top: 0.5rem;
  font-size: 0.9rem;
  line-height: 1.4;
}

/* Optional: alternate alignment per row (left, center, right) */
.gallery-item:nth-child(3n+1) { justify-self: start; }
.gallery-item:nth-child(3n+2) { justify-self: center; }
.gallery-item:nth-child(3n+3) { justify-self: end; }
</style>

<div class="gallery-grid">
  {% for item in page.gallery %}
    <figure class="gallery-item">
      <img src="{{ item.image }}" alt="{{ item.alt }}" />
      <figcaption>
        {{ item.caption | markdownify }}
      </figcaption>
    </figure>
  {% endfor %}
</div>
