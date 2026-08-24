---
layout: single
title: "Graph Neural Networks for Neutrino Event Reconstruction"
permalink: /ai/gnn-neutrino-reconstruction/
author_profile: true
hide_title: true
excerpt: "Geometry-aware graph reconstruction for sparse underwater neutrino-detector events."
---

<div class="research-detail research-story">
  <section class="detail-hero">
    <p class="section-kicker">AI &amp; Computational Methods</p>
    <h1>Graph Neural Networks for Neutrino Event Reconstruction</h1>
    <p class="detail-subtitle">From sparse detector hits to topology, direction, energy, and oscillation inference</p>
  </section>

  <figure class="detail-figure">
    <img src="/assets/images/gnn-neutrino/reconstruction-workflow.png" alt="Graph-neural-network reconstruction workflow for sparse underwater neutrino-detector events">
    <figcaption>
      Sparse detector responses are represented as geometry-aware graphs and processed with Edge Convolution
      before task-specific topology, direction, and energy reconstruction.
    </figcaption>
  </figure>

  <section class="detail-section">
    <h2>Physics Problem</h2>
    <p>
      A large-volume underwater neutrino detector records sparse optical signals rather than the incident
      neutrino directly. Oscillation measurements therefore depend on reconstructing the event topology,
      incoming direction, and energy from irregular detector observations while retaining the information needed
      for the final physics fit.
    </p>
    <p>
      I developed this workflow for a compact underwater detector concept motivated by TRIDENT. The study is a
      simulation-stage research project and is not presented as an official detector configuration or a
      production reconstruction system.
    </p>
  </section>

  <section class="detail-section">
    <h2>Geometry-Aware Event Representation</h2>
    <p>
      Each fired hybrid digital optical module is represented as a graph node. Node features include its
      three-dimensional position, relative first-hit time, first-photon energy, and photoelectron count. The
      graph combines nearest-neighbor connections with links that preserve the detector's vertical geometry.
    </p>
    <p>
      This representation keeps the spatial structure of track-like and cascade-like events without forcing the
      detector into a regular image grid. Edge Convolution blocks aggregate local relationships, global mean-max
      pooling summarizes the event, and separate prediction heads reconstruct topology, direction, and energy.
    </p>
  </section>

  <section class="detail-section">
    <h2>From Reconstruction to Oscillation Physics</h2>
    <p>
      Model performance is not evaluated only through classification and regression metrics. The reconstructed
      direction and energy define oscillation-sensitive event templates, while the topology classifier selects
      the track-like sample used in the fit. I connected these outputs to a likelihood analysis and tested the
      full chain with pseudo-data generated at known oscillation parameters.
    </p>
    <div class="result-box">
      <span class="result-box__label">Physics-Level Validation</span>
      <strong>64,273 selected benchmark events</strong>
      <p>
        The closure study recovered the input values of
        <span class="inline-math">\(\sin^2\theta_{23}\)</span> and
        <span class="inline-math">\(\Delta m^2_{32}\)</span> within uncertainty.
      </p>
    </div>
  </section>

  <section class="detail-section">
    <h2>Implementation and Validation</h2>
    <ul class="clean-list">
      <li>Built the atmospheric-neutrino simulation-to-reconstruction chain using HONDA fluxes, FLUKA interactions, and Geant4 detector transport.</li>
      <li>Implemented dataset construction, GPU training, and full-event inference with PyTorch Geometric and Edge Convolution.</li>
      <li>Evaluated topology probabilities together with direction and energy residuals on controlled simulation samples.</li>
      <li>Connected reconstructed outputs to oscillation-sensitive templates and likelihood-based closure tests.</li>
      <li>Operated the analysis through HTCondor batch workflows on a university GPU cluster.</li>
    </ul>
  </section>

  <section class="detail-section">
    <h2>Current Status</h2>
    <p>
      This work is at the manuscript-preparation stage. The current public description therefore focuses on the
      documented simulation, reconstruction, and closure workflow and does not imply peer-reviewed publication,
      detector deployment, or online reconstruction performance.
    </p>
  </section>

  <div class="detail-actions">
    <a class="home-button" href="/#ai-methods">Back to AI &amp; Computational Methods</a>
  </div>
</div>
