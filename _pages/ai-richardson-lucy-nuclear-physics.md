---
layout: single
title: "Richardson-Lucy Reconstruction in Nuclear Physics"
permalink: /ai/richardson-lucy-nuclear-physics/
author_profile: true
excerpt: "Bayesian deblurring, inverse problems, and physics-informed reconstruction."
---

<div class="research-detail research-story">
  <section class="detail-hero">
    <p class="section-kicker">AI &amp; Machine Learning / Scientific Computing / Inverse Problems</p>
    <h1>Richardson-Lucy Reconstruction in Nuclear Physics</h1>
    <p class="detail-subtitle">Bayesian deblurring, inverse problems, and physics-informed reconstruction</p>
  </section>

  <section class="detail-section">
    <p>
      Many measurements in nuclear physics are indirect. Experiments do not always observe the physical quantity
      of interest directly; instead, they measure a blurred or transformed version of it. A detector response can
      smear an original \(\gamma\)-ray spectrum. A two-particle correlation function can encode, but not directly
      reveal, the freeze-out source distribution. In both cases, the core computational problem is an inverse
      problem:
    </p>
    <div class="detail-equation">\[
      \text{measured distribution}
      =
      \text{response kernel}
      \otimes
      \text{hidden physical distribution}.
    \]</div>
    <p>
      My work develops and applies the Richardson-Lucy (RL) algorithm as a Bayesian iterative reconstruction
      method for such inverse problems in nuclear physics. Rather than treating RL as a black-box numerical tool,
      I use it as a physics-informed inference framework, where the response kernel is constructed from detector
      simulations, two-particle wave functions, or final-state-interaction models.
    </p>
    <p>
      This research connects nuclear experimental analysis with machine-learning concepts such as probabilistic
      inference, non-negative reconstruction, iterative optimization, large response-matrix computation,
      regularization, and uncertainty propagation.
    </p>
  </section>

  <section class="detail-section">
    <h2>Algorithmic Principle</h2>
    <p>
      The Richardson-Lucy algorithm was originally developed for optical image deblurring. In a typical
      deblurring problem, a true distribution <span class="inline-math">\(\mathcal{F}(\mu)\)</span> is not
      directly observed. Instead, the measured distribution <span class="inline-math">\(f(\nu)\)</span> is related
      to the true distribution through a conditional probability kernel:
    </p>
    <div class="detail-equation">\[
      f(\nu)=\int d\mu\,P(\nu|\mu)\mathcal{F}(\mu).
    \]</div>
    <p>
      Here, <span class="inline-math">\(P(\nu|\mu)\)</span> is the response function: the probability that an
      object with true property <span class="inline-math">\(\mu\)</span> is measured as
      <span class="inline-math">\(\nu\)</span>. The goal is to recover
      <span class="inline-math">\(\mathcal{F}(\mu)\)</span> from the measured
      <span class="inline-math">\(f(\nu)\)</span> and the known response kernel.
    </p>
    <p>
      The RL algorithm solves this problem iteratively. Starting from an initial trial distribution, it predicts
      the measured distribution, compares it with the actual measurement, and updates the hidden distribution
      through a multiplicative amplification factor:
    </p>
    <div class="detail-equation">\[
      \mathcal{F}^{(r+1)}(\mu)
      =
      \mathcal{F}^{(r)}(\mu)A^{(r)}(\mu).
    \]</div>
    <p>
      The multiplicative update naturally preserves non-negativity, which is crucial for physical distributions
      such as spectra, source functions, and probability densities.
    </p>
    <p>
      For numerical implementation, the continuous equation is discretized into a matrix problem:
    </p>
    <div class="detail-equation">\[
      e_i=\sum_j D_{ij}\mathcal{E}_j.
    \]</div>
    <p>
      Here, <span class="inline-math">\(e_i\)</span> is the measured distribution,
      <span class="inline-math">\(\mathcal{E}_j\)</span> is the original distribution to be reconstructed, and
      <span class="inline-math">\(D_{ij}\)</span> is the response matrix. The reconstruction is performed by
      repeated matrix operations instead of direct matrix inversion, which is important because direct inversion
      is often unstable when data contain statistical fluctuations or when the response kernel is broad.
    </p>
    <p>In my applications, the RL framework is combined with:</p>
    <ul class="clean-list">
      <li>large response-matrix construction;</li>
      <li>Monte Carlo integration of physical kernels;</li>
      <li>iterative convergence tests;</li>
      <li>pseudo-data sampling for uncertainty propagation;</li>
      <li>physics constraints such as positivity and smoothness;</li>
      <li>comparison with theoretical models after unfolding.</li>
    </ul>
  </section>

  <section class="detail-section">
    <h2>Application I: Femtoscopic Source Imaging</h2>
    <p>
      In heavy-ion collisions, particles are emitted from a small and rapidly evolving freeze-out source. The
      spatial distribution of emission points contains information about the space-time evolution of the collision
      system. However, this source function is not directly measured. Experiments measure the two-particle
      correlation function <span class="inline-math">\(C(q)\)</span>, which depends on the relative momentum
      <span class="inline-math">\(q\)</span> of the detected particle pair.
    </p>
    <p>
      The correlation function and the source function are connected by the Koonin-Pratt equation:
    </p>
    <div class="detail-equation">\[
      C(q)=\int d^3r\,|\Psi_q(r)|^2S(r),
    \]</div>
    <p>
      where <span class="inline-math">\(S(r)\)</span> is the source function and
      <span class="inline-math">\(\Psi_q(r)\)</span> is the two-particle wave function including final-state
      interactions. This equation has the same mathematical structure as an image-blurring problem: the source is
      the hidden image, while the wave-function kernel acts as the blurring response.
    </p>
    <p>
      Traditional HBT analyses often assume a Gaussian source and fit a few radius parameters. My approach avoids
      imposing a predefined Gaussian shape. Instead, I use the RL algorithm to reconstruct the source function
      directly from the measured correlation function.
    </p>
  </section>

  <section class="detail-section">
    <h2>Proton and Antiproton Source Imaging</h2>
    <p>
      In my CPL work, I combined the RL deblurring algorithm with the Lednicky-Lyuboshitz final-state-interaction
      model to reconstruct the freeze-out source functions of protons and antiprotons from
      <span class="inline-math">\(pp\)</span> and <span class="inline-math">\(\bar{p}\bar{p}\)</span> correlation
      functions in Au+Au collisions at
    </p>
    <div class="detail-equation">\[
      \sqrt{s_{NN}}=200~\mathrm{GeV}.
    \]</div>
    <p>
      This method reconstructs the source distribution while simultaneously constraining the strong-interaction
      parameters between particle pairs. In the analysis, the effective range was fixed at
    </p>
    <div class="detail-equation">\[
      d_0=2.8~\mathrm{fm},
    \]</div>
    <p>and the extracted scattering lengths were</p>
    <div class="detail-equation">\[
      f_0(pp)=(7.7\pm0.2)~\mathrm{fm}, \qquad
      f_0(\bar{p}\bar{p})=(7.9\pm0.3)~\mathrm{fm}.
    \]</div>
    <p>
      The reconstructed correlation functions agree with the experimental data, and the reconstructed source
      functions show that protons and antiprotons share the same freeze-out spatial distribution within
      uncertainties.
    </p>
    <p>
      The key result is not only that the proton and antiproton sources are consistent, but also that the
      reconstructed source functions are non-Gaussian. Compared with the conventional Gaussian source assumption,
      the RL-imaged source is more concentrated at small radii, especially for
      <span class="inline-math">\(r \lt 5~\mathrm{fm}\)</span>, and has reduced density at larger radii. From the
      algorithmic perspective, this work demonstrates that RL can turn a one-dimensional correlation observable
      into a model-independent source image.
    </p>
  </section>

  <section class="detail-section">
    <h2>Extension: Three-Dimensional Source Imaging</h2>
    <p>
      A later extension generalized the RL imaging method from one-dimensional source reconstruction to
      three-dimensional source imaging. In that study, the RL algorithm was applied to reconstruct the
      three-dimensional source function of identical pions from
      <span class="inline-math">\(\pi^-\pi^-\)</span> correlation functions. The method was validated using
      simulated Gaussian sources and then applied to experimental HADES Au+Au data at 1.23A GeV.
    </p>
    <p>
      The three-dimensional framework reconstructs the source in the out-side-long coordinate system, allowing
      the correlation function <span class="inline-math">\(C(q_o,q_s,q_l)\)</span> to be related to the spatial
      distribution <span class="inline-math">\(S(r_o,r_s,r_l)\)</span>. This represents a significantly larger
      inverse problem than the one-dimensional case, requiring multidimensional response kernels, larger matrix
      operations, and more careful convergence control.
    </p>
    <p>
      The same framework was further used with UrQMD simulations of Pb+Pb collisions at 1.5A GeV to study
      sensitivity to neutron skin thickness. This extension was built on the original RL imaging strategy. My
      role was to provide methodological guidance based on the earlier source-imaging framework.
    </p>
  </section>

  <section class="detail-section">
    <h2>Application II: Gamma-Ray Spectrum Reconstruction</h2>
    <p>
      A second major application of my RL work is the reconstruction of original bremsstrahlung
      <span class="inline-math">\(\gamma\)</span>-ray spectra in heavy-ion collisions.
    </p>
    <p>
      In SRC studies, high-energy bremsstrahlung photons are used to probe high-momentum nucleons in nuclei.
      However, the measured <span class="inline-math">\(\gamma\)</span>-ray spectrum is not the original physical
      spectrum. High-energy <span class="inline-math">\(\gamma\)</span> rays undergo complex transport inside the
      CsI(Tl) detector array, including shower development, energy leakage, partial absorption, and finite detector
      resolution. Therefore, the detector output is a response-filtered version of the original spectrum.
    </p>
    <p>The measured spectrum can be written as</p>
    <div class="detail-equation">\[
      e_i=\sum_jD_{ij}\mathcal{E}_j,
    \]</div>
    <p>
      where <span class="inline-math">\(\mathcal{E}_j\)</span> is the original
      <span class="inline-math">\(\gamma\)</span>-ray energy spectrum and
      <span class="inline-math">\(D_{ij}\)</span> is the detector response matrix obtained from Geant4
      simulations. The RL algorithm reconstructs <span class="inline-math">\(\mathcal{E}_j\)</span> iteratively
      without directly inverting <span class="inline-math">\(D_{ij}\)</span>, avoiding numerical instability and
      preserving the positivity of the spectrum.
    </p>
    <p>This is a typical AI/ML-style scientific computing problem:</p>
    <ul class="clean-list">
      <li>construct a high-dimensional response matrix;</li>
      <li>solve an ill-posed inverse problem;</li>
      <li>avoid unstable direct inversion;</li>
      <li>impose physical constraints such as non-negativity;</li>
      <li>use iterative optimization and convergence criteria;</li>
      <li>propagate uncertainty through pseudo-data sampling.</li>
    </ul>
  </section>

  <section class="detail-section">
    <h2>Bremsstrahlung Experiments</h2>
    <p>
      The first application was the reconstruction of the bremsstrahlung
      <span class="inline-math">\(\gamma\)</span>-ray spectrum in
      <span class="inline-math">\(^{86}\mathrm{Kr}+^{124}\mathrm{Sn}\)</span> collisions at 25 MeV/u. The RL
      algorithm was introduced to solve the detector-response inverse problem and recover the original spectrum
      from the measured detector-level spectrum. The reconstructed spectrum was then compared directly with IBUU
      transport-model calculations containing different high-momentum-tail fractions.
    </p>
    <p>
      The RL reconstruction method was later applied to the high-statistics
      <span class="inline-math">\(^{124}\mathrm{Sn}+^{124}\mathrm{Sn}\)</span> experiment at 25 MeV/u. The main
      analysis extracted the SRC-induced high-momentum-tail fraction as
      <span class="inline-math">\(R_{\mathrm{HMT}}=(20\pm3)\%\)</span>. In the PRC study, the RL algorithm was
      used as an independent reconstruction method. After unfolding the detector response, the reconstructed
      original bremsstrahlung <span class="inline-math">\(\gamma\)</span>-ray spectrum was compared directly with
      IBUU-MDI calculations, giving
      <span class="inline-math">\(R_{\mathrm{HMT}}=(20.8\pm1.8)\%\)</span>, consistent with the primary
      forward-folding analysis.
    </p>
  </section>

  <section class="detail-section">
    <h2>Why This Belongs to AI &amp; Machine Learning</h2>
    <p>
      Although the Richardson-Lucy algorithm is not a neural network, it is deeply connected to modern
      machine-learning methodology. It is an iterative probabilistic inference algorithm for hidden-variable
      reconstruction. In my work, I use it in a physics-informed way: the response matrix is not learned from
      generic data, but constructed from physical simulations, detector models, or wave-function kernels.
    </p>
    <p>The core computational skills involved include:</p>
    <ul class="clean-list">
      <li>Bayesian iterative inference;</li>
      <li>response-matrix construction and manipulation;</li>
      <li>high-dimensional numerical integration;</li>
      <li>large-scale matrix computation;</li>
      <li>inverse-problem regularization;</li>
      <li>convergence and stability analysis;</li>
      <li>Monte Carlo uncertainty propagation;</li>
      <li>physics-informed reconstruction;</li>
      <li>comparison between unfolded data and theoretical models.</li>
    </ul>
    <p>
      This work demonstrates my ability to translate algorithms across domains: from optical deblurring to
      femtoscopic source imaging and <span class="inline-math">\(\gamma\)</span>-ray spectrum unfolding in nuclear
      physics.
    </p>
  </section>

  <section class="detail-section">
    <h2>My Contributions</h2>
    <ul class="clean-list">
      <li>Developed Richardson-Lucy-based reconstruction frameworks for nuclear-physics inverse problems.</li>
      <li>Applied Bayesian deblurring to reconstruct femtoscopic freeze-out source functions from two-particle correlation functions.</li>
      <li>Combined RL source imaging with physical wave-function kernels and final-state-interaction models.</li>
      <li>Implemented detector-response unfolding for high-energy bremsstrahlung <span class="inline-math">\(\gamma\)</span>-ray spectra using Geant4-based response matrices.</li>
      <li>Used iterative reconstruction, pseudo-data sampling, and uncertainty propagation to validate the stability of the results.</li>
      <li>Extended RL reconstruction from proof-of-principle applications to precision SRC studies in <span class="inline-math">\(^{124}\mathrm{Sn}+^{124}\mathrm{Sn}\)</span> collisions.</li>
    </ul>
  </section>

  <section class="detail-section">
    <h2>Related Publications</h2>
    <ol class="publication-list">
      <li>
        <span class="publication-label">Source imaging</span>
        <strong>J. Xu et al.</strong>, "Imaging Freeze-Out Sources and Extracting Strong Interaction Parameters
        in Relativistic Heavy-Ion Collisions,"
        <a href="https://doi.org/10.1088/0256-307X/42/3/031401" target="_blank" rel="noopener">
          <em>Chinese Physics Letters</em> <strong>42</strong>, 031401 (2025).
        </a>
      </li>
      <li>
        <span class="publication-label">Source imaging extension</span>
        <strong>H. Zhang, J. Xu et al.</strong>, "Probing the three-dimensional emission source and neutron skin
        via \(\pi\)-\(\pi\) correlations in heavy-ion collisions,"
        <a href="https://doi.org/10.1103/jdsn-p3v4" target="_blank" rel="noopener">
          <em>Physical Review C</em> <strong>113</strong>, 034904 (2026).
        </a>
      </li>
      <li>
        <span class="publication-label">Gamma-ray spectrum reconstruction</span>
        <strong>J. Xu et al.</strong>, "Reconstruction of bremsstrahlung \(\gamma\)-rays spectrum in heavy ion
        reactions with Richardson-Lucy algorithm,"
        <a href="https://doi.org/10.1016/j.physletb.2024.139009" target="_blank" rel="noopener">
          <em>Physics Letters B</em> <strong>857</strong>, 139009 (2024).
        </a>
      </li>
      <li>
        <span class="publication-label">Gamma-ray SRC application</span>
        <strong>J. Xu et al.</strong>, "Experimental study of bremsstrahlung \(\gamma\)-ray emission and
        short-range correlations in \(^{124}\mathrm{Sn}+^{124}\mathrm{Sn}\) collisions at 25 MeV/nucleon,"
        <a href="https://doi.org/10.1103/dhz2-nl56" target="_blank" rel="noopener">
          <em>Physical Review C</em> <strong>113</strong>, 044613 (2026).
        </a>
      </li>
    </ol>
  </section>

  <div class="detail-actions">
    <a class="home-button" href="/#ai-methods">Back to AI &amp; ML</a>
  </div>
</div>
