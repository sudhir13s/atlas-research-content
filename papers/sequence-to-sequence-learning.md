---
id: paper/sequence-to-sequence-learning
type: paper
slug: sequence-to-sequence-learning
schema_version: 1.0
title: Sequence to Sequence Learning with Neural Networks
authors: Sutskever, Vinyals & Le
year: 2014
url: https://arxiv.org/abs/1409.3215
arxiv_id: '1409.3215'
topics:
- research-topic/neural-networks
must_read:
  era: Deep Learning Revolution (2012-2015)
  order: 24
is_high_impact: false
citation_signals:
  cited_by_count: 21813
  venue: NeurIPS 2014
  observed_at: '2026-11-20'
  source: https://openalex.org/W2130942839
summary: 'Presents a general end-to-end approach to sequence learning: a multilayered long short-term memory (LSTM) network maps the input sequence to a fixed-dimensional vector, and another deep LSTM decodes the target sequence from it.'
tags:
- paper
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/1409.3215
  title: Sequence to Sequence Learning with Neural Networks
- url: https://proceedings.neurips.cc/paper_files/paper/2014/hash/5a18e133cbf9f257297f410bb7eca942-Abstract.html
  title: Sequence to Sequence Learning with Neural Networks
locked:
- citation_signals.venue
---

## Why It Matters

On WMT'14 English-to-French the authors report:

- 34.8 BLEU (bilingual evaluation understudy score) on the full test set, against 33.3 for a phrase-based statistical machine translation system;
- 36.5 BLEU when the LSTM reranks that system’s 1000 hypotheses;
- no difficulty on long sentences, and markedly better results when the words of source sentences are reversed.
