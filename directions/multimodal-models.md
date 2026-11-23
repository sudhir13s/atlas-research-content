---
id: research-direction/multimodal-models
type: research-direction
slug: multimodal-models
schema_version: 2.2
title: Multimodal Models
search_query: multimodal+vision+language+model
order: 5
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - vision-language-models
  - multimodal-large-language-models
  keyword_names:
  - vision-language models
  - multimodal large language models
  first_seen: '2026-11-23'
selection:
  works_recent: 1657
  works_previous: 1421
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
  papers_recent: 1077
  papers_previous: 1176
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: true
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3Amultimodal+AND+all%3Avision+AND+all%3Alanguage+AND+all%3Amodel+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2204.14198
  title: 'Flamingo: a Visual Language Model for Few-Shot Learning'
  trust: 0.9
---

## Why It Matters

Models that take images or video together with text as input.

- Flamingo, for example, bridges pretrained vision-only and language-only models and handles arbitrarily interleaved images, video and text.
