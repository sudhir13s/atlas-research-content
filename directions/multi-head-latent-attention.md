---
id: research-direction/multi-head-latent-attention
type: research-direction
slug: multi-head-latent-attention
schema_version: 1.0
title: Multi-Head Latent Attention
search_query: multi+head+latent+attention
is_hot: true
order: 2
tags:
- research-direction
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/2405.04434
  title: 'DeepSeek-V2: A Strong, Economical, and Efficient Mixture-of-Experts Language Model'
  trust: 0.9
---

## Why It Matters

Multi-head latent attention (MLA) compresses the attention key-value (KV) cache into a latent vector to make inference cheaper.

- The DeepSeek-V2 authors report that, compared with DeepSeek 67B, the model reduces the KV cache by 93.3% and raises maximum generation throughput 5.76 times.
