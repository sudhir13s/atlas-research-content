---
id: research-direction/mixture-of-experts-moe
type: research-direction
slug: mixture-of-experts-moe
schema_version: 2.2
title: Mixture of Experts (MoE)
search_query: '"mixture+of+experts"'
order: 1
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - mixture-of-experts
  keyword_names:
  - mixture of experts
  first_seen: '2026-11-23'
selection:
  works_recent: 293
  works_previous: 230
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  min_recent_papers: 250
  max_field_share: 0.08
  max_directions: 25
  leave_below_ratio: 0.7
  leave_after_runs: 2
  runs_below: 0
  observed_at: '2026-11-23'
activity:
  papers_recent: 506
  papers_previous: 433
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: true
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22mixture+of+experts%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
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
