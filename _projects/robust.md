---
layout: page
title: Robust and Decision-Focused Bayesian Experimental Design
description: Beyond information gain — designing experiments for uncertain priors and downstream decisions
importance: 3
category: research
related_publications: true
img: assets/img/goboed.png
---

Standard BOED maximizes expected information gain (EIG), which measures how much
an experiment reduces parameter uncertainty on average. In practice, two
orthogonal limitations arise. The EIG objective is sensitive to the choice of
prior, and it treats all parameter uncertainty as equally valuable regardless of
whether it affects downstream decisions. My research addresses both limitations.


### Robustness to Prior Uncertainty

EIG rankings are sensitive to the prior distribution, and sampling-based EIG
estimators behave similarly to EIG under a perturbed prior. We propose
**robust expected information gain (REIG)**, which replaces the standard EIG
objective with a minimax formulation over an ambiguity set of distributions
close to the original prior in KL-divergence. We show that REIG corresponds
to a log-sum-exp stabilization of the samples used to estimate EIG, making it
efficient to implement as a drop-in replacement for standard estimators. REIG
improves robustness to prior misspecification and also compensates for the
variability of under-sampled EIG estimators {% cite go2022robust %}.


### Decision-Focused Design

Even with a well-specified prior, maximizing EIG does not necessarily improve
the quality of downstream decisions. Only specific parameter directions that
govern the constraints of a control problem truly matter. We propose
**GoBOED (Goal-driven BOED)**, a framework that couples BOED with a
differentiable convex decision layer equipped with plug-in risk functionals.
GoBOED directly optimizes experimental designs for a specified downstream
decision objective, rather than maximizing information gain alone.


### Key Takeaways

- REIG provides robustness to prior misspecification with minimal computational
  overhead over standard EIG estimators
- GoBOED targets parameter directions that matter for downstream decisions,
  rather than reducing all uncertainty uniformly
- Near-optimal design windows are substantially wider under GoBOED than under
  EIG maximization, offering practical flexibility in scheduling experiments