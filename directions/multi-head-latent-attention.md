---
id: research-direction/multi-head-latent-attention
type: research-direction
slug: multi-head-latent-attention
schema_version: 2.2
title: Multi-Head Latent Attention
search_query: '"multi-head+latent+attention"'
order: 2
status: retired
origin:
  source: OpenAlex keyword
  keyword_ids:
  - multi-head-latent-attention
  keyword_names:
  - multi-head latent attention
  first_seen: '2026-11-23'
selection:
  works_recent: 0
  works_previous: 0
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
  papers_recent: 16
  papers_previous: 11
  field_recent: 43623
  field_previous: 36684
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: false
  observed_at: '2026-11-22'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22multi-head+latent+attention%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608170000+TO+202611150000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2405.04434
  title: 'DeepSeek-V2: A Strong, Economical, and Efficient Mixture-of-Experts Language Model'
  trust: 0.9
---

## Why It Matters

Multi-head latent attention (MLA) compresses the attention key-value (KV) cache into a latent vector to make inference cheaper.

- The DeepSeek-V2 authors report that, compared with DeepSeek 67B, the model reduces the KV cache by 93.3% and raises maximum generation throughput 5.76 times.
