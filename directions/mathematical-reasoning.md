---
id: research-direction/mathematical-reasoning
type: research-direction
slug: mathematical-reasoning
schema_version: 3.0
title: Mathematical Reasoning
search_query: '"mathematical+reasoning"'
order: 23
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - mathematical-reasoning
  keyword_names:
  - mathematical reasoning
  first_seen: '2026-11-23'
selection:
  works_recent: 415
  works_previous: 324
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  leave_after_runs: 2
  runs_below: 0
  observed_at: '2026-11-23'
quotes:
- Experiments on Qwen3 (1.7B/4B/8B) and Olmo-3-7B-Think across mathematical and logical reasoning show that RLCSD consistently outperforms GRPO and prior OPSD methods, with additional results on agentic tasks supporting broader applicability.
- Finally, we show that LLM-as-a-Verifier can provide dense feedback for RL, improving the sample efficiency of SAC and GRPO on robotics and mathematical reasoning benchmarks.
- Experiments show that TrOPD consistently outperforms SoTA OPD baselines, including OPD, EOPD, and REOPOLD, across mathematical reasoning, code generation, and general-domain benchmarks.
- We train on two math datasets (Geometry3K and ViRL39K) and evaluate on eight benchmarks covering both mathematical reasoning and visual understanding, across three teacher sizes (4B, 8B, and 32B) on the Qwen3-VL family.
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
  papers_recent: 368
  papers_previous: 306
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  is_hot: false
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22mathematical+reasoning%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2606.11709
  title: 'RLCSD: Reinforcement Learning with Contrastive On-Policy Self-Distillation'
- url: https://arxiv.org/abs/2607.05391
  title: 'LLM-as-a-Verifier: A General-Purpose Verification Framework'
- url: https://arxiv.org/abs/2606.01249
  title: Trust Region On-Policy Distillation
- url: https://arxiv.org/abs/2605.21924
  title: Visual-Advantage On-Policy Distillation for Vision-Language Models
- url: https://arxiv.org/abs/2606.08432
  title: Trajectory-Refined Distillation
---

## Why It Matters

In the most cited recent papers under this keyword, mathematical reasoning is a benchmark for methods that train language models: the authors of one reinforcement-learning method with self-distillation report that it outperforms earlier methods on mathematical and logical reasoning. One paper proposes a verification framework that, its authors report, improves the sample efficiency of reinforcement learning on robotics and mathematical reasoning benchmarks. Another introduces a distillation method that its authors report outperforms earlier baselines across mathematical reasoning, code generation and general-domain benchmarks. A third trains vision-language models on two math datasets with a distillation method and evaluates them on benchmarks covering mathematical reasoning and visual understanding.
