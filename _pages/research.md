---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

<p class="py-lead">My research asks how models behave where data is scarce but decisions matter most, and builds methods that measure and improve reliability there, with applications in healthcare, climate, and finance.</p>

<h2 class="py-sec">Doctoral Research</h2>
<div class="py-thesis">
<p class="py-kicker">PhD Thesis · IIT Jodhpur</p>
<h3>Rare Regions in Learning and Decision-Making: Certified Oversampling, Local Support, and Thresholds</h3>
</div>

Models are typically fitted assuming that they are trained on a proportional data distribution. Such a model allocates its accuracy to the regions where observations are dense. A performance metric then aggregates that accuracy across the sample as a whole. However, in critical domains such as healthcare and climate finance, what a decision costs does not follow this proportional distribution. It concentrates in the rare regions, which the model has least reason to learn.

<div class="py-duo">
<div><span class="py-duo-k">Label space</span><span class="py-duo-t">The minority class</span><span class="py-duo-d">of an imbalanced classification problem.</span></div>
<div><span class="py-duo-k">Value space</span><span class="py-duo-t">The extreme tail</span><span class="py-duo-d">of a continuous distribution.</span></div>
</div>

These two forms of rare region are usually treated as separate problems with separate methods, but they present the same difficulty. Across these areas, the reliability of a model in a rare region is treated as an implicit consequence of aggregate performance rather than measured in its own right. In each case the reported figure describes the non-rare region, while the decision is taken in the rare one. Motivated by these limitations, this thesis develops methods and diagnostics for learning and decision-making in rare regions, spanning statistical construction, deep architectural analysis, and applied decision-making in two downstream domains.

<div class="py-parts">
<div class="py-part">
<span class="py-part-n">01 · Generation</span>
<h4>Certified Interpolation Oversampling (CISO)</h4>
<p class="py-gap">Gap: oversampling methods assume the safety of synthetic instances rather than computing it.</p>
<p>An interpolation oversampler with a per-instance certified clearance guarantee and a provably monotone safety parameter, evaluated across 39,900 fold-level runs.</p>
<a href="{{ base_path }}/publication/2026-ciso-oversampling">Preprint →</a>
</div>
<div class="py-part">
<span class="py-part-n">02 · Diagnosis</span>
<h4>Kolmogorov–Arnold Networks under Imbalance</h4>
<p class="py-gap">Gap: architectural studies do not ask whether local functions received the observations they require.</p>
<p>A parameter-matched comparison of KANs, MLPs, and XGBoost across 10 imbalanced datasets.</p>
<a href="{{ base_path }}/publication/2026-kans-imbalance">IEEE TETCI 2026 →</a>
</div>
<div class="py-part">
<span class="py-part-n">03 · Admissibility</span>
<h4>SAvRAC: Cost-Aware Clinical Thresholds</h4>
<p class="py-gap">Gap: clinical pipelines report discrimination without asking whether an admissible decision rule exists.</p>
<p>A cost-aware threshold framework for three clinical care settings, with a dataset suitability metric.</p>
</div>
<div class="py-part">
<span class="py-part-n">04 · Transfer</span>
<h4>Rainfall Hedging in Climate Finance</h4>
<p class="py-gap">Gap: distributional forecasts report pooled coverage without stratifying by the regime in which contracts trigger.</p>
<p>A quantile–gamma XGBoost/SARIMA framework for weather-derivative triggers across drought and flood regimes.</p>
<a href="{{ base_path }}/publication/2026-rainfall-hedging">Journal of Climate Finance 2026 →</a>
</div>
</div>

<h2 class="py-sec">Ongoing &amp; Future Directions</h2>
<div class="py-dirs">
<div class="py-dir">
<i class="fa-solid fa-wand-magic-sparkles" aria-hidden="true"></i>
<h4>Generative AI for Interpretable and Explainable Learning</h4>
<p>Exploring generative adversarial networks (GANs), autoencoders, diffusion models, and natural language processing (NLP) with an emphasis on interpretability and explainability, and connecting them to world models.</p>
</div>
<div class="py-dir">
<i class="fa-solid fa-chart-area" aria-hidden="true"></i>
<h4>Extreme Value Theory and Its Applications</h4>
<p>A strong interest in extreme value theory and its downstream applications, mainly in climate and finance, where the rarest events carry the highest costs.</p>
</div>
</div>

<div class="py-research-foot">
<a href="{{ base_path }}/publications/">All publications</a>
<a href="{{ base_path }}/cv/">Curriculum Vitae</a>
<a href="mailto:yadav.58@iitj.ac.in">Collaborate with me</a>
</div>
