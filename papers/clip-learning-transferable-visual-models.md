---
id: paper/clip-learning-transferable-visual-models
type: paper
slug: clip-learning-transferable-visual-models
schema_version: 1.0
title: Learning Transferable Visual Models From Natural Language Supervision
aliases:
- CLIP
authors: Radford et al.
year: 2021
url: https://arxiv.org/abs/2103.00020
arxiv_id: '2103.00020'
topics:
- research-topic/vision
- research-topic/multimodal
must_read:
  era: Scaling & Foundation Models (2020-2022)
  order: 13
is_high_impact: false
citation_signals:
  cited_by_count: 62551
  venue: ICML 2021
  observed_at: '2026-11-23'
  source: https://openalex.org/W3135367836
summary: 'Learns image representations from natural language: the model (CLIP) is pre-trained to predict which caption goes with which image, on 400 million (image, text) pairs collected from the internet.'
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2103.00020
  title: Learning Transferable Visual Models From Natural Language Supervision
- url: https://proceedings.mlr.press/v139/radford21a.html
  title: Learning Transferable Visual Models From Natural Language Supervision
locked:
- citation_signals.venue
---

## Why It Matters

After pre-training, text that names or describes a visual concept lets the model transfer zero-shot to downstream tasks.

- On over 30 computer vision datasets the authors report non-trivial transfer to most tasks, often competitive with a fully supervised baseline.
- Zero-shot, it matches the original ResNet-50 on ImageNet without using any of the 1.28 million training examples.
- Code and pre-trained weights were released.
