---
id: paper/wavenet-a-generative-model-for-raw-audio
type: paper
slug: wavenet-a-generative-model-for-raw-audio
schema_version: 3.0
title: 'WaveNet: A Generative Model for Raw Audio'
aliases:
- WaveNet
authors: van den Oord et al.
year: 2016
url: https://arxiv.org/abs/1609.03499
topics:
- research-topic/audio
must_read:
  era: Attention & Transformers (2016-2019)
  order: 21
is_high_impact: false
summary: Autoregressive generation applied to raw audio waveforms. Produced speech quality that was indistinguishable from human recordings for the first time. The architectural ancestor of all modern text-to-speech and audio generation models.
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/1609.03499
  title: 'WaveNet: A Generative Model for Raw Audio'
---

## Why It Matters

Generated raw audio waveforms sample by sample using dilated causal convolutions, producing speech so natural it was nearly indistinguishable from human recordings. Replaced the entire concatenative and parametric TTS pipeline with a single neural network. The foundation of Google's text-to-speech system and the starting point for all modern neural audio synthesis.
