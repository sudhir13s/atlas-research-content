---
id: feed-item/2026-11-18-metrics-in-the-loop-complexity-feedback-reshapes-agent-writt-e7264247
type: feed-item
slug: 2026-11-18-metrics-in-the-loop-complexity-feedback-reshapes-agent-writt-e7264247
schema_version: 1.0
title: 'Metrics-in-the-Loop: Complexity Feedback Reshapes Agent-Written Code'
kind: paper
url: https://arxiv.org/abs/2611.23817
source: arXiv
source_tool: arxiv
published_at: '2026-11-18T04:19:48+00:00'
relevance: 7
quote: 'We introduce metrics-in-the-loop, an inference-time intervention that gives agents in-flight feedback: cheap, automatically computed code metrics injected into the agent''s context during the trajectory.'
credit: Metadata from the arXiv API; thank you to arXiv for use of its open access interoperability.
fields:
  arxiv_id: '2611.23817'
  version: 1
  authors:
  - Nicolas Chapados
  - Jean-François Gagné
  - Nouha Dziri
  categories:
  - cs.AI
  primary_category: cs.AI
  pdf_url: https://arxiv.org/pdf/2611.23817v1
  doi: ''
  journal_reference: ''
  comment: Agent Evaluation Science Symposium, Fall 2026, New York City
  updated: '2026-11-18T04:19:48Z'
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
- research
- agents
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2611.23817
  title: 'Metrics-in-the-Loop: Complexity Feedback Reshapes Agent-Written Code'
---

## Summary

The paper introduces metrics-in-the-loop, an inference-time intervention that provides coding agents with in-flight feedback consisting of code metrics such as cyclomatic complexity and test coverage. This feedback allows agents to refactor code or strengthen tests before continuing their autonomous runs. Experiments show that complexity feedback reduces erosion without affecting held-out correctness.

## Why It Matters

As agents scale to codebases with millions of lines, such interventions become critical to sustaining effective development and long-term code maintainability.
