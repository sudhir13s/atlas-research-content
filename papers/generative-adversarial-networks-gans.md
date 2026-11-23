---
id: paper/generative-adversarial-networks-gans
type: paper
slug: generative-adversarial-networks-gans
schema_version: 1.0
title: Generative Adversarial Networks
aliases:
- GANs
- Generative Adversarial Nets
authors: Goodfellow et al.
year: 2014
url: https://arxiv.org/abs/1406.2661
arxiv_id: '1406.2661'
topics:
- research-topic/neural-networks
- research-topic/diffusion
must_read:
  era: Deep Learning Revolution (2012-2015)
  order: 23
is_high_impact: false
citation_signals:
  cited_by_count: 12093
  venue: NeurIPS 2014
  observed_at: '2026-11-23'
  source: https://openalex.org/W4298289240
summary: 'Proposes estimating generative models through an adversarial process: a generative model G and a discriminative model D are trained together, with G trained to maximize the probability that D makes a mistake.'
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/1406.2661
  title: Generative Adversarial Networks
- url: https://proceedings.neurips.cc/paper_files/paper/2014/hash/f033ed80deb0234979a61f95710dbe25-Abstract.html
  title: Generative Adversarial Nets (NeurIPS 2014 proceedings)
locked:
- citation_signals.venue
---

## Why It Matters

The authors frame the procedure as a minimax two-player game.

- For arbitrary functions G and D a unique solution exists, in which G recovers the training data distribution and D equals 1/2 everywhere.
- When G and D are multilayer perceptrons the whole system trains with backpropagation, with no Markov chains or unrolled approximate inference networks.
