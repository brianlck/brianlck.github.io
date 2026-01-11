---
title: Tilt Matching
date: Jan 2026
authors: ["Peter Potaptchik", "Michael Albergo"]
image: tilt-matching.png
link: https://www.arxiv.org/abs/2512.21829
---
We propose a simple, scalable algorithm for using stochastic interpolants to sample from unnormalized densities and for fine-tuning generative models. The approach, Tilt Matching, arises from a dynamical equation relating the flow matching velocity to one targeting the same distribution tilted by a reward, implicitly solving a stochastic optimal control problem. The new velocity inherits the regularity of stochastic interpolant transports while also being the minimizer of an objective with strictly lower variance than flow matching itself. The update to the velocity field can be interpreted as the sum of all joint cumulants of the stochastic interpolant and copies of the reward, and to first order is their covariance. The algorithms do not require any access to gradients of the reward or backpropagating through trajectories of the flow or diffusion. We empirically verify that the approach is efficient and highly scalable, providing state-of-the-art results on sampling under Lennard-Jones potentials and is competitive on fine-tuning Stable Diffusion, without requiring reward multipliers. It can also be straightforwardly applied to tilting few-step flow map models.

The theoretical groundwork of this algorithm is mostly developed by Peter and Michael, please reach out to them for any question.
