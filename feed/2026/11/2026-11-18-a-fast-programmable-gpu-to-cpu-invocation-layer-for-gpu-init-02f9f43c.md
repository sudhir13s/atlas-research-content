---
id: feed-item/2026-11-18-a-fast-programmable-gpu-to-cpu-invocation-layer-for-gpu-init-02f9f43c
type: feed-item
slug: 2026-11-18-a-fast-programmable-gpu-to-cpu-invocation-layer-for-gpu-init-02f9f43c
schema_version: 2.0
title: A Fast, Programmable GPU-to-CPU Invocation Layer for GPU-Initiated Communication
kind: paper
url: https://arxiv.org/abs/2611.23848
source: arXiv
source_tool: arxiv
published_at: '2026-11-18T04:52:50+00:00'
relevance: 8
quote: We present KIWI, a programmable reverse-offload framework that achieves sub-microsecond one-way device-to-host latency and hundreds of millions of operations per second.
credit: Metadata from the arXiv API; thank you to arXiv for use of its open access interoperability.
fields:
  arxiv_id: '2611.23848'
  version: 1
  authors:
  - Jiakun Yan
  - Shiksha Patel
  - David Sidler
  - Gengyu Rao
  - Brandon Potter
  - Bradford Beckmann
  categories:
  - cs.DC
  - cs.LG
  primary_category: cs.DC
  pdf_url: https://arxiv.org/pdf/2611.23848v1
  comment: 11 pages, 9 figures, 3 tables
  updated: '2026-11-18T04:52:50Z'
review:
  score: 10.0
  reviewed_by:
    provider: nvidia-gemma-4-31b
    model: nvidia_nim/google/gemma-4-31b-it
  prompt_versions:
    writer: 2.1.0
    critic: 1.1.0
generated_by:
  job: news-digest
  run_id: 4
  provider: gemini-flash-lite
  model: gemini/gemini-3.5-flash-lite
  prompt_version: 2.1.0
tags:
- hardware
- frameworks
- open-source
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2611.23848
  title: A Fast, Programmable GPU-to-CPU Invocation Layer for GPU-Initiated Communication
---

## Summary

Researchers present KIWI, a programmable reverse-offload framework that achieves sub-microsecond one-way device-to-host latency and hundreds of millions of operations per second. The KIWI-P2P library outperforms state-of-the-art GDA implementations, while KIWI-EP lowers expert-parallel communication latency by up to 2.3x on AMD GPUs and time per output token in vLLM by up to 29%. The source code is made available on GitHub.

## Why It Matters

unknown
