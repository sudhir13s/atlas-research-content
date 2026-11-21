---
id: paper/wavenet-a-generative-model-for-raw-audio
type: paper
slug: wavenet-a-generative-model-for-raw-audio
schema_version: 1.0
title: 'WaveNet: A Generative Model for Raw Audio'
aliases:
- WaveNet
authors: van den Oord et al.
year: 2016
url: https://arxiv.org/abs/1609.03499
arxiv_id: '1609.03499'
topics:
- research-topic/audio
must_read:
  era: Attention & Transformers (2016-2019)
  order: 21
is_high_impact: false
citation_signals:
  cited_by_count: 9876
  venue: arXiv preprint
  observed_at: '2026-11-20'
  source: https://openalex.org/W2519091744
summary: Introduces WaveNet, a fully probabilistic, autoregressive deep neural network that generates raw audio waveforms, conditioning each audio sample on all previous ones.
tags:
- paper
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/1609.03499
  title: 'WaveNet: A Generative Model for Raw Audio'
locked:
- citation_signals.venue
---

## Why It Matters

The authors report:

- in text-to-speech, human listeners rate it significantly more natural than the best parametric and concatenative systems, for English and Mandarin;
- one model captures many speakers and switches between them when conditioned on speaker identity;
- trained on music, it generates novel and often highly realistic fragments, and it gives promising results for phoneme recognition.
