---
id: research-direction/flow-matching
type: research-direction
slug: flow-matching
schema_version: 2.2
title: Flow Matching
search_query: '"flow+matching"'
order: 22
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - flow-matching
  keyword_names:
  - flow matching
  first_seen: '2026-11-23'
selection:
  works_recent: 313
  works_previous: 194
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  min_recent_papers: 250
  max_field_share: 0.08
  max_directions: 25
  leave_below_ratio: 0.7
  leave_after_runs: 2
  runs_below: 0
  observed_at: '2026-11-23'
quote: In this paper, we introduce VT-WAM, a Visual-Tactile World Action Model that jointly learns future visual prediction, tactile deformation prediction, and action prediction within a unified flow matching framework.
review:
  score: 10.0
  reviewed_by:
    provider: cloudflare-llama-3-3-70b
    model: openai/@cf/meta/llama-3.3-70b-instruct-fp8-fast
  prompt_versions:
    writer: 1.0.0
    critic: 1.2.0
generated_by:
  job: research-curation
  run_id: 29
  provider: gemini-flash-lite
  model: gemini/gemini-3.5-flash-lite
  prompt_version: 1.0.0
activity:
  papers_recent: 673
  papers_previous: 454
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: true
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22flow+matching%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2606.19531
  title: 'ImageWAM: Do World Action Models Really Need Video Generation, or Just Image Editing?'
- url: https://arxiv.org/abs/2607.02503
  title: 'VT-WAM: Visual-Tactile World Action Model for Contact-Rich Manipulation'
- url: https://arxiv.org/abs/2605.30877
  title: Wall-OSS-0.5 Technical Report
- url: https://arxiv.org/abs/2605.28544
  title: 'DriveWAM: Video Generative Priors Enable Scalable World-Action Modeling for Autonomous Driving'
- url: https://arxiv.org/abs/2606.27377
  title: 'DanceOPD: On-Policy Generative Field Distillation'
---

## Why It Matters

Recent papers use flow matching as a training objective for robot and driving policies and for image generation models. One paper introduces a visual-tactile world action model that jointly learns future visual, tactile deformation, and action prediction under a unified flow matching objective. Another paper adopts continuous flow matching as the deployment-time action interface for an open-source vision-language-action model, while others apply it to action experts, video-action policies, or on-policy generative field distillation.
