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
        <div class="news-item{% if forloop.first %} news-item--latest{% endif %}">
          <div class="news-item__date">
            <time>{{ item.date }}</time>
          </div>
          <div class="news-item__body">
            {% if item.title %}
              <h3>{{ item.title }}</h3>
            {% endif %}
            {% if item.location %}
              <p class="news-item__location">{{ item.location }}</p>
            {% endif %}
            <div class="news-item__text">
              {{ item.text | markdownify }}
            </div>
          </div>
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
        <h3>Short-Range Correlations in Nuclei</h3>
        <figure class="research-card__visual research-card__visual--contain">
          <img src="/assets/images/home/physics-short-range-correlations.png" alt="Short-range correlated nucleon pair">
        </figure>
        <div class="research-card__content">
          <p>
            Hard bremsstrahlung \(\gamma\) rays as a clean probe of SRC-induced high-momentum nucleons in
            low-energy heavy-ion collisions.
          </p>
          <span class="research-card__cta">Read More &rarr;</span>
        </div>
      </a>

      <a class="research-card research-card--teal" href="/research/atmospheric-neutrino-simulation/">
        <span class="research-card__index">02</span>
        <h3>Atmospheric Neutrino Simulation</h3>
        <figure class="research-card__visual">
          <img src="/assets/images/home/physics-atmospheric-neutrino.png" alt="Atmospheric neutrino crossing an underwater detector array">
        </figure>
        <div class="research-card__content">
          <p>
            Simulation workflows for atmospheric neutrinos in compact deep-sea detector arrays, linking flux,
            interactions, detector response, and reconstruction.
          </p>
          <span class="research-card__cta">Read More &rarr;</span>
        </div>
      </a>

      <a class="research-card research-card--gold" href="/research/correlation-function-imaging/">
        <span class="research-card__index">03</span>
        <h3>Correlation Function Imaging</h3>
        <figure class="research-card__visual">
          <img src="/assets/images/home/physics-correlation-imaging.jpg" alt="Femtoscopic correlation function imaging concept">
        </figure>
        <div class="research-card__content">
          <p>
            Femtoscopic imaging reconstructs freeze-out source distributions from two-particle correlations
            without assuming a Gaussian source shape.
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
            Bayesian Richardson-Lucy deblurring for nuclear-physics inverse problems, from detector-response
            unfolding to femtoscopic source imaging.
          </p>
          <span class="research-card__cta">Read More &rarr;</span>
        </div>
      </a>

      <a class="research-card research-card--teal" href="/ai/gnn-neutrino-reconstruction/">
        <span class="research-card__index">02</span>
        <div class="research-card__content">
          <h3>Graph Neural Networks for Neutrino Event Reconstruction</h3>
          <p>
            Graph-based reconstruction of sparse detector-hit patterns for neutrino event classification,
            direction reconstruction, and energy estimation.
          </p>
          <span class="research-card__cta">Read More &rarr;</span>
        </div>
      </a>

      <a class="research-card research-card--gold" href="/ai/bayesian-filtering-engineering/">
        <span class="research-card__index">03</span>
        <div class="research-card__content">
          <h3>Bayesian Filtering Methods for Engineering Applications</h3>
          <p>
            Recursive Bayesian filtering for noisy engineering systems with evolving states, incomplete
            observations, and uncertainty-aware data fusion.
          </p>
          <span class="research-card__cta">Read More &rarr;</span>
        </div>
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

  <section id="downloads" class="home-section home-section--downloads">
    <div class="section-heading">
      <p class="section-kicker">Downloads</p>
    </div>

    <div class="download-actions">
      <a class="download-button download-button--primary" href="{{ site.author.cv | relative_url }}" target="_blank" rel="noopener">
        <i class="fas fa-file-pdf" aria-hidden="true"></i>
        <span>Curriculum Vitae</span>
      </a>

      <a class="download-button" href="{{ site.author.publication_list | relative_url }}" target="_blank" rel="noopener">
        <i class="fas fa-file-pdf" aria-hidden="true"></i>
        <span>Publication List</span>
      </a>
    </div>
  </section>

  {% comment %}
  <div class="visitor-map" aria-label="Visitor map">
    <div id="clustr_globe_container">
      <script>
        (function () {
          var container = document.getElementById("clustr_globe_container");
          var globe = document.createElement("script");
          globe.type = "text/javascript";
          globe.id = "clstr_globe";
          globe.src = "https://cdn.clustrmaps.com/globe.js?d=0y7sxcbqs8DpRDKtY8hidLM1WXMbALHYbCdxnPx6ZkY";
          globe.onerror = function () {
            globe.remove();
            var fallback = document.createElement("script");
            fallback.type = "text/javascript";
            fallback.id = "clstr_globe";
            fallback.src = "https://clustrmaps.com/globe.js?d=0y7sxcbqs8DpRDKtY8hidLM1WXMbALHYbCdxnPx6ZkY";
            container.appendChild(fallback);
          };
          container.appendChild(globe);
        })();
      </script>
    </div>
  </div>
  {% endcomment %}
</div>
