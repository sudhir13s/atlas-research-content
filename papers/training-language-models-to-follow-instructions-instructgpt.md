---
id: paper/training-language-models-to-follow-instructions-instructgpt
type: paper
slug: training-language-models-to-follow-instructions-instructgpt
schema_version: 1.0
title: Training language models to follow instructions with human feedback
aliases:
- InstructGPT
authors: Ouyang et al.
year: 2022
url: https://arxiv.org/abs/2203.02155
arxiv_id: '2203.02155'
topics:
- research-topic/alignment
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 9
is_high_impact: false
citation_signals:
  cited_by_count: 11061
  venue: NeurIPS 2022
  observed_at: '2026-11-23'
  source: https://openalex.org/W4226278401
summary: Fine-tunes GPT-3 with human feedback, first by supervised learning on labeler demonstrations, then by reinforcement learning from human feedback (RLHF) on rankings of model outputs; the resulting models are called InstructGPT.
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2203.02155
  title: Training language models to follow instructions with human feedback
- url: https://proceedings.neurips.cc/paper_files/paper/2022/hash/b1efde53be364a73914f58805a001731-Abstract-Conference.html
  title: Training language models to follow instructions with human feedback
locked:
- citation_signals.venue
---

## Why It Matters

In human evaluations on the authors’ prompt distribution:

- outputs from the 1.3B-parameter InstructGPT model are preferred to those of the 175B GPT-3, despite 100 times fewer parameters;
- InstructGPT shows improvements in truthfulness and reductions in toxic output, with minimal regressions on public natural language processing datasets.

The authors conclude that fine-tuning with human feedback is a promising direction for aligning language models with human intent.
