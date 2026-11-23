---
id: paper/colbert
type: paper
slug: colbert
schema_version: 3.0
title: ColBERT
authors: Khattab & Zaharia
year: 2020
url: https://arxiv.org/abs/2004.12832
topics:
- research-topic/rag
is_high_impact: false
citation_signals:
  cited_by_count: 452
  venue: arXiv (Cornell University)
  observed_at: '2026-11-23'
  source: https://openalex.org/W3034439313
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2004.12832
  title: ColBERT
---

## Why It Matters

Introduced late interaction — encoding queries and documents independently into token-level embeddings, then computing fine-grained similarity via MaxSim at search time. Achieves cross-encoder quality with bi-encoder speed. The retrieval architecture that powers RAGatouille and is increasingly the default for production RAG systems that need both quality and speed.
