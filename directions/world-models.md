---
id: research-direction/world-models
type: research-direction
slug: world-models
schema_version: 2.2
title: World Models
search_query: '"world+models"'
order: 18
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - world-models
  keyword_names:
  - world models
  first_seen: '2026-11-23'
selection:
  works_recent: 286
  works_previous: 163
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
quote: World models aim to simulate how complex environments evolve under actions and events
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
  run_id: 28
  provider: gemini-flash-lite
  model: gemini/gemini-3.5-flash-lite
  prompt_version: 1.0.0
activity:
  papers_recent: 906
  papers_previous: 618
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: true
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22world+models%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2605.26379
  title: When Does LeJEPA Learn a World Model?
- url: https://arxiv.org/abs/2608.08023
  title: '4D-WAM: Infusing Spatiotemporal Awareness into World Action Models through Trajectory Fields'
- url: https://arxiv.org/abs/2608.25927
  title: 'Code World Model: Coding Agent as World Brain'
- url: https://arxiv.org/abs/2605.21800
  title: 'stable-worldmodel: A Platform for Reproducible World Modeling Research and Evaluation'
- url: https://arxiv.org/abs/2606.05160
  title: 'GRAIL: Generating Humanoid Loco-Manipulation from World Models'
---

## Why It Matters

World models aim to simulate how complex environments evolve under actions and events. Recent papers introduce new methods and platforms for them: one paper introduces a framework that combines language models with video models to separate world evolution from visual realization, and another presents an open-source platform for reproducible world modeling research.
