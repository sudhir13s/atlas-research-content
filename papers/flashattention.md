---
id: paper/flashattention
type: paper
slug: flashattention
schema_version: 3.0
title: FlashAttention
authors: Dao et al.
year: 2022
url: https://arxiv.org/abs/2205.14135
topics:
- research-topic/transformers
- research-topic/efficiency
is_high_impact: false
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2205.14135
  title: FlashAttention
---

## Why It Matters

Rewrites attention to be IO-aware — tiling computations to minimize memory reads/writes between GPU SRAM and HBM. Achieves 2-4x speedup with zero approximation. Now integrated into PyTorch and used by virtually every LLM training run.

## Also Noted

Rewrites the attention computation to be IO-aware — tiling operations to minimize reads and writes between GPU SRAM and HBM. Achieves 2-4x wall-clock speedup with zero mathematical approximation. The most impactful systems paper in modern ML — it made long-context training economically viable and is now integrated into every major deep learning framework.
