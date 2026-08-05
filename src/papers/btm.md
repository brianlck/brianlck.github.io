---
title: "Beckmann Transport Models: From Autonomous Flows to One-Step Maps"
date: Jul 2025
authors: ["Florentin Coeurdoux", "Peter Potaptchik", "Yilun Du", "Michael Albergo", "Eric Vanden-Eijnden"]
image: btm.mp4
link: https://arxiv.org/pdf/2608.01692
---
We propose an instantiation of flow matching that relies on a time-independent velocity field (an autonomous flow) to exactly map between two distributions, so long as the target is singular, i.e. supported on a lower-dimensional data manifold.

We also show that the one-step generative map associated with this flow is the unique solution of a simple conservation equation, which can be used to learn the map directly from samples.

These autonomous flows and maps give a dynamical meaning to the flux constraint of Beckmann’s transportation problem. Their construction provides a unifying framework that recovers, for instance, the closed-form Poisson-flow generative model and equilibrium matching with a quadratic flowmatching regression loss.

We illustrate how this theory corrects inconsistencies in existing methods and demonstrate the effectiveness of the autonomous flow and the one-step map on ImageNet 256x256.
