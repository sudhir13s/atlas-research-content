---
id: research-direction/mixture-of-experts-moe
type: research-direction
slug: mixture-of-experts-moe
schema_version: 1.0
title: Mixture of Experts (MoE)
search_query: mixture+of+experts+language+model
is_hot: true
order: 1
tags:
- research-direction
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/1701.06538
  title: 'Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer'
  trust: 0.9
- url: https://arxiv.org/abs/2412.19437
  title: DeepSeek-V3 Technical Report
  trust: 0.9
---

## Why It Matters

Mixture-of-experts (MoE) layers use a trainable gating network to pick a sparse combination of expert sub-networks for each input, so model capacity grows without a matching rise in computation.

- The DeepSeek-V3 authors report an MoE model with 671B total parameters, 37B of them active per token, trained in 2.788M H800 GPU hours.
