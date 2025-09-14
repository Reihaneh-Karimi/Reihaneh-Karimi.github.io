---
layout: default
title: "My Research Projects"
permalink: /project/
---

<h1>My Research Projects</h1>

<section class="projects-gallery">

  <!-- Project 1 -->
  <div class="project-card">
    <img src="/assets/images/iring.jpg" alt="Radio Continuum Aperture Photometry">
    <h3>Radio Continuum Aperture Photometry of Galaxies (IPM, Effelsberg Telescope Data)</h3>
    <p>
      At the Institute for Research in Fundamental Sciences (IPM), I analyzed radio continuum maps from
      the KINGFISHER sample observed with the Effelsberg Telescope. Using the Astronomical Image Processing System (AIPS),
      I performed aperture photometry of nearby galaxies to measure their integrated flux densities and
      created polarized intensity (PI) maps from the Stokes Q and U maps. This work provided insights into
      the radio emission of star-forming galaxies and enhanced my experience in radio astronomy data
      reduction and scientific interpretation.
    </p>
  </div>

  <!-- Project 2 -->
  <div class="project-card">
    <img src="/assets/images/HPC.jpg" alt="Hyperspectral Camera Imaging">
    <h3>Hyperspectral Camera Imaging (Leiden University, Jul 2024 – Aug 2024)</h3>
    <p>
      During a short research placement at the Leiden Quantum Matter & Optics Department, I worked with a
      state-of-the-art hyperspectral camera to investigate material properties. I became proficient in
      processing and analyzing hyperspectral images, learning how to extract and interpret spectral
      signatures for detailed material characterization. This project strengthened both my technical skills
      in advanced optical instrumentation and my ability to handle and analyze high-dimensional datasets.
    </p>
  </div>

  <!-- Project 3 -->
  <div class="project-card">
    <img src="/assets/images/pycbc.jpg" alt="Gravitational-Wave Data Analysis with PyCBC">
    <h3>Gravitational-Wave Data Analysis with PyCBC</h3>
    <p>
      I worked with the PyCBC Python library, a key toolkit used by the LIGO and Virgo collaborations to
      detect and analyze gravitational waves. Using real and simulated data, I explored techniques for
      identifying astrophysical sources from compact binary mergers and extracting their physical
      parameters. This project deepened my understanding of gravitational-wave astronomy and provided
      hands-on experience with professional analysis pipelines used in current gravitational-wave research.
    </p>
  </div>

</section>

<style>
.projects-gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2rem auto;
  max-width: 1200px;
  padding: 0 1rem;
}

.project-card {
  background: #fff;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  padding: 1.5rem;
  text-align: center;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.project-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 8px 20px rgba(0,0,0,0.15);
}

.project-card img {
  max-width: 100%;
  height: auto;
  border-radius: 12px;
  margin-bottom: 1rem;
}

.project-card h3 {
  font-size: 1.2rem;
  margin: 0.5rem 0 1rem;
  color: #333;
}

.project-card p {
  font-size: 0.95rem;
  line-height: 1.6;
  color: #555;
  text-align: justify;
}
</style>
