---
id: research-direction/federated-learning
type: research-direction
slug: federated-learning
schema_version: 2.2
title: Federated Learning
search_query: '"federated+learning"'
order: 19
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - federated-learning
  keyword_names:
  - federated learning
  first_seen: '2026-11-23'
selection:
  works_recent: 260
  works_previous: 161
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
quote: While cross-user collaboration can overcome this data bottleneck, current trajectory-sharing approaches compromise user privacy and impose a uniform global library that fails to accommodate client heterogeneity.
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
  papers_recent: 374
  papers_previous: 306
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: false
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22federated+learning%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2606.03143
  title: 'FederatedSkill: Federated Learning for Agentic Skill Evolution'
- url: https://arxiv.org/abs/2606.25533
  title: 'Security and Privacy in Retrieval-Augmented Generation: Architectures, Threats, Defenses, and Future Directions for Building Trustworthy Systems'
- url: https://arxiv.org/abs/2607.21361
  title: 'FedAgentKE: Federated Semantic Knowledge Evolution for Heterogeneous Agents'
- url: https://arxiv.org/abs/2610.03073
  title: 'SecJev: Bringing Security Expertise to System One Decision Models'
- url: https://arxiv.org/abs/2608.01561
  title: 'FedWorld: Scope-Aware Federation of Agent World Models'
---

## Why It Matters

Federated learning lets separate clients or agents improve from each other's experience without sharing raw data or trajectories. Recent papers apply it to language-model agents: one shares semantic skill patches instead of trajectories, another evolves reasoning knowledge across different agent frameworks, and a third exchanges abstract transition rules, which its authors report reduces negative transfer between clients. A survey reviews security and privacy risks in retrieval-augmented generation, including federated deployments.
