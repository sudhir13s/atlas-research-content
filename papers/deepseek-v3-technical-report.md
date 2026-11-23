---
id: paper/deepseek-v3-technical-report
type: paper
slug: deepseek-v3-technical-report
schema_version: 3.0
title: DeepSeek-V3 Technical Report
aliases:
- DeepSeek-V3
authors: DeepSeek-AI
year: 2024
url: https://arxiv.org/abs/2412.19437
topics:
- research-topic/llm
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 1
is_high_impact: false
citation_signals:
  cited_by_count: 9805
  venue: arXiv preprint
  observed_at: '2026-11-23'
  source: https://openalex.org/W4405903187
summary: Describes DeepSeek-V3, a Mixture-of-Experts (MoE) language model with 671B total parameters, 37B of them activated for each token, built on Multi-head Latent Attention (MLA) and the DeepSeekMoE architecture.
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2412.19437
  title: DeepSeek-V3 Technical Report
locked:
- citation_signals.venue
---

## Why It Matters

The report adds an auxiliary-loss-free strategy for load balancing and a multi-token prediction training objective.

- Pre-training on 14.8 trillion tokens, then supervised fine-tuning and reinforcement learning.
- Full training took 2.788M H800 GPU hours, with no irrecoverable loss spikes or rollbacks.
- The authors report that it outperforms other open-source models and performs comparably to leading closed-source models; the checkpoints are public.
