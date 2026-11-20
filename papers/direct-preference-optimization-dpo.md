---
id: paper/direct-preference-optimization-dpo
type: paper
slug: direct-preference-optimization-dpo
schema_version: 1.0
title: Direct Preference Optimization (DPO)
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
  cited_by_count: 10923
  venue: neural information processing systems
  observed_at: '2026-11-20'
  source: https://openalex.org/W7133208539
summary: Simplified RLHF by eliminating the reward model entirely. Directly optimizes the language model on preference pairs. Now the dominant alignment technique for open models.
tags:
- paper
updated: '2026-11-20'
sources:
- url: https://arxiv.org/abs/2305.18290
  title: Direct Preference Optimization (DPO)
---

## Why It Matters

Eliminated the reward model from RLHF by reformulating preference optimization as a simple classification loss on preference pairs. Turns a complex RL pipeline into a single supervised fine-tuning step. Now the most widely used alignment method because it is dramatically simpler to implement, more stable to train, and produces comparable results to PPO-based RLHF.
