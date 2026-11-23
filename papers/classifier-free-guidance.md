---
id: paper/classifier-free-guidance
type: paper
slug: classifier-free-guidance
schema_version: 1.0
title: Classifier-Free Guidance
authors: Ho & Salimans
year: 2022
url: https://arxiv.org/abs/2207.12598
arxiv_id: '2207.12598'
topics:
- research-topic/diffusion
is_high_impact: false
citation_signals:
  cited_by_count: 7441
  venue: arXiv (Cornell University)
  observed_at: '2026-11-23'
  source: https://openalex.org/W4288099666
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2207.12598
  title: Classifier-Free Guidance
---

## Why It Matters

Eliminated the need for a separate classifier during guided diffusion by jointly training conditional and unconditional models and interpolating between them at inference. The guidance scale parameter gives users direct control over the quality-diversity tradeoff. Used by literally every modern diffusion model — Stable Diffusion, DALL-E 3, Midjourney, FLUX.
