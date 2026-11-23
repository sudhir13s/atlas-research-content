---
id: paper/long-short-term-memory-lstm
type: paper
slug: long-short-term-memory-lstm
schema_version: 3.0
title: Long Short-Term Memory
aliases:
- LSTM
authors: Hochreiter & Schmidhuber
year: 1997
url: https://doi.org/10.1162/neco.1997.9.8.1735
topics:
- research-topic/neural-networks
must_read:
  era: Statistical Learning & Revival (1990s-2000s)
  order: 30
is_high_impact: false
citation_signals:
  cited_by_count: 133603
  venue: Neural Computation
  observed_at: '2026-11-23'
  source: https://openalex.org/W2064675550
summary: Introduces long short-term memory (LSTM), a gradient-based recurrent network method that addresses the insufficient, decaying error backflow that makes learning over long time intervals slow.
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://doi.org/10.1162/neco.1997.9.8.1735
  title: Long Short-Term Memory
- url: https://direct.mit.edu/neco/article/9/8/1735/6109/Long-Short-Term-Memory
  title: Long Short-Term Memory
- url: https://arxiv.org/abs/1409.3215
  title: Sequence to Sequence Learning with Neural Networks
---

## Why It Matters

Constant error carousels inside special units enforce constant error flow, and multiplicative gate units learn to open and close access to it.

- The authors report that LSTM can bridge time lags of more than 1000 discrete time steps.
- Against real-time recurrent learning, backpropagation through time and other methods, it had many more successful runs and learned much faster.
- In 2014, Sequence to Sequence Learning with Neural Networks used multilayered LSTMs for English-to-French translation.
