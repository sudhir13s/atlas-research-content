---
id: research-direction/linear-attention-state-space
type: research-direction
slug: linear-attention-state-space
schema_version: 2.2
title: Linear Attention / State-Space
search_query: '"linear+attention"'
order: 3
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - state-space-models
  - mamba
  keyword_names:
  - state-space model
  - Mamba
  first_seen: '2026-11-23'
selection:
  works_recent: 83
  works_previous: 128
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  min_recent_papers: 250
  max_field_share: 0.08
  max_directions: 25
  leave_below_ratio: 0.7
  leave_after_runs: 2
  runs_below: 1
  observed_at: '2026-11-23'
activity:
  papers_recent: 116
  papers_previous: 79
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: true
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22linear+attention%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2312.00752
  title: 'Mamba: Linear-Time Sequence Modeling with Selective State Spaces'
  trust: 0.9
---

## Why It Matters

Subquadratic sequence models, such as linear attention and structured state space models (SSMs), aim to avoid the cost of attention on long sequences.

- The Mamba authors report linear scaling in sequence length and 5 times higher inference throughput than Transformers.
