---
id: paper/training-compute-optimal-large-language-models-chinchilla
type: paper
slug: training-compute-optimal-large-language-models-chinchilla
schema_version: 3.0
title: Training Compute-Optimal Large Language Models
aliases:
- Chinchilla Scaling Laws
- An empirical analysis of compute-optimal large language model training
authors: Hoffmann et al.
year: 2022
url: https://arxiv.org/abs/2203.15556
topics:
- research-topic/llm
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 10
is_high_impact: false
citation_signals:
  cited_by_count: 6772
  venue: NeurIPS 2022
  observed_at: '2026-11-23'
  source: https://openalex.org/W7133225605
summary: Investigates the optimal model size and number of training tokens for a transformer language model under a given compute budget, training over 400 models from 70 million to over 16 billion parameters.
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2203.15556
  title: Training Compute-Optimal Large Language Models
- url: https://proceedings.neurips.cc/paper_files/paper/2022/hash/c1e2faff6f588870935f114ebe04a3e5-Abstract-Conference.html
  title: An empirical analysis of compute-optimal large language model training (NeurIPS 2022 proceedings)
locked:
- citation_signals.venue
---

## Why It Matters

The authors find current large language models significantly undertrained: for compute-optimal training, model size and training tokens should be scaled equally.

- They test this with Chinchilla, which uses Gopher’s compute budget with 70B parameters and 4 times more data.
- Chinchilla uniformly and significantly outperforms Gopher (280B), GPT-3 (175B), Jurassic-1 (178B) and Megatron-Turing NLG (530B) on a large range of downstream tasks, with 67.5% average accuracy on the MMLU benchmark.
