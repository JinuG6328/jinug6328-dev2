---
layout: page
title: Bayesian Optimal Experimental Design
description: Optimizing experiments to reduce parameter uncertainty in complex scientific systems
importance: 1
category: research
related_publications: true
img: assets/img/boed.png
---

Bayesian optimal experimental design (BOED) asks: *which experiment should we
run next to learn the most?* While powerful, classical BOED faces two core
challenges. It is computationally expensive for complex scientific models,
and it assumes a fixed, well-specified prior that may not reflect reality.
This project addresses both limitations, and pushes BOED toward a third
frontier: optimizing experiments for **downstream decisions**, not just
parameter estimation.

### Scalable BOED with Neural Operators

Computing expected information gain (EIG) — a measure of how much an
experiment is expected to reduce uncertainty about model parameters — requires
repeated model evaluations, making it prohibitively expensive for PDE-governed
systems. We replace costly forward models with **derivative-informed neural
operators (DINO)** and **latent-variable attention-based neural operators
(LANO)** as surrogates, reducing EIG computation by orders of magnitude while
maintaining accuracy. This enables sequential BOED for time-dependent PDE
systems at practical cost {% cite go2025accurate go2025sequential %}.

### Robust BOED under Prior Uncertainty

Classical BOED is sensitive to the choice of prior — a misspecified prior
leads to poorly designed experiments. We address this with a
**distributionally robust EIG** formulation using ambiguity sets, which
produces risk-averse experiment selections that remain reliable even when
prior beliefs are imperfect {% cite go2022robust %}. This work received an
**Oral Presentation (Top 5%)** at UAI 2022.

### Goal-Driven Design for Scientific Decisions

Parameter estimation is rarely the end goal. In epidemiological control, for
instance, the real objective is to inform intervention policy, not to estimate
transmission rates. We are developing frameworks that directly optimize
experiments for downstream decision quality, with ongoing work extending this
toward optimal control in scientific and engineering systems.

### LLM-Informed Priors

A deeper challenge in BOED is constructing priors that faithfully reflect
domain knowledge. We are actively investigating how **large language models**
can serve as structured, domain-aware priors for scientific inference,
providing richer prior distributions that improve both experimental design
and downstream decision-making.