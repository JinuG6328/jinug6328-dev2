---
layout: page
title: Generative Priors for High-Dimensional Bayesian Experimental Design
description: Pretrained diffusion models as flexible priors for scalable BOED in non-Gaussian, high-dimensional inverse problems
importance: 4
category: research
related_publications: true
---

Classical EIG estimation becomes computationally prohibitive when the unknown
parameter is high-dimensional and the posterior is non-Gaussian. This ongoing
work addresses this by using **pretrained diffusion models** as flexible priors
for sequential BOED.

The key idea is to interpret posterior sampling as a guided diffusion trajectory,
where the accumulated likelihood guidance along the latent path serves as a
tractable surrogate for information gain. This **MINDE-DPS** estimator requires
no additional nested Monte Carlo — the EIG estimate accumulates for free
alongside posterior samples {% cite go2026latent %}.

We validate the approach on source localization, CES, and Darcy flow parameter
estimation, including high-dimensional PDE-constrained settings where classical
methods struggle. Ongoing work explores **flow matching** as a faster alternative
for posterior sampling and EIG accumulation.