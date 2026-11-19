---
id: paper/training-compute-optimal-large-language-models-chinchilla
type: paper
slug: training-compute-optimal-large-language-models-chinchilla
schema_version: 1.0
title: Training Compute-Optimal Large Language Models (Chinchilla)
aliases:
- Chinchilla Scaling Laws
authors: Hoffmann et al.
year: 2022
url: https://arxiv.org/abs/2203.15556
arxiv_id: '2203.15556'
topics:
- research-topic/llm
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 10
is_high_impact: false
summary: Most LLMs were undertrained, not undersized. A 70B model trained on 4x more data outperformed 280B trained on less. Completely changed how the industry allocates compute.
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2203.15556
  title: Training Compute-Optimal Large Language Models (Chinchilla)
---

## Why It Matters

Proved that most large models were massively undertrained relative to their size — a compute-optimal 70B model trained on 4x more data outperformed a 280B Gopher. This single insight redirected billions of dollars in training budgets toward more data and longer training. Every model after Chinchilla trains on far more tokens per parameter.
