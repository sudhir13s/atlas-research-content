---
id: research-direction/group-relative-policy-optimization
type: research-direction
slug: group-relative-policy-optimization
schema_version: 3.0
title: Group Relative Policy Optimization
search_query: '"Group+Relative+Policy+Optimization"'
order: 21
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - group-relative-policy-optimization
  keyword_names:
  - Group Relative Policy Optimization
  first_seen: '2026-11-23'
selection:
  works_recent: 364
  works_previous: 274
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  leave_after_runs: 2
  runs_below: 0
  observed_at: '2026-11-23'
quotes:
- group-wise sampling in the widely-used GRPO framework does not naturally fit asynchronous agentic training.
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
  papers_recent: 223
  papers_previous: 199
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  is_hot: false
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22Group+Relative+Policy+Optimization%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2607.05391
  title: 'LLM-as-a-Verifier: A General-Purpose Verification Framework'
- url: https://arxiv.org/abs/2607.07508
  title: Single-Rollout Asynchronous Optimization for Agentic Reinforcement Learning
- url: https://arxiv.org/abs/2605.24517
  title: 'ECHO: Terminal Agents Learn World Models for Free'
- url: https://arxiv.org/abs/2606.01619
  title: 'ReSkill: Reconciling Skill Creation with Policy Optimization in Agentic RL'
- url: https://arxiv.org/abs/2605.21768
  title: 'Memory-R2: Fair Credit Assignment for Long-Horizon Memory-Augmented LLM Agents'
---

## Why It Matters

Group Relative Policy Optimization (GRPO) is a group-wise sampling and reinforcement learning framework used for training and post-training large language models and agents. Recent papers examine its applications and limitations: one explores challenges when group-wise sampling does not fit asynchronous agentic training, another studies how it uses group-wise structure to embed skill creation mechanisms, and a third discusses how different intermediate memory states can make trajectory-level comparisons in group-relative methods unfair.
