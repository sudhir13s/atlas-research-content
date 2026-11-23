---
id: feed-item/2026-11-19-coda-davinci-reimagining-video-generation-with-code2video-1fa2ba59
type: feed-item
slug: 2026-11-19-coda-davinci-reimagining-video-generation-with-code2video-1fa2ba59
schema_version: 2.0
title: 'Coda-DaVinci: Reimagining Video Generation with Code2Video'
kind: paper
url: https://arxiv.org/abs/2611.26595
source: Hugging Face Papers
source_tool: huggingface-papers
published_at: '2026-11-19T00:00:00+00:00'
relevance: 8
quote: Code2Video uses agent-authored 3D proxies to guide video generation, enabling explicit control over structure and dynamics.
credit: Paper list and upvotes from Hugging Face Papers (huggingface.co/papers); each paper is on arXiv under its own licence, thank you to arXiv for use of its open access interoperability.
fields:
  arxiv_id: '2611.26595'
  authors:
  - Yiyan Ji
  - Qixun Wang
  - Yang Shi
  - Zhuoran Zhang
  - Yifan Xu
  - Tengfei Liu
  - Yuqi Tang
  - Xiaohan Zhang
  - Shujie Li
  - Jiafu Tang
  - Xuanyu Zhu
  - Xinyu Liu
  - Yan He
  - Yushuo Guan
  - Zihao Wang
  - Xianghua Ying
  - Shixuan Liu
  - Haotian Wang
  - Wenjing Yang
  - Zhaoxiang Zhang
  - Yuanxing Zhang
  - Pengfei Wan
  - Jiaheng Liu
  upvotes: 32
  comments: 3
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
- research
- models
- agents
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/2611.26595
  title: 'Coda-DaVinci: Reimagining Video Generation with Code2Video'
---

## Summary

The paper studies proxy granularity, physics simulation, and prompting in Code2Video generation through controlled experiments and blinded human evaluations. Building on these findings, the authors introduce Coda-DaVinci, a task-adaptive agentic framework that selects between proxy-guided and direct generation, adapts modeling granularity, and coordinates simulation with prompting. Experiments show leading instruction following, improved physical plausibility, and higher visual realism compared to baselines.

## Why It Matters

It enables explicit control over structure and dynamics in video generation by using agent-authored 3D proxies to guide the generation process.
