---
id: feed-item/2026-11-19-hiuni-harmonizing-understanding-and-generation-in-shared-vis-d2a08847
type: feed-item
slug: 2026-11-19-hiuni-harmonizing-understanding-and-generation-in-shared-vis-d2a08847
schema_version: 2.0
title: 'HiUni: Harmonizing Understanding and Generation in Shared Visual Space'
kind: paper
url: https://arxiv.org/abs/2611.26107
source: Hugging Face Papers
source_tool: huggingface-papers
published_at: '2026-11-19T00:00:00+00:00'
relevance: 8
quote: Extensive experiments show that HiUni achieves a similar average understanding score to the pretrained VLM while attaining competitive performance on image generation and editing.
credit: Paper list and upvotes from Hugging Face Papers (huggingface.co/papers); each paper is on arXiv under its own licence, thank you to arXiv for use of its open access interoperability.
fields:
  arxiv_id: '2611.26107'
  authors:
  - Jiahao Hu
  - Jingdong Du
  - Yichen Zhang
  - Yi Song
  - Zhenyu Zhang
  - Jiaxin Niu
  - Ruihang Li
  - Xiangzhao Hao
  - Yiqian Zhang
  - Yong Huang
  - Zefeng Zhang
  - Zheyuan Gu
  - Shuohuan Wang
  upvotes: 25
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
- url: https://arxiv.org/abs/2611.26107
  title: 'HiUni: Harmonizing Understanding and Generation in Shared Visual Space'
---

## Summary

The paper presents HiUni, a unified multimodal model that extends a pretrained vision language model with extensive parameter sharing for visual understanding and generation. It reuses the same language-aligned ViT and dense Transformer backbone for both capabilities while using a Pixel Diffusion Head and a lightweight HiGate pathway to address optimization and spatial detail challenges.

## Why It Matters

Extensive experiments show that HiUni achieves a similar average understanding score to the pretrained VLM while attaining competitive performance on image generation and editing.
