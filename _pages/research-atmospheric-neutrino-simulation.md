---
layout: single
title: "Atmospheric Neutrino Simulation"
permalink: /research/atmospheric-neutrino-simulation/
author_profile: true
hide_title: true
excerpt: "Exploring compact deep-sea Cherenkov arrays for GeV atmospheric-neutrino oscillation measurements."
---

<div class="research-detail research-story atmospheric-story">
  <section class="detail-hero">
    <p class="section-kicker">Physics Research</p>
    <h1>Atmospheric Neutrino Simulation</h1>
    <p class="detail-subtitle">A compact deep-sea Cherenkov concept for GeV atmospheric-neutrino oscillations</p>
  </section>

  <section class="detail-section">
    <h2>Atmospheric Neutrinos as an Oscillation Probe</h2>
    <p>
      Large neutrino telescopes use naturally transparent ice or water as both the interaction target and the
      detection medium. IceCube in Antarctic ice, KM3NeT in the Mediterranean Sea, and Baikal-GVD in Lake Baikal
      instrument vast volumes with optical modules that record Cherenkov photons from neutrino-induced charged
      particles. IceCube's denser DeepCore infill and KM3NeT's lower-energy ORCA array extend this technique into
      the GeV range, where atmospheric-neutrino data can be used to measure oscillation parameters.
    </p>
    <p>
      Atmospheric neutrinos are produced in cosmic-ray air showers and reach the detector from all zenith
      directions. Down-going neutrinos travel only tens of kilometers, whereas up-going neutrinos can cross nearly
      the full diameter of the Earth. Together with their broad energy spectrum, this provides a wide range of
      <span class="inline-math">\(L/E\)</span> over which muon-neutrino disappearance can be observed.
    </p>

    <div class="atmospheric-equation">
      <p class="atmospheric-equation__label">Muon-neutrino survival probability</p>
      <div class="detail-equation">
        \[
        \begin{aligned}
        P(\nu_\mu\!\rightarrow\!\nu_\mu)
        &\simeq 1-\sin^2(2\theta_{23})\\
        &\quad\times\sin^2\!\left(1.27\,\Delta m^2_{32}\frac{L}{E}\right).
        \end{aligned}
        \]
      </div>
      <p class="atmospheric-equation__note">
        In this two-flavor vacuum approximation, \(L\) is measured in kilometers, \(E\) in GeV, and
        \(\Delta m^2_{32}\) in \(\mathrm{eV}^2\). The mixing angle \(\theta_{23}\) controls the disappearance
        amplitude, while \(|\Delta m^2_{32}|\) sets the oscillation frequency in \(L/E\). Quantitative calculations
        require three-flavor propagation through the Earth's matter profile.
      </p>
    </div>

    <div class="atmospheric-baseline">
      <figure class="detail-figure atmospheric-baseline__figure">
        <img src="/assets/images/atmospheric-neutrino/atmospheric-baseline-l-over-e.png"
             alt="Atmospheric-neutrino propagation baseline through the Earth and its relation to zenith angle and energy reconstruction">
        <figcaption>
          Baselines range from roughly \(20~\mathrm{km}\) for down-going events to
          \(1.3\times10^4~\mathrm{km}\) for neutrinos crossing the Earth.
        </figcaption>
      </figure>

      <div class="atmospheric-baseline__copy">
        <h3>From detector observables to the oscillation pattern</h3>
        <p>
          The detector records photon arrival times and charges rather than \(L\) or \(E\) directly. Event
          reconstruction estimates the topology, zenith direction, and neutrino energy. The zenith direction,
          together with an atmospheric production-height model and the Earth's geometry, gives
          <span class="inline-math">\(L_{\rm reco}\)</span>.
        </p>
        <p>
          A reconstructed \(L/E\) projection makes the oscillation phase intuitive, while precision analyses
          commonly retain the two-dimensional
          <span class="inline-math">\((E_{\rm reco},\cos\theta_{z,\rm reco})\)</span> distribution. Detector
          resolution, selection efficiency, and topology misclassification determine how much oscillation
          information remains visible.
        </p>
      </div>
    </div>
  </section>

  <section class="detail-section">
    <h2>The Hai-Ling/TRIDENT Opportunity</h2>
    <p>
      TRIDENT, nicknamed Hai-Ling, is being developed in the South China Sea as a next-generation deep-sea
      neutrino telescope for high-energy astrophysical source discovery and all-flavor observations. Its
      pathfinder program has characterized the deep-sea site and measured key optical properties of the water,
      while the broader detector program is developing hybrid digital optical modules, in situ calibration
      methods, and the simulation and deployment framework needed for a large underwater array.
    </p>
    <p>
      These environmental measurements and detector technologies create an opportunity to investigate a
      complementary question at lower energy. The sparse, large-volume geometry favored for high-energy source
      searches is not automatically optimal for GeV atmospheric neutrinos. Our study therefore uses the South
      China Sea environment and related detector technologies as inputs to a separate, GeV-oriented compact
      reference geometry.
    </p>
  </section>

  <section class="detail-section">
    <h2>Why a More Compact Detector Array?</h2>
    <p>
      GeV neutrino interactions produce less Cherenkov light and more spatially compact event patterns than
      TeV to PeV events. A GeV-oriented detector therefore requires denser optical sampling, adequate containment,
      and calibrated timing and charge measurements. These features set the energy threshold and determine
      whether direction, energy, and topology can be reconstructed precisely enough for the oscillation structure
      to survive detector smearing.
    </p>
    <div class="result-box atmospheric-question">
      <span class="result-box__label">Research question</span>
      <strong>
        Can a compact deep-sea Cherenkov array retain enough topology, direction, and energy information to
        support an atmospheric-neutrino oscillation measurement in the GeV range?
      </strong>
    </div>
    <ul class="clean-list">
      <li>Dense optical sampling improves photon statistics for low-energy events.</li>
      <li>Containment and optical calibration improve the stability of energy and direction reconstruction.</li>
      <li>Topology classification defines oscillation-sensitive samples and supports background rejection.</li>
      <li>
        Reconstructed energy and zenith angle provide either \(L_{\rm reco}/E_{\rm reco}\) or a two-dimensional
        oscillation observable.
      </li>
    </ul>
  </section>

  <section class="detail-section">
    <h2>Current Status</h2>
    <div class="quiet-panel">
      <span>Detector simulation, event reconstruction, and oscillation studies are in progress. Quantitative results will be added as the analysis develops.</span>
    </div>
  </section>

  <div class="detail-actions">
    <a class="home-button" href="/#physics-research">Back to Physics Research</a>
  </div>
</div>
