---
id: paper/mixtral-of-experts
type: paper
slug: mixtral-of-experts
schema_version: 1.0
title: Mixtral of Experts
authors: Jiang et al.
year: 2024
url: https://arxiv.org/abs/2401.04088
arxiv_id: '2401.04088'
topics:
- research-topic/llm
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 3
is_high_impact: false
summary: Made Mixture-of-Experts practical and open. 8 expert networks, 2 active per token — so a 46B total model runs at the cost of a 12B model. Unlocked the quality-of-large at the cost-of-small tradeoff.
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2401.04088
  title: Mixtral of Experts
---

## Why It Matters

First practical open-weight Mixture-of-Experts LLM, routing each token to 2 of 8 expert networks for 8x7B total parameters but only 13B active per token. Matched GPT-3.5 quality at far lower inference cost. Proved MoE is production-ready, not just a research curiosity.
