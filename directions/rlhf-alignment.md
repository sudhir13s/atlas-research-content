---
id: research-direction/rlhf-alignment
type: research-direction
slug: rlhf-alignment
schema_version: 3.0
title: RLHF + Alignment
search_query: '"preference+optimization"+"language+model"'
order: 7
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - reinforcement-learning-from-human-feedback
  keyword_names:
  - reinforcement learning from human feedback
  first_seen: '2026-11-23'
selection:
  works_recent: 153
  works_previous: 112
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  leave_after_runs: 2
  runs_below: 1
  observed_at: '2026-11-23'
activity:
  papers_recent: 111
  papers_previous: 113
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  is_hot: false
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22preference+optimization%22+AND+all%3A%22language+model%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2203.02155
  title: Training language models to follow instructions with human feedback
  trust: 0.9
- url: https://arxiv.org/abs/2305.18290
  title: 'Direct Preference Optimization: Your Language Model is Secretly a Reward Model'
  trust: 0.9
---

## Why It Matters

Training language models to follow human preferences.

- InstructGPT fine-tunes GPT-3 with reinforcement learning from human feedback (RLHF) on rankings of model outputs.
- Direct preference optimization (DPO) solves the same RLHF objective with only a simple classification loss, its authors report.
