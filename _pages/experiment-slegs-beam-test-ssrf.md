---
layout: single
title: "SLEGS Beam Test at SSRF"
permalink: /experiments/slegs-beam-test-ssrf/
author_profile: true
excerpt: "CsI(Tl) gamma-ray response calibration and detector-performance validation."
---

<div class="research-detail research-story">
  <section class="detail-hero">
    <p class="section-kicker">Experiments &amp; Collaborations</p>
    <h1>SLEGS Beam Test at SSRF</h1>
    <p class="detail-subtitle">CsI(Tl) \(\gamma\)-ray response calibration with laser-Compton \(\gamma\) beams</p>
  </section>

  <section class="detail-section">
    <h2>Overview</h2>
    <p>
      In January 2025, I participated in a beam test at the Shanghai Laser Electron Gamma Source (SLEGS) at the
      Shanghai Synchrotron Radiation Facility (SSRF). The goal was to characterize the response of CsI(Tl)
      crystals to energetic photons below 20 MeV, providing calibration and detector-performance input for
      high-energy \(\gamma\)-ray measurements in nuclear reaction experiments.
    </p>
    <p>
      This experiment connects detector instrumentation with physics analysis. Reliable \(\gamma\)-ray spectra
      require more than measuring deposited energy: the detector response must be understood, validated, and
      propagated into the final reconstruction and model comparison.
    </p>
  </section>

  <section class="detail-section">
    <h2>Experimental Context</h2>
    <p>
      The CSHINE-Gamma hodoscope uses CsI(Tl) crystals to detect high-energy photons emitted in heavy-ion
      collisions. These photons are key observables in studies of bremsstrahlung emission and short-range
      correlations, but their measurement is affected by shower development, partial energy deposition, leakage,
      detector thresholds, and finite energy resolution.
    </p>
    <p>
      SLEGS provides a controlled \(\gamma\)-ray beam environment for validating the response of the detector to
      energetic photons. By comparing measured detector signals with Geant4 simulations, the experiment tests
      whether the simulated response matrix can reliably describe the behavior of the CsI(Tl) detector system.
    </p>
  </section>

  <section class="detail-section">
    <h2>Detector Response Validation</h2>
    <p>
      A central task was to determine whether the CsI(Tl) crystal response remains approximately linear for
      energetic photons below 20 MeV. This validation is important because the detector response matrix is later
      used in both forward-folding comparisons and Richardson-Lucy unfolding of measured
      <span class="inline-math">\(\gamma\)</span>-ray spectra.
    </p>
    <p>
      The analysis combined beam-test data, detector calibration, response simulations, and systematic checks.
      Agreement between the measured response and simulated response supports the use of Geant4-based detector
      filtering in precision \(\gamma\)-ray spectrum analysis.
    </p>
  </section>

  <section class="detail-section">
    <h2>Connection to SRC Measurements</h2>
    <p>
      In SRC studies, the high-energy tail of the bremsstrahlung <span class="inline-math">\(\gamma\)</span>-ray
      spectrum is sensitive to high-momentum nucleons in the initial nucleus. Detector-response effects can
      distort this spectral shape, so response validation is a necessary part of extracting a reliable
      <span class="inline-math">\(R_{\mathrm{HMT}}\)</span> constraint.
    </p>
    <p>
      The SLEGS beam test therefore supports the experimental foundation of the SRC program: it helps connect
      raw detector signals to physical \(\gamma\)-ray spectra, and it strengthens the reliability of both
      detector-filtered transport-model comparisons and unfolded-spectrum analyses.
    </p>
  </section>

  <section class="detail-section">
    <h2>My Contributions</h2>
    <ul class="clean-list">
      <li>Participated in the SLEGS beam test campaign at SSRF for CsI(Tl) \(\gamma\)-ray response studies.</li>
      <li>Contributed to detector-performance validation for energetic photons below 20 MeV.</li>
      <li>Connected beam-test response studies with CSHINE-Gamma calibration and high-energy \(\gamma\)-ray spectrum analysis.</li>
      <li>Used detector-response validation to support Geant4-based response filtering and Richardson-Lucy unfolding in SRC measurements.</li>
    </ul>
  </section>

  <section class="detail-section">
    <h2>Related Publication</h2>
    <ol class="publication-list">
      <li>
        <strong>J. Xu et al.</strong>,
        "Linear response of CsI(Tl) crystal to energetic photons below 20 MeV,"
        <a href="https://doi.org/10.1016/j.nima.2025.170787" target="_blank" rel="noopener">
          <em>Nuclear Instruments and Methods in Physics Research Section A</em> <strong>1080</strong>, 170787
          (2025).
        </a>
      </li>
    </ol>
  </section>

  <div class="detail-actions">
    <a class="home-button" href="/#experiments">Back to Experiments &amp; Collaborations</a>
  </div>
</div>
