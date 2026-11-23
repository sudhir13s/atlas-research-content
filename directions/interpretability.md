---
id: research-direction/interpretability
type: research-direction
slug: interpretability
schema_version: 3.0
title: Interpretability
search_query: '"interpretability"'
order: 26
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - interpretability
  keyword_names:
  - interpretability
  first_seen: '2026-11-23'
selection:
  works_recent: 317
  works_previous: 296
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  leave_after_runs: 2
  runs_below: 0
  observed_at: '2026-11-23'
quotes:
- Using a new interpretability technique, the Jacobian lens, we identify the representations a model is poised to verbalize at any point in its processing.
- By transforming image generation from a black-box paradigm into a staged process akin to authentic human creation, GenClaw offers a step toward for highly controllable and interpretable visual generation systems.
- Furthermore, these black-box mappings lack interpretability, hindering the simultaneous achievement of generality, robustness, and transparency.
- We show that MDA has improved sample efficiency compared to various baseline methods, and the learned models are good predictors but also provide interpretable abstractions of each domain.
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
  papers_recent: 3583
  papers_previous: 3614
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  is_hot: true
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3Ainterpretability+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2607.15495
  title: Verbalizable Representations Form a Global Workspace in Language Models
- url: https://arxiv.org/abs/2605.30248
  title: 'GenClaw: Code-Driven Agentic Image Generation'
- url: https://arxiv.org/abs/2607.10383
  title: 'ABot-N1: Toward a General Visual Language Navigation Foundation Model'
- url: https://arxiv.org/abs/2608.09696
  title: 'Model Discovery Agent: LLM-assisted Bayesian experiment design for data-efficient discovery of mechanistic world models'
- url: https://arxiv.org/abs/2607.22925
  title: Not All LLM Reasoning is Visible in the Chain-of-Thought
---

## Why It Matters

One paper uses a new interpretability technique, which it calls the Jacobian lens, to identify the representations a language model is poised to verbalize at any point in its processing. Another proposes a code-driven agentic image generation paradigm, which its authors describe as a step toward controllable and interpretable visual generation systems. A third presents a visual language navigation foundation model that addresses the lack of interpretability in monolithic policies by decoupling cognition from control. A fourth introduces an agent that learns mechanistic world models, which its authors report provide interpretable abstractions of each domain.
