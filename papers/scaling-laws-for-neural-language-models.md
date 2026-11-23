---
id: paper/scaling-laws-for-neural-language-models
type: paper
slug: scaling-laws-for-neural-language-models
schema_version: 3.0
title: Scaling Laws for Neural Language Models
aliases:
- Scaling Laws
authors: Kaplan et al.
year: 2020
url: https://arxiv.org/abs/2001.08361
topics:
- research-topic/llm
must_read:
  era: Scaling & Foundation Models (2020-2022)
  order: 16
is_high_impact: true
citation_signals:
  cited_by_count: 12576
  venue: arXiv preprint
  observed_at: '2026-11-23'
  source: https://openalex.org/W3001279689
summary: Studies empirical scaling laws for language model performance on the cross-entropy loss.
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2001.08361
  title: Scaling Laws for Neural Language Models
locked:
- citation_signals.venue
---

## Why It Matters

The authors report:

- loss scales as a power law with model size, dataset size and training compute, some trends spanning more than seven orders of magnitude;
- network width or depth has minimal effects within a wide range;
- simple equations for overfitting and training speed allow the optimal allocation of a fixed compute budget to be determined;
- larger models are more sample-efficient, so compute-optimal training uses very large models on relatively modest data and stops well before convergence.
