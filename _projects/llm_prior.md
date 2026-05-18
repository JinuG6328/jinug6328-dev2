---
layout: page
title: LLM-Elicited Priors for Bayesian Experimental Design
description: Using large language models as structured prior sources for decision making under uncertainty
importance: 5
category: research
related_publications: true
---

When observations are scarce or unavailable, specifying a prior distribution
is the hardest step in Bayesian inference. This project explores using
**large language models as structured prior sources** — leveraging their
compressed domain knowledge to propose causal graphs, parameter ranges, and
plausible regimes that a standard likelihood cannot recover from data alone.

We study this question through an **epidemic control** application, where an
LLM-elicited causal DAG and scenario-conditioned parameter samples serve as
the prior for model-predictive control over non-pharmaceutical interventions.
Across conditions, retaining the full LLM sample pool as a scenario ensemble
outperforms collapsing it into a point density, with disagreement among
samples acting as a natural measure of regime uncertainty {% cite go2026llmprior %}.

The broader goal is a prior-to-posterior-to-control pipeline applicable to
any domain where expert knowledge exists but data from the target regime
does not yet.

**Paper**: *Enabling Robust Epidemic Control via LLM-Elicited Causal Discovery*.
Submitted to the AI for Science Workshop, ICML 2026. *(Under review)*