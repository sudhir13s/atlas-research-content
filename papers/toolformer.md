---
id: paper/toolformer
type: paper
slug: toolformer
schema_version: 1.0
title: 'Toolformer: Language Models Can Teach Themselves to Use Tools'
aliases:
- Toolformer
authors: Schick et al.
year: 2023
url: https://arxiv.org/abs/2302.04761
arxiv_id: '2302.04761'
topics:
- research-topic/agents
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 5
is_high_impact: false
citation_signals:
  cited_by_count: 7880
  venue: NeurIPS 2023
  observed_at: '2026-11-23'
  source: https://openalex.org/W7133214447
summary: Introduces Toolformer, a language model trained in a self-supervised way, from a handful of demonstrations per API, to decide which APIs to call, when, with what arguments, and how to use the results.
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2302.04761
  title: 'Toolformer: Language Models Can Teach Themselves to Use Tools'
- url: https://proceedings.neurips.cc/paper_files/paper/2023/hash/d842425e4bf79ba039352da0f658a906-Abstract-Conference.html
  title: 'Toolformer: Language Models Can Teach Themselves to Use Tools'
locked:
- citation_signals.venue
---

## Why It Matters

The tools include a calculator, a question-answering system, two search engines, a translation system and a calendar.

The authors report substantially improved zero-shot performance across a variety of downstream tasks, often competitive with much larger models, without sacrificing core language modeling abilities.
