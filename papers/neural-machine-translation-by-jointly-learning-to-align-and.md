---
id: paper/neural-machine-translation-by-jointly-learning-to-align-and
type: paper
slug: neural-machine-translation-by-jointly-learning-to-align-and
schema_version: 3.0
title: Neural Machine Translation by Jointly Learning to Align and Translate
aliases:
- Attention for NMT (Bahdanau)
authors: Bahdanau, Cho & Bengio
year: 2014
url: https://arxiv.org/abs/1409.0473
topics:
- research-topic/nlp-classics
must_read:
  era: Deep Learning Revolution (2012-2015)
  order: 25
is_high_impact: false
summary: Introduced the attention mechanism — the decoder looks back at different parts of the input instead of compressing everything into one vector. This single idea is the direct ancestor of transformer self-attention.
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/1409.0473
  title: Neural Machine Translation by Jointly Learning to Align and Translate
---

## Why It Matters

Introduced the attention mechanism for neural machine translation, allowing the decoder to dynamically focus on different parts of the source sentence at each generation step. Eliminated the information bottleneck of fixed-size encoder vectors. The direct precursor to the transformer — 'Attention Is All You Need' took this idea and removed everything else.
