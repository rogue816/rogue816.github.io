---
layout: default
title: Pankaj Yadav
permalink: /
author_profile: false
---

{% include base_path %}

<style>
  /* Home-page-only styles. Site-wide colors/fonts live in assets/css/custom.css */
  .py-home { padding: 48px 1.2em 0 1.2em; }           /* clears the fixed top menu */
  .py-wrap { max-width: 1040px; margin: 0 auto; }
  .py-home section { scroll-margin-top: 100px; }

  /* ---- Hero ---- */
  .py-hero {
    display: grid;
    grid-template-columns: 260px 1fr;
    gap: 52px;
    align-items: center;
    padding: 16px 8px 48px 8px;
    border-bottom: 1px solid var(--py-rule);
  }
  .py-portrait { position: relative; width: 100%; }
  .py-portrait::before {
    content: "";
    position: absolute;
    inset: 12px -12px -12px 12px;
    border: 1px solid var(--py-gold);
    border-radius: 4px;
    opacity: 0.7;
  }
  .py-portrait img {
    position: relative;
    display: block;
    width: 100%;
    aspect-ratio: 3 / 4;
    object-fit: cover;
    object-position: center 15%;   /* lower % = show more of the top of the photo */
    border-radius: 4px;
    box-shadow: 0 18px 40px rgba(0,0,0,0.45);
  }
  .py-hero-text h1 {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-weight: 500;
    font-style: italic;
    color: var(--py-heading);
    font-size: clamp(2.8rem, 6vw, 4.4rem);
    line-height: 1.05;
    margin: 0;
    border: none;
  }
  .py-divider { width: 64px; height: 2px; background: var(--py-gold); margin: 20px 0 16px 0; }
  .py-tagline {
    font-family: 'Inter', sans-serif;
    color: var(--py-gold-soft);
    font-size: 0.85rem;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 5px;
    margin: 0 0 22px 0;
  }
  .py-intro { font-size: 1.12rem; line-height: 1.68; margin: 0 0 12px 0; }
  .py-intro em { color: var(--py-gold-soft); }
  .py-intro strong { color: var(--py-heading); font-weight: 500; }
  .py-cta { display: flex; gap: 12px; flex-wrap: wrap; margin-top: 22px; }
  .py-cta a {
    font-family: 'Inter', sans-serif;
    font-size: 0.8rem;
    font-weight: 500;
    letter-spacing: 1px;
    padding: 8px 20px;
    border: 1px solid rgba(224,204,159,0.4);
    border-radius: 999px;
    transition: all 0.2s ease;
  }
  .py-cta a.py-solid { background: var(--py-gold-soft); color: var(--py-bg); border-color: var(--py-gold-soft); }
  .py-cta a:hover { background: var(--py-gold); color: var(--py-bg); border-color: var(--py-gold); }

  /* ---- Section labels ---- */
  .py-label {
    font-family: 'Inter', sans-serif;
    font-size: 0.76rem;
    font-weight: 600;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--py-gold);
    margin: 0 0 18px 0;
    padding-bottom: 10px;
    border-bottom: 1px solid var(--py-rule);
  }
  .py-label-row { display: flex; justify-content: space-between; align-items: baseline; gap: 12px; border-bottom: 1px solid var(--py-rule); margin: 0 0 18px 0; }
  .py-label-row .py-label { border: none; margin: 0; }
  .py-label-row a { font-family: 'Inter', sans-serif; font-size: 0.78rem; letter-spacing: 1px; white-space: nowrap; }
  .py-block { padding: 52px 8px 0 8px; }

  /* ---- Latest news: featured paper cards ---- */
  .py-grid2 { display: grid; grid-template-columns: 1fr 1fr; gap: 22px; }
  .py-paper {
    display: flex;
    flex-direction: column;
    background: var(--py-bg-raised);
    border: 1px solid var(--py-rule);
    border-left: 3px solid var(--py-gold);
    border-radius: 6px;
    padding: 22px 24px;
  }
  .py-paper-top { display: flex; align-items: center; gap: 10px; flex-wrap: wrap; margin: 0 0 10px 0; }
  .py-date {
    font-family: 'Inter', sans-serif;
    font-size: 0.7rem;
    font-weight: 600;
    letter-spacing: 1px;
    text-transform: uppercase;
    color: var(--py-gold-soft);
    background: rgba(201,169,110,0.10);
    border: 1px solid rgba(201,169,110,0.30);
    border-radius: 4px;
    padding: 3px 9px;
    white-space: nowrap;
  }
  .py-venue {
    font-family: 'Inter', sans-serif;
    font-size: 0.7rem;
    font-weight: 600;
    letter-spacing: 1.2px;
    text-transform: uppercase;
    color: var(--py-text-dim);
  }
  .py-paper h4 {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 1.4rem;
    font-weight: 600;
    line-height: 1.28;
    color: var(--py-heading);
    margin: 0 0 8px 0;
  }
  .py-authors { font-size: 1rem; color: var(--py-text-dim); margin: 0 0 10px 0; }
  .py-authors strong { color: var(--py-text); font-weight: 500; }
  .py-paper p.py-sum { font-size: 1.02rem; line-height: 1.6; margin: 0 0 18px 0; }
  .py-actions { margin-top: auto; display: flex; gap: 10px; flex-wrap: wrap; }
  .py-actions a, .py-links a {
    font-family: 'Inter', sans-serif;
    font-size: 0.8rem;
    font-weight: 500;
    letter-spacing: 1px;
    padding: 7px 18px;
    border: 1px solid rgba(224,204,159,0.4);
    border-radius: 999px;
    transition: all 0.2s ease;
  }
  .py-actions a:hover, .py-links a:hover { background: var(--py-gold-soft); color: var(--py-bg); }

  /* ---- News lists ---- */
  .py-news { list-style: none; margin: 0; padding: 0; }
  .py-news li {
    display: grid;
    grid-template-columns: 92px 1fr;
    gap: 16px;
    padding: 12px 0;
    border-bottom: 1px dashed var(--py-rule);
    font-size: 1.04rem;
    line-height: 1.55;
  }
  .py-news li:last-child { border-bottom: none; }
  .py-news .py-date { text-align: center; height: fit-content; margin-top: 3px; }
  .py-news em { color: var(--py-heading); }
  .py-news-more { margin-top: 18px; }
  .py-past { margin-top: 40px; }
  .py-past .py-label { color: var(--py-text-dim); }
  .py-past .py-news li { font-size: 1rem; color: var(--py-text-dim); }
  .py-past .py-news em { color: var(--py-text); }
  .py-past .py-date { color: var(--py-text-dim); background: transparent; border-color: var(--py-rule); }

  /* ---- Research interest boxes ---- */
  .py-grid4 { display: grid; grid-template-columns: repeat(4, 1fr); gap: 18px; }
  .py-box {
    display: block;
    background: var(--py-bg-raised);
    border: 1px solid var(--py-rule);
    border-top: 2px solid var(--py-gold);
    border-radius: 6px;
    padding: 22px 20px 20px 20px;
    color: var(--py-text);
    transition: transform 0.2s ease, border-color 0.2s ease;
  }
  .py-box:hover { transform: translateY(-3px); border-color: #3a4a6a; border-top-color: var(--py-gold-soft); color: var(--py-text); }
  .py-box-num { font-family: 'Cormorant Garamond', serif; font-style: italic; font-size: 1.6rem; color: var(--py-gold); line-height: 1; }
  .py-box h4 {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 1.3rem;
    font-weight: 600;
    line-height: 1.25;
    color: var(--py-heading);
    margin: 10px 0 8px 0;
  }
  .py-box p { margin: 0; font-size: 0.98rem; line-height: 1.55; color: var(--py-text-dim); }

  /* ---- Philosophy, contact, connect, visitors ---- */
  .py-narrow { max-width: 780px; margin: 0 auto; }
  .py-shloka {
    text-align: center;
    padding: 28px 24px 24px 24px;
    background: var(--py-bg-raised);
    border: 1px solid var(--py-rule);
    border-top: 2px solid var(--py-gold);
    border-radius: 6px;
  }
  .py-shloka .py-sa {
    font-family: 'Noto Serif Devanagari', 'Tiro Devanagari Sanskrit', serif;
    font-size: 1.45rem;
    line-height: 1.9;
    color: var(--py-gold-soft);
    margin: 0;
  }
  .py-shloka .py-tr { font-style: italic; font-size: 1.12rem; color: var(--py-text); margin: 14px auto 0 auto; max-width: 600px; }
  .py-bridge { text-align: center; color: var(--py-text-dim); font-size: 1.08rem; margin: 26px auto 22px auto; max-width: 640px; }
  .py-quote {
    margin: 0;
    padding: 20px 26px;
    background: var(--py-bg-raised);
    border-left: 3px solid var(--py-gold);
    border-radius: 0 4px 4px 0;
    font-style: italic;
    font-size: 1.15rem;
  }
  .py-contact { text-align: center; margin: 40px 0 0 0; font-size: 1.12rem; color: var(--py-text-dim); }
  .py-contact strong { color: var(--py-heading); font-weight: 500; }
  .py-contact a { border-bottom: 1px solid rgba(224,204,159,0.4); }
  .py-connect {
    margin: 48px 0 0 0;
    padding: 44px 24px;
    background: var(--py-bg-raised);
    border: 1px solid var(--py-rule);
    border-radius: 6px;
    text-align: center;
  }
  .py-connect h2 { font-size: 2rem; margin: 0 0 22px 0; border: none; }
  .py-links { display: flex; flex-wrap: wrap; justify-content: center; gap: 12px; }
  .py-visitors { text-align: center; padding: 52px 8px 40px 8px; }
  .py-visitors .py-label { border: none; text-align: center; }
  .py-visitors img { max-width: 100%; height: auto; border-radius: 6px; border: 1px solid var(--py-rule); box-shadow: 0 8px 24px rgba(0,0,0,0.35); }

  /* ---- Responsive ---- */
  @media (max-width: 960px) { .py-grid4 { grid-template-columns: repeat(2, 1fr); } }
  @media (max-width: 800px) {
    .py-home { padding-top: 32px; }
    .py-hero { grid-template-columns: 1fr; gap: 36px; text-align: center; }
    .py-portrait { max-width: 230px; margin: 0 auto; }
    .py-divider { margin: 18px auto 14px auto; }
    .py-tagline { letter-spacing: 3px; font-size: 0.78rem; }
    .py-intro { font-size: 1.1rem; }
    .py-cta { justify-content: center; }
    .py-grid2 { grid-template-columns: 1fr; }
  }
  @media (max-width: 520px) {
    .py-grid4 { grid-template-columns: 1fr; }
    .py-news li { grid-template-columns: 1fr; gap: 6px; }
    .py-news .py-date { width: fit-content; }
    .py-shloka .py-sa { font-size: 1.2rem; }
  }
</style>

<div class="py-home"><div class="py-wrap">
<!-- ================= HERO ================= -->
<section class="py-hero">
<div class="py-portrait"><img src="{{ base_path }}/images/healthcare.png" alt="Pankaj Yadav"></div>
<div class="py-hero-text">
<h1>Pankaj Yadav</h1>
<div class="py-divider"></div>
<p class="py-tagline">Probabilistic AI Research</p>
<p class="py-intro">Hi! I am <strong>Pankaj Yadav</strong>, a PhD researcher working in artificial intelligence, with a strong mathematical background. My interest stems from classical probability theory and statistical inference, and from a simple question: how reliable is a model when its data is scarce, imbalanced, or extreme?</p>
<p class="py-intro">To answer it, my work explores mitigating AI data bias, statistical inference, and deep generative models. I examine their theoretical foundations, translate them into algorithms, and test them empirically. Along the way, I have built oversampling frameworks for tabular data generation that connect the foundations of statistics and machine learning, and this work extends naturally to state-of-the-art generative AI. I then carry it into downstream applications, mainly in finance, climate, and healthcare, where rare events often carry the highest cost.</p>
<p class="py-intro">Beyond research, I have served as a teaching assistant at IIT Jodhpur for undergraduate, postgraduate, and diploma courses in probability, statistics, linear algebra, financial engineering, and financial analytics. I welcome collaboration on interdisciplinary ideas, so please feel free to get in touch.</p>
<div class="py-cta">
<a class="py-solid" href="mailto:yadav.58@iitj.ac.in">Get in touch</a>
<a href="{{ base_path }}/research/">My research</a>
</div>
</div>
</section>
<!-- ================= LATEST NEWS ================= -->
<section class="py-block">
<div class="py-label-row"><h3 class="py-label">Latest News</h3><a href="{{ base_path }}/publications/">All publications →</a></div>
<div class="py-grid2">
<article class="py-paper">
<div class="py-paper-top"><span class="py-date">Nov 2026</span><span class="py-venue">IEEE Trans. Emerging Topics in Computational Intelligence</span></div>
<h4>Are Kolmogorov–Arnold Networks Suitable for Imbalanced Data Classification?</h4>
<p class="py-authors"><strong>P. Yadav</strong> and V. Vijay</p>
<p class="py-sum">Published. Evaluates Kolmogorov–Arnold Networks (KANs) under structured class imbalance against parameter-matched MLPs and XGBoost baselines.</p>
<div class="py-actions"><a href="https://doi.org/10.1109/TETCI.2026.3747841" target="_blank" rel="noopener">DOI</a><a href="{{ base_path }}/publication/2026-kans-imbalance">Details</a></div>
</article>
<article class="py-paper">
<div class="py-paper-top"><span class="py-date">2026</span><span class="py-venue">Journal of Climate Finance</span></div>
<h4>Hedging Rainfall Volatility in Indian Agriculture: A Quantile-Gamma Approach to Weather Derivatives</h4>
<p class="py-authors"><strong>P. Yadav</strong> and V. Vijay</p>
<p class="py-sum">Published. A quantile–gamma XGBoost/SARIMA framework for weather-derivative triggers across drought and flood regimes.</p>
<div class="py-actions"><a href="https://doi.org/10.1016/j.jclimf.2026.100082" target="_blank" rel="noopener">DOI</a><a href="{{ base_path }}/publication/2026-rainfall-hedging">Details</a></div>
</article>
</div>
<ul class="py-news py-news-more">
<li><span class="py-date">2026</span><span>Preprint <em>“Certified Interpolation Oversampling: Per-Instance Safety Guarantees for Imbalanced Learning”</em> released on arXiv.</span></li>
<li><span class="py-date">Feb 2025</span><span>Preprint <em>“Rebalancing the scales: A systematic mapping study of GANs in addressing data imbalance”</em> released on arXiv.</span></li>
</ul>
<!-- ================= PAST NEWS ================= -->
<div class="py-past">
<h3 class="py-label">Past News</h3>
<ul class="py-news">
<li><span class="py-date">Dec 2024</span><span><em>Solar PV power generation forecasting</em> with AI and metaheuristics, published at the International Advanced Computing Conference (IACC), Springer.</span></li>
<li><span class="py-date">Nov 2023</span><span><em>Prediction of muscle power in the elderly</em> using functional screening data, presented at IEEE MIPR 2023.</span></li>
<li><span class="py-date">2023</span><span><em>Advantages of oversampling techniques</em> for fall-risk prediction, published in Springer CCIS (vol. 1856).</span></li>
<li><span class="py-date">2023</span><span><em>Fall prediction using machine learning: a systematic review</em>, published in the American Journal of Biomedical Science &amp; Research.</span></li>
<li><span class="py-date">May 2022</span><span>Received the <em>Best Student Paper Award</em> at ICT4AWE 2022 for our work on fall-risk factors in the elderly using SMOTE.</span></li>
</ul>
</div>
</section>
<!-- ================= RESEARCH INTERESTS ================= -->
<section class="py-block">
<div class="py-label-row"><h3 class="py-label">Research Interests</h3><a href="{{ base_path }}/research/">Explore my research →</a></div>
<div class="py-grid4">
<a class="py-box" href="{{ base_path }}/research/"><div class="py-box-num">01</div><h4>Rare Regions &amp; Imbalanced Learning</h4><p>Minority classes and distribution tails, with certified oversampling and cost-aware decision thresholds.</p></a>
<a class="py-box" href="{{ base_path }}/research/"><div class="py-box-num">02</div><h4>Generative AI &amp; Interpretability</h4><p>GANs, autoencoders, diffusion models and NLP, towards explainable models and world models.</p></a>
<a class="py-box" href="{{ base_path }}/research/"><div class="py-box-num">03</div><h4>Extreme Value Theory &amp; Tail Risk</h4><p>Modelling extremes for downstream decisions in climate and finance.</p></a>
<a class="py-box" href="{{ base_path }}/research/"><div class="py-box-num">04</div><h4>Probabilistic Modeling &amp; Statistical Inference</h4><p>Quantifying uncertainty in real-world data, from healthcare to energy and markets.</p></a>
</div>
</section>
<!-- ================= PHILOSOPHY + CONTACT ================= -->
<section class="py-block py-narrow">
<h3 class="py-label">Philosophy &amp; Approach</h3>
<div class="py-shloka">
<p class="py-sa" lang="sa">स्वस्ति श्रीदेवसमन्ताय।<br>शर्मन्! श्रमेण स्वयं सर्वं साध्यम्।</p>
<p class="py-tr">O seeker of peace! Through conscious inner effort, one can realize and master the entire universe within oneself.</p>
</div>
<p class="py-bridge">I carry this into research and life alike: steady, deliberate effort is how we meet an uncertain world.</p>
<p class="py-quote">As uncertainty in the world increases—the inevitable Law of Thermodynamics—life will continue to surprise you. Keep Body, Soul, and Spirit in check, and the mortgage will be paid.</p>
<p class="py-contact"><strong>Contact:</strong> <a href="mailto:yadav.58@iitj.ac.in">yadav.58@iitj.ac.in</a></p>
</section>
<!-- ================= CONNECT ================= -->
<div class="py-connect">
<h2>Connect with Me</h2>
<div class="py-links">
<a href="https://scholar.google.co.in/citations?hl=en&user=ejZNgHgAAAAJ" target="_blank" rel="noopener">Google Scholar</a>
<a href="https://www.linkedin.com/in/pankaj-yadav-867a40200?utm_source=share_via&utm_content=profile&utm_medium=member_ios" target="_blank" rel="noopener">LinkedIn</a>
<a href="https://github.com/rogue816" target="_blank" rel="noopener">GitHub</a>
<a href="https://orcid.org/0009-0009-1437-5659?lang=en" target="_blank" rel="noopener">ORCID</a>
</div>
</div>
<!-- Live Flat Map Analytics Widget Section -->
<div class="py-visitors">
<h3 class="py-label">Global Visitor Reach</h3>
<a href="https://mapmyvisitors.com/web/1c9ds" title="Visit tracker" target="_blank" rel="noopener"><img src="https://mapmyvisitors.com/map.png?d=sKAaxWpSIhqPpJsq6envxHh9wm5d5RZV3FmR5YPehIo&cl=ffffff" alt="Visitor Map"></a>
</div>
</div></div>
