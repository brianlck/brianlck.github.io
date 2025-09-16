---
title: Any-Order Flexible Length Masked Diffusion
date: Aug 2025
authors: ["Jaeyeon Kim", "Carles Domingo-Enrich", "Sham Kakade", "Yilun Du", "Timothy Ngotiaoco", "Sitan Chen", "Michael Albergo"]
image: flexmdm_animation.mp4
link: https://flexmdm.github.io/
---
We introduce FlexMDM, a class of masked diffusion models for variable-length data that operates by inserting and subsequently unmasking tokens. The model's construction relies on the joint interpolant, an extension of the stochastic interpolant for defining more general interpolation paths (see [EditFlow](https://arxiv.org/abs/2506.09018) for an equivalent formulation).

We show that FlexMDM retains the any-order sampling guarantees of masked diffusion as established in prior [work](https://arxiv.org/abs/2502.06768) by Jaeyeon Kim and Kulin Shah.

In collaboration with the wonderful Jaeyeon Kim, we demonstrate that the method scales to 8B parameters and achieves notable performance improvements over previous masked diffusion models.