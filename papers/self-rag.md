---
id: paper/self-rag
type: paper
slug: self-rag
schema_version: 1.0
title: Self-RAG
authors: Asai et al.
year: 2023
url: https://arxiv.org/abs/2305.15294
arxiv_id: '2305.15294'
topics:
- research-topic/rag
is_high_impact: false
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2305.15294
  title: Self-RAG
---

## Why It Matters

Trained the LLM to emit special retrieval tokens when it needs external knowledge and critique tokens to evaluate whether retrieved passages are relevant. Unlike naive RAG that always retrieves, Self-RAG retrieves on demand, reducing noise and hallucination. Showed that teaching models when NOT to retrieve is as important as teaching them to use retrieval.
