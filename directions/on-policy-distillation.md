---
id: research-direction/on-policy-distillation
type: research-direction
slug: on-policy-distillation
schema_version: 2.2
title: On-Policy Distillation
search_query: '"on-policy+distillation"'
order: 16
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - on-policy-distillation
  - on-policy-self-distillation
  keyword_names:
  - on-policy distillation
  - on-policy self-distillation
  first_seen: '2026-11-23'
selection:
  works_recent: 403
  works_previous: 127
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  min_recent_papers: 250
  max_field_share: 0.08
  max_directions: 20
  leave_below_ratio: 0.7
  leave_after_runs: 2
  runs_below: 0
  observed_at: '2026-11-23'
quote: On-policy distillation (OPD) trains a student on its own rollouts with token-level teacher supervision.
review:
  score: 10.0
  reviewed_by:
    provider: cloudflare-llama-3-3-70b
    model: openai/@cf/meta/llama-3.3-70b-instruct-fp8-fast
  prompt_versions:
    writer: 1.0.0
    critic: 1.2.0
generated_by:
  job: research-curation
  run_id: 28
  provider: gemini-flash-lite
  model: gemini/gemini-3.5-flash-lite
  prompt_version: 1.0.0
activity:
  papers_recent: 396
  papers_previous: 212
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: true
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22on-policy+distillation%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2606.30406
  title: 'MOPD: Multi-Teacher On-Policy Distillation for Capability Integration in LLM Post-Training'
- url: https://arxiv.org/abs/2606.11709
  title: 'RLCSD: Reinforcement Learning with Contrastive On-Policy Self-Distillation'
- url: https://arxiv.org/abs/2607.14777
  title: 'SEED: Self-Evolving On-Policy Distillation for Agentic Reinforcement Learning'
- url: https://arxiv.org/abs/2605.26844
  title: 'Not All Disagreement Is Learnable: Token Teachability in On-Policy Distillation'
- url: https://arxiv.org/abs/2607.05184
  title: Rethinking On-Policy Self-Distillation for Thinking Models
---

## Why It Matters

On-policy distillation trains a student model on its own rollouts with token-level teacher supervision. One recent paper introduces a multi-teacher post-training paradigm for capability integration, while another proposes a contrastive method to mitigate style drift in self-distillation.
