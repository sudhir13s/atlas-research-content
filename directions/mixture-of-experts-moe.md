---
id: research-direction/mixture-of-experts-moe
type: research-direction
slug: mixture-of-experts-moe
schema_version: 2.1
title: Mixture of Experts (MoE)
search_query: '"mixture+of+experts"'
order: 1
activity:
  papers_recent: 505
  papers_previous: 438
  field_recent: 43623
  field_previous: 36684
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: true
  observed_at: '2026-11-22'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22mixture+of+experts%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608170000+TO+202611150000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-22'
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
