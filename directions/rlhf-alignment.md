---
id: research-direction/rlhf-alignment
type: research-direction
slug: rlhf-alignment
schema_version: 2.1
title: RLHF + Alignment
search_query: '"preference+optimization"+"language+model"'
order: 7
activity:
  papers_recent: 110
  papers_previous: 115
  field_recent: 43623
  field_previous: 36684
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: false
  observed_at: '2026-11-22'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22preference+optimization%22+AND+all%3A%22language+model%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608170000+TO+202611150000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-22'
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
