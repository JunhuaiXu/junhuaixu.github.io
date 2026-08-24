---
layout: single
title: "Correlation Function Imaging"
permalink: /research/correlation-function-imaging/
author_profile: true
hide_title: true
excerpt: "Imaging femtoscopic freeze-out sources from two-particle correlations."
---

<div class="research-detail research-story">
  <section class="detail-hero">
    <p class="section-kicker">Physics Research</p>
    <h1>Correlation Function Imaging</h1>
    <p class="detail-subtitle">Imaging femtoscopic freeze-out sources from two-particle correlations</p>
  </section>

  <section class="visual-abstract visual-abstract--physics" aria-label="Visual abstract for correlation function imaging">
    <div class="visual-abstract__header">
      <p class="visual-abstract__title">Visual Abstract</p>
      <p>Two-particle correlations carry a blurred femtoscopic image of the freeze-out source.</p>
    </div>
    <div class="visual-flow">
      <div class="visual-step">
        <span class="visual-step__icon">HIC</span>
        <span class="visual-step__label">Freeze-out</span>
        <strong>Source function</strong>
        <small>Particles leave an expanding fireball</small>
      </div>
      <div class="visual-step">
        <span class="visual-step__icon">\(C(q)\)</span>
        <span class="visual-step__label">Observable</span>
        <strong>Two-particle correlation</strong>
        <small>Momentum-space femtoscopic signal</small>
      </div>
      <div class="visual-step">
        <span class="visual-step__icon">\(|\Psi|^2\)</span>
        <span class="visual-step__label">Kernel</span>
        <strong>Koonin-Pratt + FSI</strong>
        <small>Quantum statistics and interactions</small>
      </div>
      <div class="visual-step">
        <span class="visual-step__icon">RL</span>
        <span class="visual-step__label">Imaging</span>
        <strong>Richardson-Lucy reconstruction</strong>
        <small>Source imaging without a Gaussian ansatz</small>
      </div>
      <div class="visual-step visual-step--result">
        <span class="visual-step__icon">\(S(r)\)</span>
        <span class="visual-step__label">Source</span>
        <strong>Real-space source image</strong>
        <small>\(pp\) and \(\bar{p}\bar{p}\) share a non-Gaussian source</small>
      </div>
    </div>
  </section>

  <section class="detail-section">
    <p>
      Heavy-ion collisions create tiny, rapidly evolving droplets of strongly interacting matter. After the
      system expands and cools, particles are emitted from the fireball at the freeze-out stage. The spatial
      distribution of these emission points, the freeze-out source function, contains direct information about
      the space-time evolution of the collision system.
    </p>
    <p>
      However, this source distribution is not directly observable. What experiments measure is the two-particle
      correlation function, which describes how the probability of detecting two particles changes with their
      relative momentum. In femtoscopy, this correlation function acts like a blurred image of the emission
      source: it is shaped by quantum statistics and final-state interactions between the emitted particles.
      The key challenge is therefore an inverse problem: can we reconstruct the source distribution from the
      measured correlation function without assuming its shape?
    </p>
  </section>

  <section class="detail-section">
    <h2>Physical Motivation</h2>
    <p>
      Traditional correlation-function analyses often assume that the source function has a Gaussian form. This
      assumption makes the analysis convenient and allows the extraction of HBT radii, but it may also hide
      important physics. If the collision evolves extremely rapidly, the emitted particles may not be fully
      randomized in coordinate space before freeze-out. In that case, the true source can deviate from a
      Gaussian distribution and may preserve information about the early geometry and dynamical evolution of
      the system.
    </p>
    <p>
      My work focuses on developing a nonparametric imaging method that reconstructs the source function from
      experimental correlation functions without imposing a Gaussian shape. The result still depends on the
      physical interaction kernel, whose assumptions must be tested explicitly.
    </p>
    <p>The central physics questions are:</p>
    <ul class="clean-list">
      <li>Can we image the freeze-out source without imposing a Gaussian ansatz?</li>
      <li>Do protons and antiprotons share the same spatial distribution at freeze-out?</li>
      <li>Can source imaging provide coordinate-space evidence for matter-antimatter symmetry?</li>
      <li>Can the same method be extended to three-dimensional imaging and nuclear-structure observables?</li>
    </ul>
  </section>

  <section class="detail-section">
    <h2>Method: From Correlation Functions to Source Images</h2>
    <p>
      The connection between the correlation function <span class="inline-math">\(C(q)\)</span> and the source
      function <span class="inline-math">\(S(r)\)</span> is described by the Koonin-Pratt equation:
    </p>
    <div class="detail-equation">\[
      C(q) = \int d^{3}r\, |\Psi_q(r)|^{2} S(r)
    \]</div>
    <p>
      Here, <span class="inline-math">\(q\)</span> is the relative momentum of the particle pair,
      <span class="inline-math">\(S(r)\)</span> describes the relative spatial distribution of the emitted particles,
      and <span class="inline-math">\(\Psi_q(r)\)</span> is the two-particle wave function including
      final-state interactions. In this sense, the measured correlation function is a convolution of the source
      function with an interaction kernel.
    </p>
    <p>
      This structure is mathematically similar to an optical deblurring problem. In optical imaging, a blurred
      image can be restored if the point-spread function is known. I applied this idea to femtoscopy by combining:
    </p>
    <ul class="clean-list">
      <li>the Richardson-Lucy deblurring algorithm, originally developed for image restoration;</li>
      <li>the Koonin-Pratt formalism, which relates <span class="inline-math">\(C(q)\)</span> and <span class="inline-math">\(S(r)\)</span>;</li>
      <li>the Lednicky-Lyuboshitz model, which describes the final-state interaction between particle pairs.</li>
    </ul>
    <p>
      This framework allows the source distribution and the interaction parameters to be extracted
      simultaneously. In the proton-proton and antiproton-antiproton systems, the interaction is characterized by
      the scattering length <span class="inline-math">\(f_0\)</span> and the effective range
      <span class="inline-math">\(d_0\)</span>. By scanning the interaction parameters and minimizing the
      difference between reconstructed and measured correlation functions, the method determines both the source
      image and the interaction strength.
    </p>
  </section>

  <section class="detail-section">
    <h2>Validation with Model Tests</h2>
    <p>
      Before applying the method to experimental data, I validated the imaging procedure with controlled model
      tests. Starting from a known source function and known proton-proton interaction parameters, I generated a
      correlation function and then added fluctuations to mimic experimental uncertainties. The Richardson-Lucy
      algorithm was then used to reconstruct the original source function.
    </p>
    <p>
      The reconstructed source function was compared with the known input, and its re-projected correlation
      function was checked against the generated correlation. The optimized interaction parameters also returned
      the input values within the model test, providing closure for both the source reconstruction and the
      interaction-parameter extraction.
    </p>
  </section>

  <section class="detail-section">
    <h2>Application to Proton and Antiproton Correlations</h2>
    <p>
      I applied the method to proton-proton and antiproton-antiproton correlation functions measured in Au+Au
      collisions at <span class="inline-math">\(\sqrt{s_{NN}} = 200~\mathrm{GeV}\)</span> by the STAR Collaboration
      at RHIC. The analysis reconstructs the freeze-out source functions for protons and antiprotons directly
      from the experimental correlation functions, without assuming a Gaussian source shape.
    </p>
    <p>
      In the analysis, the effective range was fixed at
    </p>
    <div class="detail-equation">\[
      d_0 = 2.8~\mathrm{fm}.
    \]</div>
    <p>
      The extracted scattering lengths were
    </p>
    <div class="detail-equation">\[
      f_0(pp) = (7.7 \pm 0.2)~\mathrm{fm}, \qquad
      f_0(\bar{p}\bar{p}) = (7.9 \pm 0.3)~\mathrm{fm}.
    \]</div>
    <p>
      These values are consistent between protons and antiprotons, supporting the symmetry of their final-state
      interactions.
    </p>
  </section>

  <section class="detail-section">
    <h2>Main Results</h2>
    <p>
      The reconstructed source functions show two important features.
    </p>
    <p>
      First, within experimental uncertainties, protons and antiprotons share the same freeze-out spatial
      distribution. This provides coordinate-space evidence that matter and antimatter are produced and evolve
      symmetrically in relativistic heavy-ion collisions.
    </p>
    <p>
      Second, both proton and antiproton source functions deviate from the conventional Gaussian assumption.
      The reconstructed source is more concentrated at small relative distances, especially for
      <span class="inline-math">\(r \lt 5~\mathrm{fm}\)</span>, and shows reduced density compared with the Gaussian expectation
      at larger distances. This non-Gaussian structure suggests that the collision evolves so rapidly that the
      system is not fully randomized in coordinate space before freeze-out.
    </p>
    <p>
      This result turns correlation-function analysis from a parameter-fitting method into a direct imaging tool.
      Instead of asking only "what is the Gaussian radius?", the method asks a more general question: what does
      the freeze-out source actually look like?
    </p>
  </section>

  <section class="detail-section">
    <h2>Physical Interpretation</h2>
    <p>
      The non-Gaussian profile shows that a single Gaussian radius does not capture all of the structure retained
      in the measured correlation function. Determining whether that structure originates from collective
      expansion, resonance decays, hadronic rescattering, or other dynamics requires systematic comparisons
      across collision conditions and source models.
    </p>
    <p>
      For the proton-antiproton comparison, the result provides a femtoscopic coordinate-space test of
      matter-antimatter symmetry. Previous analyses had shown similar momentum-space behavior and interaction
      parameters. This imaging work adds the spatial component: protons and antiprotons are emitted from the
      same freeze-out source within uncertainties.
    </p>
  </section>

  <section class="detail-section">
    <h2>My Contributions</h2>
    <ul class="clean-list">
      <li>Developed a Richardson-Lucy-based imaging framework for reconstructing femtoscopic source functions from two-particle correlation functions.</li>
      <li>Combined source imaging with the Lednicky-Lyuboshitz final-state-interaction model to extract both source functions and interaction parameters.</li>
      <li>Validated the inverse-imaging method using controlled model tests with known source functions and interaction parameters.</li>
      <li>Applied the method to STAR proton-proton and antiproton-antiproton correlation functions in Au+Au collisions at <span class="inline-math">\(\sqrt{s_{NN}} = 200~\mathrm{GeV}\)</span>.</li>
      <li>Found that the non-Gaussian proton and antiproton source functions agree within experimental uncertainty.</li>
    </ul>
  </section>

  <section class="detail-section">
    <h2>Further Extension: Three-Dimensional Imaging and Neutron Skin</h2>
    <p>
      This imaging framework was later extended in a subsequent study by Haojie Zhang et al., where I
      contributed as a co-author and provided methodological guidance based on the original correlation-function
      imaging approach.
    </p>
    <p>
      In that work, the Richardson-Lucy algorithm was generalized to reconstruct three-dimensional pion source
      functions from <span class="inline-math">\(\pi^-\pi^-\)</span> correlation functions. The
      method was first tested with simulated Gaussian sources and then applied to HADES Au+Au data at 1.23A GeV,
      where it revealed non-Gaussian features in the extracted source function, particularly at large relative
      distances.
    </p>
    <p>
      The study further used UrQMD simulations of Pb+Pb collisions at 1.5A GeV to investigate whether pion
      femtoscopy is sensitive to the neutron skin thickness of heavy nuclei. By varying the neutron density
      profile in the initial nucleus, the reconstructed source functions were shown to respond to changes in
      neutron skin configuration. This suggests that correlation-function imaging may become a complementary
      probe of neutron density distributions and nuclear structure in heavy-ion collisions.
    </p>
    <p>
      This extension demonstrates the broader potential of the method: from one-dimensional source imaging of
      matter-antimatter freeze-out distributions to three-dimensional femtoscopic reconstruction and possible
      applications in neutron-skin studies.
    </p>
  </section>

  <section class="detail-section">
    <h2>Related Publications</h2>
    <ol class="publication-list">
      <li>
        <span class="publication-label">Primary work</span>
        <strong>J. Xu et al.</strong>, "Imaging Freeze-Out Sources and Extracting Strong Interaction Parameters
        in Relativistic Heavy-Ion Collisions,"
        <a href="https://doi.org/10.1088/0256-307X/42/3/031401" target="_blank" rel="noopener">
          <em>Chinese Physics Letters</em> <strong>42</strong>, 031401 (2025).
        </a>
      </li>
      <li>
        <span class="publication-label">Further extension</span>
        <strong>H. Zhang, J. Xu et al.</strong>, "Probing the three-dimensional emission source and neutron skin
        via \(\pi\)-\(\pi\) correlations in heavy-ion collisions,"
        <a href="https://doi.org/10.1103/jdsn-p3v4" target="_blank" rel="noopener">
          <em>Physical Review C</em> <strong>113</strong>, 034904 (2026).
        </a>
      </li>
    </ol>
  </section>

  <div class="detail-actions">
    <a class="home-button" href="/#physics-research">Back to Physics Research</a>
  </div>
</div>
