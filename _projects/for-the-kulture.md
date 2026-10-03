---
layout: page
title: Algorithmic Misalignment Proving Ground
description: Empirical audit of geo-cultural flattening, unmonitored policy drift, and RecSys world models.
permalink: /projects/for-the-kulture/
importance: 1
category: work
---

## Are music streaming apps flattening geo-cultural taste and artistic expression?

### Introduction

A key metric for music streaming recommendation systems is to help users discover music and to expose artists to new fan bases[cite: 3]. This optimization works but not all the time[cite: 3]. For instance, since the introduction of streaming music services in South Africa this assumption does not hold[cite: 3]. Local fans find it harder to discover local subgenres that actually reflect their true taste[cite: 3]. Instead these platforms constantly recommend generic and out-of-context songs and artists[cite: 3]. This forces fans to flatten their true taste and this consequently forces local independent artists to flatten their true artist expression to conform to the algorithm[cite: 3].

### What is the core observation and why does it matter?

We ran a survey ($$N = 152$$) to ask fans about their experience with discovering their true local music taste on these platforms[cite: 3]. Although the sample lacked statistical power, we observed that users hold multiple platforms to overcome this local music discovery issue[cite: 3]. A noticeable sequence emerged, revealing fans discover local music authentic to their taste by way of peer-to-peer recommendations and social media[cite: 3]. These multi-million recommendation systems fail to engage users at a geo-cultural and subgenre level, instead they recycle popular and out-of-context music[cite: 3].

### From empirical research to RecSys World Models

Our methodology evolved across distinct research phases[cite: 3]:

#### 1. Empirical Counter-Alignment

Our empirical audit for-the-kulture formalises the concept of "The Inversion Problem," where platform delivery constraints $$C$$ bias observed consumer behaviour $$B$$, such that[cite: 3]:

$$P(B \mid M, C) \ne P(B \mid M)$$

where $$M$$ represents true underlying musical preferences[cite: 3].

We evaluated two counter-alignment paradigms to mitigate bias[cite: 3]:
- **Paradigm A (SCRUF-D Committee):** A 3-agent social choice committee balancing engagement and representation[cite: 3].
- **Paradigm B (Spherical Representation Alignment):** A JAX/Flax Two-Tower neural network mapping embeddings onto the unit hypersphere to prevent popularity-driven magnitude expansion[cite: 3].

#### 2. Industrial Production Integration

To ensure these interventions survive production constraints we integrate it to an open-source tidal-algorithmic-mixes production pipeline[cite: 3, 4]. This architecture combines SASRec sequence transformers with PySpark filtering and clustering pipelines to manage candidate selection and post-processing at scale[cite: 4].

#### 3. Closed-Loop Simulation Benchmarks

Instead of testing the above in a static offline environment, **kulture-rwm** constructs a predictive environmental world model to simulate long running listener feedback loops[cite: 4]. The idea is for researchers to test whether these scoring functions, representation bounds, and post-processing filters successfully prevent "The Inversion Problem" and popularity bias over extended time horizons[cite: 4]. This provides an actionable socio-technical framework to preserve geo-cultural taste and ensure equitable discovery for independent artists across the African continent and globally[cite: 4].

### Recommendations & Future Directions

Building on the combined architecture we recommend the following research to advance research on geo-cultural taste preservation[cite: 4]:

1. **Closed-Loop Synthetic Environment Simulation:** To simulate listener feedback loops over multi-days horizons with synthetic listener trajectories[cite: 4].
2. **Systematic Pipeline Ablation Experiments:** Researchers should conduct end to end ablation studies across the representation stage, sequence prediction stage and post-processing committee stage[cite: 4].
3. **Adopting Socio-Technical Evaluation Metrics:** Evaluation should be beyond top-k ranking metrics and adopt multi-dimensional metrics like local discovery shift percentages and artist-level distribution equity[cite: 4].
4. **Cross-Regional Generalisation Beyond South Africa:** The pilot focused on South Africa's local subgenres (Barcadi, Motswako and Gqom)[cite: 4]. It is important that the **kulture-rwm** framework is applied in other regions across Africa (YuroPop and Gengetone) and globally to test if hyperspherical alignment holds across diverse cultural contexts[cite: 4].

### Appendix: Open Sourced Code

To help the development and research communities test and extend these architectures, the core components are open-sourced across our repositories[cite: 4]:

- **for-the-kulture:** [github.com/baddest-cmd/for-the-kulture](https://github.com/baddest-cmd/for-the-kulture) — Official implementation of SCRUF-D committees, JAX/Flax hyperspherical neural networks, and empirical datasets ($$N = 152$$)[cite: 4].
- **kulture-rwm:** [github.com/baddest-cmd/kulture-rwm](https://github.com/baddest-cmd/kulture-rwm) — Workspace for training RecSys World Models and running simulation benchmarks[cite: 4].
- **tidal-algorithmic-mixes:** [github.com/tidal-music/tidal-algorithmic-mixes](https://github.com/tidal-music/tidal-algorithmic-mixes) — PySpark production pipelines for SASRec sequence transformation and post-processing curation[cite: 4].
