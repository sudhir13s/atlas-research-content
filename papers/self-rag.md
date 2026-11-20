---
id: paper/self-rag
type: paper
slug: self-rag
schema_version: 1.0
title: Self-RAG
authors: Asai et al.
year: 2023
url: https://arxiv.org/abs/2310.11511
arxiv_id: '2310.11511'
topics:
- research-topic/rag
is_high_impact: false
citation_signals:
  cited_by_count: 2276
  venue: International Conference on Learning Representations
  observed_at: '2026-11-20'
  source: https://openalex.org/W4387800173
tags:
- paper
updated: '2026-11-20'
sources:
- url: https://arxiv.org/abs/2310.11511
  title: Self-RAG
---

## Why It Matters

Trained the LLM to emit special retrieval tokens when it needs external knowledge and critique tokens to evaluate whether retrieved passages are relevant. Unlike naive RAG that always retrieves, Self-RAG retrieves on demand, reducing noise and hallucination. Showed that teaching models when NOT to retrieve is as important as teaching them to use retrieval.
