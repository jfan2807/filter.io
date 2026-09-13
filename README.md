# Aquarium Media Lab

> **An interactive filter-media bio-calculator and water chemistry simulator** — build a virtual filter stack and watch nitrification capacity, 30-day water chemistry, and livestock compatibility respond in real time.

![Status](https://img.shields.io/badge/status-active-success?style=flat-square)
![PWA](https://img.shields.io/badge/PWA-offline%20capable-5A0FC8?style=flat-square&logo=pwa&logoColor=white)
![Stack](https://img.shields.io/badge/stack-single%20HTML%20file%20·%20zero%20dependencies-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Data](https://img.shields.io/badge/media%20database-12%20researched%20media-2ea44f?style=flat-square)
![Species](https://img.shields.io/badge/species%20database-65%20fish%20%26%20inverts-0aa?style=flat-square)
![License](https://img.shields.io/badge/license-all%20rights%20reserved-lightgrey?style=flat-square)

**Live app:** https://jfan2807.github.io/filter.io/ — installable as an offline PWA on iPhone, Android and desktop.

---

## Overview

Choosing aquarium filter media is usually marketing-driven guesswork. Aquarium
Media Lab replaces it with an engineering model: 12 researched media types with
real surface-area, nitrification-rate, anoxic-pore and pH/KH/GH drift data, a
6-slot filter stack whose shares always total 100% of your filter's capacity,
and a simulation that projects fish-waste processing, steady-state nitrate and
a 30-day chemistry trajectory from your actual tap water.

Everything runs client-side in one self-contained HTML file — no build step, no
external dependencies — and installs as an offline PWA on iPhone, Android and
desktop.

---

## Feature Showcase

### The Lab
![Desktop overview](./docs/assets/desktop-overview.png)
*Desktop three-column layout: tank and tap-water inputs on the left, the 6-slot filter stack builder with quick-start presets in the middle, and live results on the right — an S–F filter rating, synergy badges (deep anoxic cores, MBBR + porous denitrification combos), the waste-processing pipeline, and steady-state nitrate under your water-change schedule.*

### Filter Stack Builder & Live Visualizer
<img src="./docs/assets/mobile-stack.png" width="390" alt="Stack builder on mobile">

*The stack builder on mobile: preset stacks (Community, Blackwater, Rift Cichlid, Low-Nitrate), a filter-size slider, and per-slot share sliders that rebalance so media always totals 100%. Below, the "Inside Your Filter" visualizer animates each medium to scale — biofilm bacteria in green, heterotrophs in rose — at a speed driven by your flow rate.*

### Results & 30-Day Chemistry Projection
<img src="./docs/assets/mobile-output.png" width="390" alt="Results and chemistry chart">

*Plain-language results ("comfortably handles ~159 inches of fish… nitrate holds at ~12 ppm… cycles in about 22 days") backed by a waste-processing pipeline and a 30-day pH/KH/GH trajectory chart that accounts for weekly water changes and KH buffering.*

### Science Cards
![Science card](./docs/assets/science-card.png)
*Every medium has an evidence card: total vs bio-accessible surface area, nitrification rate at temperature, anoxic pore fraction, per-litre chemistry drift, microbial mechanics, and the literature basis for each figure.*

### Livestock Matching
<img src="./docs/assets/mobile-life.png" width="390" alt="Fish recommendations">

*65 freshwater fish and invertebrates scored against your tank volume, projected pH/GH and filter capacity — perfect/good/stretch tiers, group-size stocking maths in fish-inches, and a pH-range bar with a tick marking your projected water. Searchable and filterable by category.*

### Chemistry Advisor
<img src="./docs/assets/mobile-config.png" width="390" alt="Chemistry advisor and setup">

*Set pH/KH/GH targets and the advisor issues quantitative dosing: grams of baking soda, remineralizer amounts, RO mixing ratios, or media-share changes — with per-parameter checkmarks once the projection lands on target.*

---

## Under the Hood

1. **Literature-derived media model** — each medium carries total and
   bio-accessible specific surface area, biofilm nitrification rate with
   temperature kinetics, anoxic pore fraction for denitrification, and
   per-litre pH/KH/GH drift; synergy detection rewards stacks that combine
   MBBR nitrification with porous denitrification.
2. **Steady-state chemistry simulation** — fish waste → nitrification →
   denitrification → nitrate accumulation, damped by weekly water changes and
   KH buffering, projected over 30 days against your tap-water baseline.
3. **Quantitative advisor** — not "add some buffer" but grams, ratios and
   share percentages computed from the same model the simulation runs on.
4. **Zero-dependency engineering** — one HTML file, hand-rolled canvas charts
   and particle visualizer, scroll-spy section nav on mobile, service-worker
   offline support and installable PWA.

---

## License

This is a public showcase repository — it contains the project README and
feature screenshots only. The source code is private; access can be arranged
on request for portfolio review. All rights reserved.
