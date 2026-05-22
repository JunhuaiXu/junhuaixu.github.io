---
layout: single
title: "SLEGS Beam Test at SSRF"
permalink: /experiments/slegs-beam-test-ssrf/
redirect_from:
  - /research/slegs-beam-test/
author_profile: true
excerpt: "High-energy gamma-ray response calibration of CsI(Tl) crystals for CSHINE-Gamma."
---

<div class="research-detail research-story">
  <section class="detail-hero">
    <p class="section-kicker">Detector Instrumentation</p>
    <h1>SLEGS Beam Test at SSRF</h1>
    <p class="detail-subtitle">
      High-energy \(\gamma\)-ray response calibration of CsI(Tl) crystals for CSHINE-Gamma
    </p>
  </section>

  <figure class="detail-figure">
    <img src="/assets/images/slegs-beam-test/slegs-team-photo.jpg" alt="SLEGS beam test team photo">
    <figcaption>
      SLEGS beam test at the Shanghai Synchrotron Radiation Facility. This experiment provided a direct
      high-energy \(\gamma\)-ray calibration benchmark for the CsI(Tl)-based CSHINE-Gamma hodoscope.
    </figcaption>
  </figure>

  <section class="detail-section">
    <h2>Motivation</h2>
    <p>
      High-energy \(\gamma\)-ray spectroscopy is a central part of my work on bremsstrahlung \(\gamma\) rays in
      heavy-ion collisions. In the CSHINE experiment, a CsI(Tl)-based \(\gamma\)-ray hodoscope is used to measure
      energetic photons emitted from nuclear reactions. These \(\gamma\) rays can deposit tens of MeV in a
      crystal, while standard radioactive sources such as \(^{60}\mathrm{Co}\) and natural \(\mathrm{ThO}_2\)
      provide calibration points only up to about 2.6 MeV.
    </p>
    <p>
      This large extrapolation makes the linearity of the CsI(Tl) response a key systematic issue. Any
      non-linearity in the detector response can distort the reconstructed \(\gamma\)-ray spectrum and propagate
      into the extracted physical observables. Therefore, a dedicated high-energy \(\gamma\)-ray beam test was
      needed to validate the detector response and quantify the calibration uncertainty.
    </p>
  </section>

  <section class="detail-section">
    <h2>Experimental Setup</h2>
    <p>
      The beam test was performed at the Shanghai Laser Electron Gamma Source (SLEGS) beamline of the Shanghai
      Synchrotron Radiation Facility (SSRF). SLEGS provides tunable quasi-monochromatic \(\gamma\)-ray beams
      through Compton scattering between laser photons and electrons, making it an ideal facility for testing
      detector response at well-defined \(\gamma\)-ray energies.
    </p>
    <p>
      In this experiment, the CsI(Tl) crystal detectors were tested with six high-energy \(\gamma\)-ray beam
      settings below 20 MeV. A calibrated BGO detector was used as a reference monitor for measuring the beam
      energy profiles, while the CsI(Tl) crystal under study was placed on the test bench between the
      \(\gamma\)-ray exit window and the BGO detector.
    </p>
    <p>
      The \(\gamma\)-ray beam energies used in the analysis covered approximately 4.9, 7.6, 10.2, 13.0, 15.9,
      and 17.6 MeV after unfolding the BGO detector response. These beam points allowed the CsI(Tl) response to
      be tested directly in the energy region relevant for high-energy \(\gamma\)-ray spectroscopy.
    </p>
  </section>

  <figure class="detail-figure detail-figure--placeholder">
    <div class="detail-figure__placeholder">SLEGS beamline setup schematic</div>
    <figcaption>
      Schematic of the SLEGS beamline setup. The quasi-monochromatic \(\gamma\) beam is measured with a reference
      BGO detector, while the CsI(Tl) detector is placed along the beamline for response calibration.
    </figcaption>
  </figure>

  <section class="detail-section">
    <h2>Detector and Readout</h2>
    <p>
      The tested CsI(Tl) detector units are the same type as those used in CSHINE-Gamma. Each crystal has
      dimensions of \(70~\mathrm{mm} \times 70~\mathrm{mm} \times 250~\mathrm{mm}\) and is coupled to a
      photomultiplier tube. The detector system uses a dual-range readout scheme: a high-gain channel for
      low-energy calibration sources and a low-gain channel for high-energy \(\gamma\) rays.
    </p>
    <p>
      This dual-range strategy is important because the same detector must cover both radioactive-source
      calibration peaks near a few MeV and high-energy \(\gamma\)-ray deposits extending to tens of MeV. A
      reliable bridge between the two readout ranges is therefore required for the CSHINE-Gamma energy
      calibration.
    </p>
  </section>

  <section class="detail-section">
    <h2>Analysis Strategy</h2>
    <p>
      The analysis combined experimental spectra with Geant4 detector-response simulations. For each beam
      energy, the original \(\gamma\)-ray energy profile was first obtained using the calibrated BGO detector.
      This beam profile was then used as the input to Geant4 simulations of the CsI(Tl) crystal.
    </p>
    <p>
      The simulated CsI(Tl) response spectra account for energy leakage, finite energy resolution, and the
      detector geometry. By comparing the simulated response with the measured CsI(Tl) spectra, the peak
      positions of the detector response were extracted and used to construct the high-energy calibration curve.
    </p>
    <p>
      Both linear and quadratic fits were applied to the calibration points. The difference between these fits was
      used to evaluate the possible non-linearity of the CsI(Tl) response and its contribution to the systematic
      uncertainty of high-energy \(\gamma\)-ray measurements.
    </p>
  </section>

  <figure class="detail-figure detail-figure--placeholder">
    <div class="detail-figure__placeholder">CsI(Tl) response spectra and Geant4 simulations</div>
    <figcaption>
      Comparison between measured CsI(Tl) response spectra and Geant4 simulations. The agreement validates the
      detector-response model used for high-energy \(\gamma\)-ray calibration.
    </figcaption>
  </figure>

  <section class="detail-section detail-section--result">
    <h2>Main Result</h2>
    <p>
      The beam-test results show that the CsI(Tl) crystals exhibit a good linear response to \(\gamma\) rays
      below 20 MeV. The quadratic contribution to the calibration curve is statistically insignificant for the
      tested detector units, and the relative contribution of the quadratic term is at the level of approximately
      2.6%-4.5%.
    </p>
    <p>
      The comparison between linear and quadratic calibration schemes indicates that the possible non-linearity
      of the CsI(Tl) response introduces a systematic uncertainty at the level of about 4%. This uncertainty was
      then propagated to the reconstructed \(\gamma\)-ray spectra in CSHINE heavy-ion experiments.
    </p>
    <div class="result-box">
      <span class="result-box__label">Key Result</span>
      <strong>CsI(Tl) non-linearity &lt; 4% below 20 MeV</strong>
      <p>
        High-energy \(\gamma\)-ray response validation for CSHINE-Gamma using quasi-monochromatic photon beams at
        SLEGS.
      </p>
    </div>
  </section>

  <figure class="detail-figure detail-figure--placeholder">
    <div class="detail-figure__placeholder">CsI(Tl) linearity test below 20 MeV</div>
    <figcaption>
      Linearity test of CsI(Tl) detectors. Linear and quadratic fits to the high-energy \(\gamma\)-ray response
      are consistent within a few percent, supporting the use of a linear calibration scheme with quantified
      systematic uncertainty.
    </figcaption>
  </figure>

  <section class="detail-section">
    <h2>Impact on CSHINE-Gamma Measurements</h2>
    <p>
      This beam test provided the calibration foundation for precision \(\gamma\)-ray measurements with
      CSHINE-Gamma. In the SRC experiment, bremsstrahlung \(\gamma\) rays from
      <span class="inline-math">\(^{124}\mathrm{Sn}+^{124}\mathrm{Sn}\)</span> collisions were used to probe
      SRC-induced high-momentum nucleons. The reliability of that \(\gamma\)-ray spectrum depends directly on
      the calibration and response characterization of the CsI(Tl) hodoscope.
    </p>
    <p>
      The SLEGS beam test made it possible to quantify the detector-response uncertainty rather than treating it
      as an uncontrolled extrapolation from low-energy radioactive sources. This is essential for extracting
      physical information from the high-energy end of the \(\gamma\)-ray spectrum, where SRC effects are most
      visible.
    </p>
  </section>

  <section class="detail-section">
    <h2>My Contributions</h2>
    <ul class="clean-list">
      <li>Performed high-energy \(\gamma\)-ray response studies of CsI(Tl) crystals using quasi-monochromatic photon beams at SLEGS.</li>
      <li>Analyzed CsI(Tl) response spectra and extracted peak positions for multiple \(\gamma\)-ray beam energies.</li>
      <li>Developed Geant4 detector-response simulations to account for energy leakage, finite resolution, and detector geometry.</li>
      <li>Validated the dual-range calibration scheme connecting low-energy radioactive-source calibration with high-energy \(\gamma\)-ray response.</li>
      <li>Quantified the non-linearity of the CsI(Tl) response and propagated the resulting systematic uncertainty to CSHINE-Gamma measurements.</li>
      <li>Established a calibration methodology supporting precision bremsstrahlung \(\gamma\)-ray spectroscopy in heavy-ion collision experiments.</li>
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
