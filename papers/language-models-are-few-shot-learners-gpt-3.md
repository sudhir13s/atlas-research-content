---
id: paper/language-models-are-few-shot-learners-gpt-3
type: paper
slug: language-models-are-few-shot-learners-gpt-3
schema_version: 1.0
title: Language Models are Few-Shot Learners
aliases:
- GPT-3
authors: Brown et al.
year: 2020
url: https://arxiv.org/abs/2005.14165
arxiv_id: '2005.14165'
topics:
- research-topic/llm
must_read:
  era: Scaling & Foundation Models (2020-2022)
  order: 15
is_high_impact: true
citation_signals:
  cited_by_count: 63012
  venue: NeurIPS 2020
  observed_at: '2026-11-23'
  source: https://openalex.org/W3030163527
summary: 'Trains GPT-3, an autoregressive language model with 175 billion parameters, and tests it in the few-shot setting: tasks and demonstrations are given purely as text, with no gradient updates or fine-tuning.'
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2005.14165
  title: Language Models are Few-Shot Learners
- url: https://proceedings.neurips.cc/paper_files/paper/2020/hash/1457c0d6bfcb4967418bfb8ac142f64a-Abstract.html
  title: Language Models are Few-Shot Learners
locked:
- citation_signals.venue
---

## Why It Matters

The authors report:

- scaling up language models greatly improves task-agnostic few-shot performance, sometimes competitive with prior state-of-the-art fine-tuning;
- strong results on translation, question answering and cloze tasks, and on tasks such as unscrambling words and 3-digit arithmetic;
- datasets where few-shot learning still struggles;
- generated news articles that human evaluators had difficulty distinguishing from articles written by humans.
