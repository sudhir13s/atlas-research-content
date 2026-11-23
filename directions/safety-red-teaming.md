---
id: research-direction/safety-red-teaming
type: research-direction
slug: safety-red-teaming
schema_version: 2.2
title: Safety & Red Teaming
search_query: '"red+teaming"'
order: 13
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - red-teaming
  keyword_names:
  - red teaming
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
  runs_below: 1
  observed_at: '2026-11-23'
activity:
  papers_recent: 108
  papers_previous: 103
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: false
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22red+teaming%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2209.07858
  title: 'Red Teaming Language Models to Reduce Harms: Methods, Scaling Behaviors, and Lessons Learned'
  trust: 0.9
- url: https://arxiv.org/abs/2202.03286
  title: Red Teaming Language Models with Language Models
  trust: 0.9
---

## Why It Matters

Adversarial testing to find harmful model behaviour before deployment.

- Ganguli et al. red team models of three sizes and release a dataset of 38,961 red team attacks.
- Perez et al. generate test cases with another language model.
