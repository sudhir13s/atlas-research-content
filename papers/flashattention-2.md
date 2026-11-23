---
id: paper/flashattention-2
type: paper
slug: flashattention-2
schema_version: 1.0
title: FlashAttention-2
authors: Dao
year: 2023
url: https://arxiv.org/abs/2307.08691
arxiv_id: '2307.08691'
topics:
- research-topic/efficiency
is_high_impact: false
citation_signals:
  cited_by_count: 2426
  venue: International Conference on Learning Representations
  observed_at: '2026-11-23'
  source: https://openalex.org/W4384648639
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2307.08691
  title: FlashAttention-2
---

## Why It Matters

Optimized the FlashAttention kernel with better work partitioning across GPU thread blocks and reduced non-matmul FLOPs, achieving up to 2x speedup over the original. Reaches 50-73% of theoretical peak GPU throughput on attention. Now the default attention implementation in PyTorch, JAX, and every major training framework.
