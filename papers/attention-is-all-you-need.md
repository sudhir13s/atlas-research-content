---
id: paper/attention-is-all-you-need
type: paper
slug: attention-is-all-you-need
schema_version: 3.0
title: Attention Is All You Need
authors: Vaswani et al.
year: 2017
url: https://arxiv.org/abs/1706.03762
topics:
- research-topic/transformers
must_read:
  era: Attention & Transformers (2016-2019)
  order: 20
is_high_impact: true
citation_signals:
  cited_by_count: 152463
  venue: NeurIPS 2017
  observed_at: '2026-11-23'
  source: https://openalex.org/W2626778328
summary: Introduces the Transformer, a network architecture for sequence transduction based solely on attention mechanisms, dispensing with recurrence and convolutions entirely.
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/1706.03762
  title: Attention Is All You Need
- url: https://proceedings.neurips.cc/paper_files/paper/2017/hash/3f5ee243547dee91fbd053c1c4a845aa-Abstract.html
  title: Attention is All you Need (NeurIPS 2017 proceedings)
- url: https://arxiv.org/abs/2010.11929
  title: 'An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale'
locked:
- citation_signals.venue
---

## Why It Matters

The authors report:

- higher translation quality than recurrent and convolutional models, with training that is more parallelizable and takes significantly less time;
- 28.4 BLEU (bilingual evaluation understudy score) on WMT 2014 English-to-German, over 2 BLEU above the previous best results, ensembles included;
- a single-model state of the art of 41.8 BLEU on WMT 2014 English-to-French after 3.5 days of training on eight GPUs;
- successful application to English constituency parsing.

By 2020 the Vision Transformer authors described the Transformer as the de-facto standard for natural language processing tasks.
