---
id: paper/deepseek-v3-technical-report
type: paper
slug: deepseek-v3-technical-report
schema_version: 3.0
title: DeepSeek-V3 Technical Report
aliases:
- DeepSeek-V3
authors: DeepSeek AI
year: 2024
url: https://arxiv.org/abs/2412.19437
topics:
- research-topic/llm
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 1
is_high_impact: false
summary: 671B total parameters but only 37B active per token via MoE. Introduced Multi-head Latent Attention (MLA) which compresses KV cache by 93%. Trained for $5.5M — a fraction of comparable models. MIT license. Changed the economics of frontier models.
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2412.19437
  title: DeepSeek-V3 Technical Report
---

## Why It Matters

Combined Multi-head Latent Attention (MLA) with Mixture-of-Experts at 671B parameters, achieving GPT-4-level performance at a fraction of the training cost. Released under MIT license, it proved that frontier-class models can be built outside US labs. A wake-up call for the industry on cost-efficient training.
