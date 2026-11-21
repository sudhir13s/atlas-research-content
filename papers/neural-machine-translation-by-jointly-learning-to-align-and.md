---
id: paper/neural-machine-translation-by-jointly-learning-to-align-and
type: paper
slug: neural-machine-translation-by-jointly-learning-to-align-and
schema_version: 1.0
title: Neural Machine Translation by Jointly Learning to Align and Translate
aliases:
- Attention for NMT (Bahdanau)
authors: Bahdanau, Cho & Bengio
year: 2014
url: https://arxiv.org/abs/1409.0473
arxiv_id: '1409.0473'
topics:
- research-topic/nlp-classics
must_read:
  era: Deep Learning Revolution (2012-2015)
  order: 25
is_high_impact: false
citation_signals:
  cited_by_count: 32229
  venue: ICLR 2015
  observed_at: '2026-11-20'
  source: https://openalex.org/W2133564696
summary: Extends the encoder-decoder model for neural machine translation so that it automatically (soft-)searches for the parts of a source sentence relevant to predicting each target word, instead of using one fixed-length vector.
tags:
- paper
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/1409.0473
  title: Neural Machine Translation by Jointly Learning to Align and Translate
locked:
- citation_signals.venue
---

## Why It Matters

The authors conjecture that the fixed-length vector is a bottleneck for the basic encoder-decoder architecture.

- With the new approach they report English-to-French translation performance comparable to the existing state-of-the-art phrase-based system.
- The (soft-)alignments the model finds agree well with intuition.
