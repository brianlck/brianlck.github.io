---
title: Debiasing Guidance with Sequential Monte Carlo
date: Jan 2025
authors: ["Paul Jeha", "Jes Frellsen", "Michael Albergo", "Pietro Lio", "Francisco Vargas"]
image: smc-guidance.jpg
link: https://arxiv.org/abs/2502.06079
---
Guidance in diffusion models are biased. By using a specific choice of intermediate distribution, this bias can be corrected with Sequential Monte Carlo without extra function evaluations.

Also see concurrent work [Feynman-Kac Correctors](https://arxiv.org/abs/2503.02819) for a similar scheme, and follow-up work [Radon-Nikodym Estimators](https://arxiv.org/abs/2506.05668) for a more systematic approach to derive Sequential Monte Carlo schemes for general targets.