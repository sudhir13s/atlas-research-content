---
id: research-direction/diffusion-models
type: research-direction
slug: diffusion-models
schema_version: 2.3
title: Diffusion Models
search_query: '"diffusion+models"'
order: 24
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - diffusion-models
  keyword_names:
  - diffusion models
  first_seen: '2026-11-23'
selection:
  works_recent: 489
  works_previous: 419
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
quotes:
- World-action models (WAMs) jointly generate future video and robot actions through iterative diffusion
- We introduce \textbf{Flash-WAM}, a modality-aware step-distillation framework inspired by consistency distillation that selects the consistency function for each modality to match its noise regime
- we introduce OmniDreams, a foundation generative world model mid- and post-trained from the Cosmos diffusion model to autoregressively generate action-conditioned videos in real time.
- We address this issue with FlowWAM, a dual-stream diffusion framework that adopts optical flow as a unified, video-native action representation.
review:
  score: 7.5
  reviewed_by:
    provider: cloudflare-llama-3-3-70b
    model: openai/@cf/meta/llama-3.3-70b-instruct-fp8-fast
  prompt_versions:
    writer: 2.0.0
    critic: 1.2.0
generated_by:
  job: research-curation
  run_id: 30
  provider: gemini-flash-lite
  model: gemini/gemini-3.5-flash-lite
  prompt_version: 2.0.0
activity:
  papers_recent: 1064
  papers_previous: 1019
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: true
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22diffusion+models%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2606.05254
  title: 'Flash-WAM: Modality-Aware Distillation for World Action Models'
- url: https://arxiv.org/abs/2606.03159
  title: 'NVIDIA OmniDreams: Real-Time Generative World Model for Closed-Loop Autonomous Vehicle Simulation'
- url: https://arxiv.org/abs/2607.13017
  title: 'FlowWAM: Optical Flow as a Unified Action Representation for World Action Models'
- url: https://arxiv.org/abs/2606.09828
  title: Latent Spatial Memory for Video World Models
- url: https://arxiv.org/abs/2607.07675
  title: Scaling Mixture-of-Experts Video Pretraining for Embodied Intelligence
---

## Why It Matters

Diffusion models are used in world-action models to jointly generate future video and robot actions through iterative denoising. One paper introduces Flash-WAM, a modality-aware step-distillation framework that, its authors report, compresses inference to a single step in each modality. Another introduces OmniDreams, a generative world model trained from a diffusion model to autoregressively generate action-conditioned videos in real time. A third presents FlowWAM, a dual-stream diffusion framework that adopts optical flow as a unified, video-native action representation.
