---
layout: page
title: Algorithmic Misalignment Proving Ground
description: Empirical audit of geo-cultural flattening, unmonitored policy drift, and RecSys world models.
permalink: /projects/for-the-kulture/
img: assets/img/cassettes.jpg
importance: 1
category: work
math: true
---

# Are music streaming apps flattening geo-cultural taste and artistic expression?

### Introduction

A key metric for music streaming recommendation systems is to help users discover music and to expose artists to new fan bases. This optimization works but not all the time. For instance, since the introduction of streaming music services in South Africa this assumption does not hold. Local fans find it harder to discover local subgenres that actually reflect their true taste. Instead these platforms constantly recommend generic and out of context songs and artists. This forces fans to flatten their true taste and this consequently forces local independent artists to flatten their true artist expression to conform to the algorithm.

### What is the core observation and why does it matter?

We ran a survey ($N = 152$) to ask fans about their experience with discovering their true local music taste on these platforms. Although the sample lacked statistical power, we observed that users hold multiple platforms to overcome this local music discovery issue. A noticeable sequence emerged, revealing fans discover local music authentic to their taste by way of peer-to-peer recommendations and social media. These multi-million recommendation systems fail to engage users at a geo-cultural and subgenre level, instead they recycle popular and out-of-context music.

### From empirical research to RecSys World Models

Our methodology evolved across distinct research phases:

#### 1. Empirical Counter-Alignment

Our empirical audit for-the-kulture formalises the concept of "The Inversion Problem," where platform delivery constraints $C$ bias observed consumer behaviour $B$, such that:

$$P(B \mid M, C) \ne P(B \mid M)$$

where $M$ represents true underlying musical preferences.

We evaluated two counter-alignment paradigms to mitigate bias:

- **Paradigm A (SCRUF-D Committee):** A 3-agent social choice committee balancing engagement and representation.
- **Paradigm B (Spherical Representation Alignment):** A JAX/Flax Two-Tower neural network mapping embeddings onto the unit hypersphere to prevent popularity-driven magnitude expansion.

#### 2. Industrial Production Integration

To ensure these interventions survive production constraints we integrate it to an open-source tidal-algorithmic-mixes production pipeline. This architecture combines SASRec sequence transformers with PySpark filtering and clustering pipelines to manage candidate selection and post-processing at scale.

#### 3. Closed-Loop Simulation Benchmarks

Instead of testing the above in a static offline environment, **kulture-rwm** constructs a predictive environmental world model to simulate long running listener feedback loops. The idea is for researchers to test whether these scoring functions, representation bounds, and post-processing filters successfully prevent "The Inversion Problem" and popularity bias over extended time horizons. This provides an actionable socio-technical framework to preserve geo-cultural taste and ensure equitable discovery for independent artists across the African continent and globally.

### Recommendations & Future Directions

Building on the combined architecture we recommend the following research to advance research on geo-cultural taste preservation:

1. **Closed-Loop Synthetic Environment Simulation:** To simulate listener feedback loops over multi-days horizons with synthetic listener trajectories.
2. **Systematic Pipeline Ablation Experiments:** Researchers should conduct end to end ablation studies across the representation stage, sequence prediction stage and post-processing committee stage.
3. **Adopting Socio-Technical Evaluation Metrics:** Evaluation should be beyond top-k ranking metrics and adopt multi dimensional metrics like local discovery shift percentages and artist level distribution level equity.
4. **Cross-Regional Generalisation Beyond South Africa:** The pilot focused on South Africa's local subgenres (Barcadi, Motswako and Gqom). It is important that the **kulture-rwm** framework is applied in other regions across Africa (YuroPop and Gengetone) and globally to test if hyperspherical alignment holds across diverse cultural contexts.

### Appendix: Open Sourced Code

To help the development and research communities test and extend these architectures, the core components are open-sourced across our repositories:

- **for-the-kulture:** [github.com/baddest-cmd/for-the-kulture](https://github.com/baddest-cmd/for-the-kulture) — Official implementation of SCRUF-D committees, JAX/Flax hyperspherical neural networks, and empirical datasets ($N = 152$).
- **kulture-rwm:** [github.com/baddest-cmd/kulture-rwm](https://github.com/baddest-cmd/kulture-rwm) — Workspace for training RecSys World Models and running simulation benchmarks.
- **tidal-algorithmic-mixes:** [github.com/tidal-music/tidal-algorithmic-mixes](https://github.com/tidal-music/tidal-algorithmic-mixes) — PySpark production pipelines for SASRec sequence transformation and post-processing curation.
