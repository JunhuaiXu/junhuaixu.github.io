---
layout: single
title: "Correlation Function Imaging"
permalink: /research/correlation-function-imaging/
author_profile: true
excerpt: "Imaging femtoscopic freeze-out sources from two-particle correlations."
---

<div class="research-detail research-story">
  <section class="detail-hero">
    <p class="section-kicker">Physics Research</p>
    <h1>Correlation Function Imaging</h1>
    <p class="detail-subtitle">Imaging femtoscopic freeze-out sources from two-particle correlations</p>
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
      Traditional correlation-function analyses often assume that the emission source has a Gaussian form. This
      assumption makes the analysis convenient and allows the extraction of HBT radii, but it may also hide
      important physics. If the collision evolves extremely rapidly, the emitted particles may not be fully
      randomized in coordinate space before freeze-out. In that case, the true source can deviate from a
      Gaussian distribution and may preserve information about the early geometry and dynamical evolution of
      the system.
    </p>
    <p>
      My work focuses on developing a model-independent imaging method that directly reconstructs the source
      function from experimental correlation functions. This allows us to study not only the source size, but
      also its detailed shape.
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
      The connection between the correlation function <span class="inline-math">C(q)</span> and the source
      function <span class="inline-math">S(r)</span> is described by the Koonin-Pratt equation:
    </p>
    <p class="detail-equation">
      C(q) = &int; d<sup>3</sup>r |&Psi;<sub>q</sub>(r)|<sup>2</sup> S(r)
    </p>
    <p>
      Here, <span class="inline-math">q</span> is the relative momentum of the particle pair,
      <span class="inline-math">S(r)</span> describes the relative spatial distribution of the emitted particles,
      and <span class="inline-math">&Psi;<sub>q</sub>(r)</span> is the two-particle wave function including
      final-state interactions. In this sense, the measured correlation function is a convolution of the source
      function with an interaction kernel.
    </p>
    <p>
      This structure is mathematically similar to an optical deblurring problem. In optical imaging, a blurred
      image can be restored if the point-spread function is known. I applied this idea to femtoscopy by combining:
    </p>
    <ul class="clean-list">
      <li>the Richardson-Lucy deblurring algorithm, originally developed for image restoration;</li>
      <li>the Koonin-Pratt formalism, which relates <span class="inline-math">C(q)</span> and <span class="inline-math">S(r)</span>;</li>
      <li>the Lednicky-Lyuboshitz model, which describes the final-state interaction between particle pairs.</li>
    </ul>
    <p>
      This framework allows the source distribution and the interaction parameters to be extracted
      simultaneously. In the proton-proton and antiproton-antiproton systems, the interaction is characterized by
      the scattering length <span class="inline-math">f<sub>0</sub></span> and the effective range
      <span class="inline-math">d<sub>0</sub></span>. By scanning the interaction parameters and minimizing the
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
      The reconstructed source converged back to the known input distribution. Importantly, tests with different
      initial trial source functions led to the same final result, demonstrating the robustness of the iterative
      imaging procedure. The optimized interaction parameters also converged to the input values, confirming that
      the method can recover both the source function and the interaction strength.
    </p>
  </section>

  <section class="detail-section">
    <h2>Application to Proton and Antiproton Correlations</h2>
    <p>
      I applied the method to proton-proton and antiproton-antiproton correlation functions measured in Au+Au
      collisions at <span class="inline-math">&radic;s<sub>NN</sub> = 200 GeV</span> by the STAR Collaboration
      at RHIC. The analysis reconstructs the freeze-out source functions for protons and antiprotons directly
      from the experimental correlation functions, without assuming a Gaussian source shape.
    </p>
    <p>
      In the analysis, the effective range was fixed at <span class="inline-math">d<sub>0</sub> = 2.8 fm</span>,
      and the extracted scattering lengths were
      <span class="inline-math">f<sub>0</sub>(pp) = (7.7 &plusmn; 0.2) fm</span> and
      <span class="inline-math">f<sub>0</sub>(&bar;p&bar;p) = (7.9 &plusmn; 0.3) fm</span>. These values are
      consistent between protons and antiprotons, supporting the symmetry of their final-state interactions.
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
      <span class="inline-math">r &lt; 5 fm</span>, and shows reduced density compared with the Gaussian expectation
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
      The non-Gaussian source profile indicates that the freeze-out distribution retains information about the
      dynamical evolution of the collision. In a fully randomized system, the central-limit picture would
      naturally lead to a Gaussian-like source distribution. The observed deviation therefore supports the
      picture of an ultrafast collision, in which part of the spatial information from the early-stage geometry
      remains visible at freeze-out.
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
      <li>Combined source imaging with the Lednicky-Lyuboshitz final-state-interaction model to extract both source distributions and interaction parameters.</li>
      <li>Validated the inverse-imaging method using controlled model tests with known source functions and interaction parameters.</li>
      <li>Applied the method to STAR proton-proton and antiproton-antiproton correlation functions in Au+Au collisions at <span class="inline-math">&radic;s<sub>NN</sub> = 200 GeV</span>.</li>
      <li>Demonstrated identical non-Gaussian freeze-out source functions for protons and antiprotons, providing coordinate-space evidence for matter-antimatter symmetry.</li>
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
      functions from <span class="inline-math">&pi;<sup>-</sup>&pi;<sup>-</sup></span> correlation functions. The
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
        in Relativistic Heavy-Ion Collisions," <em>Chinese Physics Letters</em> <strong>42</strong>, 031401
        (2025).
      </li>
      <li>
        <span class="publication-label">Further extension</span>
        <strong>H. Zhang, J. Xu et al.</strong>, "Probing the three-dimensional emission source and neutron skin
        via pion-pion correlations in heavy-ion collisions," <em>Physical Review C</em> <strong>113</strong>,
        034904 (2026).
      </li>
    </ol>
  </section>

  <div class="detail-actions">
    <a class="home-button" href="/#physics-research">Back to Physics Research</a>
  </div>
</div>
