---
layout: page
title: Goal-Driven Bayesian Experimental Design
description: Optimizing experiments for downstream scientific decisions under uncertainty
importance: 1
category: research
related_publications: true
---

Standard Bayesian optimal experimental design (BOED) maximizes the expected information gain (EIG) about model parameters. However, scientific workflows often care about **downstream decisions** rather than parameters themselves. This project develops goal-driven BOED frameworks that directly optimize experiments for decision quality, robustness, and task-specific utility.

Key contributions include incorporating uncertain priors into BOED for risk-averse
experiment selection, proposing robust EIG using ambiguity sets to handle prior
misspecification {% cite go2022robust %}, and developing sequential BOED frameworks
with latent-variable neural operator surrogates for time-dependent PDE-governed
systems {% cite go2025sequential %}.

We use derivative-informed neural operators (DINO) and latent-variable attention-based
neural operators (LANO) to accelerate EIG computation, reducing the cost of design
optimization by orders of magnitude compared to Monte Carlo baselines {% cite go2025accurate %}.

Applications include source localization, epidemiological control, and PDE-governed
parameter estimation.
