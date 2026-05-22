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
      Hi, I am a Ph.D. candidate at the Department of Physics, Tsinghua University, advised by Prof.
      <a href="https://inspirehep.net/authors/1062622" target="_blank" rel="noopener">Zhigang Xiao</a>.
      My research spans short-range correlations in nuclei, atmospheric neutrino simulation, and
      correlation-function imaging. Across these topics, I focus on detector response characterization, event
      reconstruction, and extracting physical observables from complex experimental data, while extending AI and
      machine learning methods to physics and engineering problems.
    </p>
    <!-- <a class="home-button" href="/assets/CV_JunhuaiXu.pdf" target="_blank" rel="noopener">Curriculum Vitae</a> -->
  </section>

  {% comment %}
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
  {% endcomment %}

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
            I develop femtoscopic imaging methods to reconstruct freeze-out source distributions from
            two-particle correlation functions in heavy-ion collisions. By combining Hanbury Brown-Twiss
            interferometry with the Richardson-Lucy deblurring algorithm, this approach extracts real-space
            source information without assuming a Gaussian shape.
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
      <p class="section-kicker">AI &amp; Machine Learning / Scientific Computing / Inverse Problems</p>
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
            This work highlights my experience in physics-informed reconstruction, large matrix computation,
            iterative inference, and uncertainty quantification.
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

  <section id="education" class="home-section">
    <div class="section-heading">
      <p class="section-kicker">Education</p>
    </div>

    <div class="cv-list">
      <div class="cv-list__item">
        <div>
          <strong>Ph.D. Student in Physics</strong>
          <span>Tsinghua University</span>
        </div>
        <time>2022 - Present</time>
      </div>
      <div class="cv-list__item">
        <div>
          <strong>Bachelor of Science</strong>
          <span>South China Normal University</span>
        </div>
        <time>2018 - 2022</time>
      </div>
    </div>
  </section>

  <section id="awards" class="home-section">
    <div class="section-heading">
      <p class="section-kicker">Selected Awards</p>
    </div>

    <div class="cv-list">
      <div class="cv-list__item">
        <div>
          <strong>First-class Comprehensive Scholarship</strong>
          <span>Tsinghua University</span>
        </div>
        <time>2025</time>
      </div>
      <div class="cv-list__item">
        <div>
          <strong>Second-class Comprehensive Scholarship</strong>
          <span>Tsinghua University</span>
        </div>
        <time>2024</time>
      </div>
      <div class="cv-list__item">
        <div>
          <strong>Outstanding Teaching Assistant</strong>
          <span>Tsinghua University</span>
        </div>
        <time>2024</time>
      </div>
      <div class="cv-list__item">
        <div>
          <strong>Third Prize, National Undergraduate Math Competition Final Round</strong>
          <span>Non-Math Major</span>
        </div>
        <time>2021</time>
      </div>
      <div class="cv-list__item">
        <div>
          <strong>First Prize, China Undergraduate Mathematical Contest in Modeling</strong>
          <span>CUMCM</span>
        </div>
        <time>2020</time>
      </div>
    </div>
  </section>

  <div class="visitor-map" aria-label="Visitor map">
    <div id="clustr_globe_container">
      <script type="text/javascript" id="clstr_globe" src="https://clustrmaps.com/globe.js?d=0y7sxcbqs8DpRDKtY8hidLM1WXMbALHYbCdxnPx6ZkY"></script>
    </div>
  </div>
</div>
