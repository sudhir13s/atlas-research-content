---
id: paper/awq
type: paper
slug: awq
schema_version: 3.0
title: AWQ
authors: Lin et al.
year: 2023
url: https://arxiv.org/abs/2306.00978
topics:
- research-topic/efficiency
is_high_impact: false
citation_signals:
  cited_by_count: 1070
  venue: arXiv (Cornell University)
  observed_at: '2026-11-23'
  source: https://openalex.org/W4379260375
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2306.00978
  title: AWQ
---

## Why It Matters

Identified that protecting just 1% of salient weight channels (those corresponding to large activations) preserves model quality during INT4 quantization. Achieves better quality than GPTQ at the same bitwidth with a simpler method. The go-to quantization technique for deploying LLMs on consumer hardware because it is fast, accurate, and widely supported by inference engines.
