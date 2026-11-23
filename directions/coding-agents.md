---
id: research-direction/coding-agents
type: research-direction
slug: coding-agents
schema_version: 3.0
title: Coding Agents
search_query: '"coding+agents"'
order: 17
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - ai-coding-agents
  keyword_names:
  - coding agents
  first_seen: '2026-11-23'
selection:
  works_recent: 350
  works_previous: 125
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  leave_after_runs: 2
  runs_below: 0
  observed_at: '2026-11-23'
quotes:
- Coding agents are rapidly becoming a major application of agentic LLMs, but serving them efficiently remains challenging.
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
  papers_recent: 737
  papers_previous: 433
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  is_hot: true
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22coding+agents%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2607.07946
  title: 'DeepSWE: Measuring Frontier Coding Agents on Original, Long-Horizon Engineering Tasks'
- url: https://arxiv.org/abs/2606.19980
  title: 'ENPIRE: Agentic Robot Policy Self-Improvement in the Real World'
- url: https://arxiv.org/abs/2606.30560
  title: 'TraceLab: Characterizing Coding Agent Workloads for LLM Serving'
- url: https://arxiv.org/abs/2606.29957
  title: 'SWE-Together: Evaluating Coding Agents in Interactive User Sessions'
- url: https://arxiv.org/abs/2606.07297
  title: 'SWE-Explore: Benchmarking How Coding Agents Explore Repositories'
---

## Why It Matters

Coding agents are language-model systems that assist with software engineering tasks, and recent papers introduce new benchmarks and evaluation frameworks for them. One paper presents a benchmark of tasks written from scratch, so that their solutions were not seen during pretraining, and graded by hand-written verifiers; another describes a multi-turn benchmark rebuilt from real user sessions; and a third releases a trace of coding-agent sessions to analyze real workload patterns for LLM serving.
