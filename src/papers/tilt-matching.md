---
title: Tilt Matching for Scalable Sampling and Fine-Tuning
date: Jan 2026
authors: ["Peter Potaptchik", "Michael Albergo"]
image: tilt-matching.png
link: https://www.arxiv.org/abs/2512.21829
---
We introduce Tilt Matching, a method for aligning pretrained flow-based generative models with a reward function by fine-tuning them sequentially through intermediate distributions. By characterising the necessary updates in drift along the interpolating path, this framework yields two algorithms: Explicit Tilt Matching, which relies on a first-order Euler approximation, and Implicit Tilt Matching, an importance sampling scheme with a learnable control variate that provably reduces variance.
