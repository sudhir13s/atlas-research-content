---
id: paper/mixtral-of-experts
type: paper
slug: mixtral-of-experts
schema_version: 1.0
title: Mixtral of Experts
authors: Jiang et al.
year: 2024
url: https://arxiv.org/abs/2401.04088
arxiv_id: '2401.04088'
topics:
- research-topic/llm
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 3
is_high_impact: false
citation_signals:
  cited_by_count: 4828
  venue: arXiv preprint
  observed_at: '2026-11-20'
  source: https://openalex.org/W4390723197
summary: 'Introduces Mixtral 8x7B, a sparse mixture-of-experts (SMoE) language model: the Mistral 7B architecture with 8 feedforward blocks (experts) per layer, of which a router selects two for each token.'
tags:
- paper
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/2401.04088
  title: Mixtral of Experts
locked:
- citation_signals.venue
---

## Why It Matters

Each token has access to 47B parameters but uses 13B active parameters during inference. The authors report:

- it outperforms or matches Llama 2 70B and GPT-3.5 on all evaluated benchmarks, and vastly outperforms Llama 2 70B on mathematics, code generation and multilingual benchmarks;
- Mixtral 8x7B - Instruct surpasses GPT-3.5 Turbo, Claude-2.1, Gemini Pro and Llama 2 70B - chat on human benchmarks.

Both models are released under the Apache 2.0 license.
