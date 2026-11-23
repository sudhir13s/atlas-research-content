---
id: paper/deep-belief-networks
type: paper
slug: deep-belief-networks
schema_version: 1.0
title: A Fast Learning Algorithm for Deep Belief Nets
aliases:
- Deep Belief Networks
authors: Hinton, Osindero & Teh
year: 2006
url: https://doi.org/10.1162/neco.2006.18.7.1527
topics: []
must_read:
  era: Statistical Learning & Revival (1990s-2000s)
  order: 28
is_high_impact: false
citation_signals:
  cited_by_count: 19195
  venue: Neural Computation
  observed_at: '2026-11-23'
  source: https://openalex.org/W2136922672
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://doi.org/10.1162/neco.2006.18.7.1527
  title: A Fast Learning Algorithm for Deep Belief Nets
- url: https://www.cs.toronto.edu/~hinton/absps/fastnc.pdf
  title: A Fast Learning Algorithm for Deep Belief Nets
---

## Why It Matters

Uses “complementary priors” to remove the explaining-away effects that make inference difficult in densely connected belief nets with many hidden layers.

- From this the authors derive a fast, greedy algorithm that learns deep, directed belief networks one layer at a time.
- The greedy stage initialises a slower fine-tuning procedure, a contrastive version of the wake-sleep algorithm.
- After fine-tuning, a network with three hidden layers models handwritten digit images and their labels; the authors report better digit classification than the best discriminative learning algorithms.
