---
id: paper/lost-in-the-middle
type: paper
slug: lost-in-the-middle
schema_version: 1.0
title: Lost in the Middle
authors: Liu et al.
year: 2023
url: https://arxiv.org/abs/2307.03172
arxiv_id: '2307.03172'
topics:
- research-topic/rag
is_high_impact: false
citation_signals:
  cited_by_count: 6848
  venue: Transactions of the Association for Computational Linguistics
  observed_at: '2026-11-20'
  source: https://openalex.org/W4391876619
tags:
- paper
updated: '2026-11-20'
sources:
- url: https://arxiv.org/abs/2307.03172
  title: Lost in the Middle
---

## Why It Matters

Demonstrated that LLMs perform best when relevant information is at the beginning or end of the context window, with significant degradation for information in the middle. This U-shaped attention pattern affects every RAG system in production. A must-read for anyone building retrieval pipelines — document ordering in the prompt is not optional, it is critical.
