---
title: Debiasing Guidance with Sequential Monte Carlo
date: Jan 2025
authors: ["Paul Jeha", "Jes Frellsen", "Michael Albergo", "Pietro Lio", "Francisco Vargas"]
image: smc-guidance.jpg
link: https://arxiv.org/abs/2502.06079
---

Discrete diffusion models are a class of generative models that produce samples from an approximated data distribution within a discrete state space. Often, there is a need to target specific regions of the data distribution. Current guidance methods aim to sample from a distribution with mass proportional to $p_0(x_0)p(\zeta|x_0)^\alpha$ but fail to achieve this in practice. We introduce a Sequential Monte Carlo algorithm that generates unbiasedly from this target distribution, utilising the learnt unconditional and guided process. We validate our approach on low-dimensional distributions, controlled images and text generations. For text generation, our method provides strong control while maintaining low perplexity compared to guidance-based approaches.
