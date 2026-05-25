---
permalink: /
title: "Junhuai Xu"
excerpt: "About me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<div class="home-page">
  <section id="about" class="home-hero">
    <p class="home-kicker">About Me</p>
    <p class="home-lead">
      Hi, I am a Ph.D. candidate in the Department of Physics at <strong>Tsinghua University</strong>, advised by
      Prof. <a href="https://inspirehep.net/authors/1062622" target="_blank" rel="noopener"><strong>Zhigang Xiao</strong></a>.
      My research lies at the intersection of <strong>experimental nuclear and particle physics</strong>,
      <strong>detector instrumentation</strong>, and <strong>scientific computing</strong>.
    </p>
    <p class="home-lead">
      My work spans short-range correlations in nuclei, atmospheric-neutrino simulations for deep-sea neutrino
      telescopes, and correlation-function imaging in heavy-ion collisions. Across these projects, I integrate
      detector calibration, response simulation, event reconstruction, and computational analysis, while extending
      machine-learning methods to neutrino reconstruction and <strong>inverse problems in physics</strong>.
    </p>
    <div class="research-vision">
      <p class="research-vision__title">Research Vision</p>
      <p>
        My long-term goal is to develop <strong>interpretable, physics-informed AI-for-science frameworks</strong>
        for extracting hidden physical information from complex experimental data. By bridging
        <strong>inverse-problem formulations</strong>, statistical inference, and machine-learning reconstruction
        with rigorous detector physics, I aim to build data-driven discovery tools grounded in
        <strong>experimental validation</strong>.
      </p>
    </div>
    <!-- <a class="home-button" href="/assets/CV_JunhuaiXu.pdf" target="_blank" rel="noopener">Curriculum Vitae</a> -->
  </section>

  {% if site.data.news %}
  <section id="news" class="home-section home-section--compact">
    <div class="section-heading">
      <p class="section-kicker">Recent News</p>
    </div>

    <div class="news-list">
      {% for item in site.data.news limit:5 %}
        <div class="news-item">
          <time>{{ item.date }}</time>
          <p>{{ item.text | markdownify | remove: '<p>' | remove: '</p>' }}</p>
        </div>
      {% endfor %}
    </div>
  </section>
  {% endif %}

  <section id="physics-research" class="home-section home-section--physics">
    <div class="section-heading">
      <p class="section-kicker">Physics Research</p>
    </div>

    <div class="research-grid research-grid--equal">
      <a class="research-card research-card--purple" href="/research/short-range-correlations/">
        <span class="research-card__index">01</span>
        <div class="research-card__content">
          <h3>Short-Range Correlations in Nuclei</h3>
          <p>
            Atomic nuclei are not simple collections of independent nucleons. At very short distances,
            protons and neutrons can form strongly correlated pairs, generating high-momentum nucleons beyond
            the traditional mean-field picture.
          </p>
          <p>
            My research develops hard bremsstrahlung \(\gamma\) rays in low-energy heavy-ion collisions as a clean
            probe of these short-range correlations. By combining precision \(\gamma\)-ray measurements with
            transport-model calculations, I extracted the SRC-induced high-momentum fraction in
            \(^{124}\mathrm{Sn}\) to be \(R_{\mathrm{HMT}} = (20 \pm 3)\%\).
          </p>
          <span class="research-card__cta">Read More &rarr;</span>
        </div>
      </a>

      <a class="research-card research-card--teal" href="/research/atmospheric-neutrino-simulation/">
        <span class="research-card__index">02</span>
        <h3>Atmospheric Neutrino Simulation</h3>
        <span class="research-card__cta">Read More &rarr;</span>
      </a>

      <a class="research-card research-card--gold" href="/research/correlation-function-imaging/">
        <span class="research-card__index">03</span>
        <div class="research-card__content">
          <h3>Correlation Function Imaging</h3>
          <p>
            Femtoscopic imaging reconstructs freeze-out source distributions from two-particle correlation
            functions in heavy-ion collisions. In this work, I combine Hanbury Brown-Twiss interferometry with
            the Richardson-Lucy deblurring algorithm to extract real-space source information without assuming
            a Gaussian shape.
          </p>
          <p>
            Applied to proton and antiproton correlations in Au+Au collisions at
            \(\sqrt{s_{NN}} = 200~\mathrm{GeV}\), the method reveals identical non-Gaussian freeze-out sources
            for matter and antimatter.
          </p>
          <span class="research-card__cta">Read More &rarr;</span>
        </div>
      </a>
    </div>
  </section>

  <section id="ai-methods" class="home-section home-section--ai">
    <div class="section-heading">
      <p class="section-kicker">AI &amp; Computational Methods</p>
    </div>

    <div class="research-grid research-grid--equal">
      <a class="research-card research-card--purple" href="/ai/richardson-lucy-nuclear-physics/">
        <span class="research-card__index">01</span>
        <div class="research-card__content">
          <h3>Richardson-Lucy Reconstruction in Nuclear Physics</h3>
          <p>
            I apply Bayesian Richardson-Lucy deblurring to nuclear-physics inverse problems, reconstructing
            hidden source functions and original \(\gamma\)-ray spectra from experimentally blurred measurements.
          </p>
          <p>
            This work combines physics-informed reconstruction, large matrix computation, iterative inference,
            and uncertainty quantification for extracting hidden physical distributions from experimentally
            blurred observables.
          </p>
          <span class="research-card__cta">Read More &rarr;</span>
        </div>
      </a>

      <a class="research-card research-card--teal" href="/ai/gnn-neutrino-reconstruction/">
        <span class="research-card__index">02</span>
        <h3>Graph Neural Networks for Neutrino Event Reconstruction</h3>
        <span class="research-card__cta">Read More &rarr;</span>
      </a>

      <a class="research-card research-card--gold" href="/ai/bayesian-filtering-engineering/">
        <span class="research-card__index">03</span>
        <h3>Bayesian Filtering Methods for Engineering Applications</h3>
        <span class="research-card__cta">Read More &rarr;</span>
      </a>
    </div>
  </section>

  <section id="experiments" class="home-section home-section--experiments">
    <div class="section-heading">
      <p class="section-kicker">Experiments &amp; Collaborations</p>
    </div>

    <div class="experience-list">
      <div class="experience-item">
        <div class="experience-item__content">
          <h3>CSHINE Experiment</h3>
          <p>
            Heavy-ion collision experiment for high-energy \(\gamma\)-ray measurement, detector response,
            and short-range-correlation studies.
          </p>
        </div>
        <div class="experience-item__meta">
          <span>Lanzhou, China</span>
          <time>2024</time>
        </div>
      </div>

      <a class="experience-item experience-item--link" href="/experiments/slegs-beam-test-ssrf/">
        <div class="experience-item__content">
          <h3>SLEGS Beam Test at SSRF</h3>
          <p>
            High-energy \(\gamma\)-ray response calibration of CsI(Tl) crystals at SLEGS/SSRF, combining
            quasi-monochromatic photon beams, detector readout, and Geant4 simulations to validate
            CSHINE-Gamma performance.
          </p>
          <span class="research-card__cta">Read More &rarr;</span>
        </div>
        <div class="experience-item__meta">
          <span>Shanghai, China</span>
          <time>Jan. 2025</time>
        </div>
      </a>

      <div class="experience-item">
        <div class="experience-item__content">
          <h3>TRIDENT Collaboration</h3>
          <p>
            Contributed to simulation studies for the TRIDENT deep-sea neutrino telescope array, evaluating its
            potential for atmospheric-neutrino oscillation parameter measurements.
          </p>
        </div>
        <div class="experience-item__meta">
          <span>Shanghai, China</span>
          <time>2024-present</time>
        </div>
      </div>

      <div class="experience-item">
        <div class="experience-item__content">
          <h3>S&pi;RIT Experiment</h3>
          <p>
            Supported detector operation and electronics control during SAMURAI beam time at RIKEN,
            contributing to stable data taking and run coordination in the S&pi;RIT collaboration.
          </p>
        </div>
        <div class="experience-item__meta">
          <span>RIKEN, Japan</span>
          <time>2024</time>
        </div>
      </div>
    </div>
  </section>

  <section id="education" class="home-section">
    <div class="section-heading">
      <p class="section-kicker">Education</p>
    </div>

    <ul class="cv-list">
      <li class="cv-list__item">
        <span class="cv-list__text">Ph.D. Student in Physics, Tsinghua University</span>
        <time>2022 - Present</time>
      </li>
      <li class="cv-list__item">
        <span class="cv-list__text">Bachelor of Science, South China Normal University</span>
        <time>2018 - 2022</time>
      </li>
    </ul>
  </section>

  <section id="awards" class="home-section">
    <div class="section-heading">
      <p class="section-kicker">Selected Awards</p>
    </div>

    <ul class="cv-list">
      <li class="cv-list__item">
        <span class="cv-list__text">First-class Comprehensive Scholarship, Tsinghua University</span>
        <time>2025</time>
      </li>
      <li class="cv-list__item">
        <span class="cv-list__text">Second-class Comprehensive Scholarship, Tsinghua University</span>
        <time>2024</time>
      </li>
      <li class="cv-list__item">
        <span class="cv-list__text">Outstanding Teaching Assistant, Tsinghua University</span>
        <time>2024</time>
      </li>
      <li class="cv-list__item">
        <span class="cv-list__text">Third Prize, National Undergraduate Math Competition Final Round, Non-Math Major</span>
        <time>2021</time>
      </li>
      <li class="cv-list__item">
        <span class="cv-list__text">First Prize, China Undergraduate Mathematical Contest in Modeling, CUMCM</span>
        <time>2020</time>
      </li>
    </ul>
  </section>

  <div class="visitor-map" aria-label="Visitor map">
    <div id="clustr_globe_container">
      <script type="text/javascript" id="clstr_globe" src="https://clustrmaps.com/globe.js?d=0y7sxcbqs8DpRDKtY8hidLM1WXMbALHYbCdxnPx6ZkY"></script>
    </div>
  </div>
</div>
