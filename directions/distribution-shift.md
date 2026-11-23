---
id: research-direction/distribution-shift
type: research-direction
slug: distribution-shift
schema_version: 2.3
title: Distribution Shift
search_query: '"distribution+shift"'
order: 25
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - distribution-shift
  keyword_names:
  - distribution shift
  first_seen: '2026-11-23'
selection:
  works_recent: 267
  works_previous: 238
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
quotes:
- Beyond capability profiling, EBench analyzes the generalization ability from 4 representative perspectives, identifying the impact of different distribution shift factors.
- In this work, we revisit the role of future representations in WAMs and show that inference-time future conditioning is critical for generalization under distribution shifts.
- 'We show that multi-turn OPD introduces a prefix trap: making histories more student-on-policy improves relevance to the student, but can query the teacher on histories where its target is unreliable. This creates a two-sided distribution shift between student occupancy and teacher reliability.'
- We progressively distill a bidirectional action-conditioned teacher into a causal student through teacher forcing and ODE distillation, and introduce LongForcing to align long student self-rollouts with an extended-horizon teacher, mitigating accumulated distribution shift and autoregressive drift.
review:
  score: 10.0
  reviewed_by:
    provider: cloudflare-llama-3-3-70b
    model: openai/@cf/meta/llama-3.3-70b-instruct-fp8-fast
  prompt_versions:
    writer: 2.0.0
    critic: 1.2.0
generated_by:
  job: research-curation
  run_id: 30
  provider: gemini-flash-lite
  model: gemini/gemini-3.5-flash-lite
  prompt_version: 2.0.0
activity:
  papers_recent: 500
  papers_previous: 502
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: true
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22distribution+shift%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2608.04404
  title: 'Faster-WAM: Efficient Inference-Time Future Conditioning for Robust World Action Models'
- url: https://arxiv.org/abs/2607.04763
  title: Multi-Turn On-Policy Distillation with Prefix Replay
- url: https://arxiv.org/abs/2607.19191
  title: 'ABot-World-0: Infinite Interactive World Rollout on a Single Desktop GPU'
- url: https://arxiv.org/abs/2606.18239
  title: 'EBench: Elemental Diagnosis of Generalist Mobile Manipulation Policies'
- url: https://arxiv.org/abs/2606.00305
  title: Bridging Reasoning Trajectories in On-Policy Distillation via Near-Future Guidance
---

## Why It Matters

One simulation benchmark for generalist mobile manipulation policies examines how different distribution shift factors affect their generalization. Another paper, on world action models for robots, reports that inference-time future conditioning is critical for generalization under distribution shifts. A third reports that multi-turn on-policy distillation introduces a two-sided distribution shift between student occupancy and teacher reliability. A fourth introduces LongForcing to mitigate accumulated distribution shift and autoregressive drift in action-conditioned video world models.
