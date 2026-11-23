---
id: feed-item/2026-11-19-zerovln-learning-to-navigate-without-supervised-fine-tuning-a81baa5d
type: feed-item
slug: 2026-11-19-zerovln-learning-to-navigate-without-supervised-fine-tuning-a81baa5d
schema_version: 2.0
title: 'ZeroVLN: Learning to Navigate without Supervised Fine-Tuning of the VLM Brain'
kind: paper
url: https://arxiv.org/abs/2611.26414
source: Hugging Face Papers
source_tool: huggingface-papers
published_at: '2026-11-19T00:00:00+00:00'
relevance: 7
quote: Trained on the same navigation episodes, ZeroVLN substantially outperforms representative SFT-based hierarchical VLN methods on standard VLN-CE (continuous environments) benchmarks, while inducing only minor changes to the brain's weights and largely preserving its general capabilities.
credit: Paper list and upvotes from Hugging Face Papers (huggingface.co/papers); each paper is on arXiv under its own licence, thank you to arXiv for use of its open access interoperability.
fields:
  arxiv_id: '2611.26414'
  authors:
  - Zixuan Huang
  - Yang Zhou
  - Guli Zhang
  - Sunzhu Li
  - Hongyan Xie
  - Zehao Chen
  - Fuzhen Zhuang
  - Kaixuan Wang
  - Xiaozhi Chen
  - Yikun Ban
  - Deqing Wang
  upvotes: 21
  comments: 1
review:
  score: 10.0
  reviewed_by:
    provider: cloudflare-llama-3-3-70b
    model: openai/@cf/meta/llama-3.3-70b-instruct-fp8-fast
  prompt_versions:
    writer: 2.2.0
    critic: 1.2.0
generated_by:
  job: news-digest
  run_id: 26
  provider: gemini-flash-lite
  model: gemini/gemini-3.5-flash-lite
  prompt_version: 2.2.0
tags:
- models
- research
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/2611.26414
  title: 'ZeroVLN: Learning to Navigate without Supervised Fine-Tuning of the VLM Brain'
---

## Summary

Researchers introduce ZeroVLN, a slow-fast navigation framework for vision-language navigation that avoids supervised fine-tuning of the vision-language model brain. It uses a semantic tool-calling interface and closed-loop reinforcement learning to jointly optimize movement decisions and execution.

## Why It Matters

It substantially outperforms representative SFT-based hierarchical VLN methods on standard VLN-CE benchmarks while inducing only minor changes to the brain's weights and largely preserving its general capabilities.
