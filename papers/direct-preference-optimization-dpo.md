---
id: paper/direct-preference-optimization-dpo
type: paper
slug: direct-preference-optimization-dpo
schema_version: 1.0
title: 'Direct Preference Optimization: Your Language Model is Secretly a Reward Model'
aliases:
- DPO
authors: Rafailov et al.
year: 2023
url: https://arxiv.org/abs/2305.18290
arxiv_id: '2305.18290'
topics:
- research-topic/alignment
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 8
is_high_impact: false
citation_signals:
  cited_by_count: 11099
  venue: NeurIPS 2023
  observed_at: '2026-11-23'
  source: https://openalex.org/W7133208539
summary: 'Introduces Direct Preference Optimization (DPO): a parameterization of the reward model in reinforcement learning from human feedback (RLHF) whose optimal policy has a closed form, so the RLHF problem is solved with a simple classification loss.'
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2305.18290
  title: 'Direct Preference Optimization: Your Language Model is Secretly a Reward Model'
- url: https://proceedings.neurips.cc/paper_files/paper/2023/hash/a85b405ed65c6477a4fe8302b5e06ce7-Abstract-Conference.html
  title: 'Direct Preference Optimization: Your Language Model is Secretly a Reward Model'
locked:
- citation_signals.venue
---

## Why It Matters

The authors describe DPO as stable, performant and computationally lightweight, with no sampling from the model during fine-tuning.

- In their experiments it aligns models with human preferences as well as or better than existing methods.
- It exceeds RLHF based on proximal policy optimization (PPO) at controlling the sentiment of generations, and matches or improves response quality in summarization and single-turn dialogue.
