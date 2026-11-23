---
id: paper/alibi-train-short-test-long
type: paper
slug: alibi-train-short-test-long
schema_version: 3.0
title: 'ALiBi: Train Short, Test Long'
authors: Press et al.
year: 2021
url: https://arxiv.org/abs/2108.12409
topics:
- research-topic/transformers
is_high_impact: false
citation_signals:
  cited_by_count: 979
  venue: arXiv (Cornell University)
  observed_at: '2026-11-23'
  source: https://openalex.org/W3196318247
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2108.12409
  title: 'ALiBi: Train Short, Test Long'
---

## Why It Matters

Adds a simple linear distance penalty to attention scores instead of positional embeddings. Zero extra parameters. Naturally extrapolates to longer sequences. Used in BLOOM and MPT as an alternative to RoPE.
