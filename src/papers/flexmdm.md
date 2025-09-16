---
title: Any-Order Flexible Length Masked Diffusion
date: Aug 2025
authors: ["Jaeyeon Kim", "Carles Domingo-Enrich", "Sham Kakade", "Yilun Du", "Timothy Ngotiaoco", "Sitan Chen", "Michael Albergo"]
image: flexmdm_animation.mp4
link: https://flexmdm.github.io/
---
Masked Diffusion Models (MDM) have been a promising alternative to autoregressive models, with recent scaling-up efforts, e.g., LLaDA, Dream7B, Mercury, Gemini Diffusion. Despite these successes, they struggle to (1) model variable-length sequence distributions and (2) insert new tokens during generation.

FlexMDM addresses these issues: By baking in the ability to insert mask tokens, FlexMDM exhibits superior performance over masked diffusion in planning and reasoning tasks where length flexibility is crucial.

FlexMDM scales up to 8B parameters—we retrofit LLaDA, an 8B open-sourced pretrained MDM, and fine-tune it using 1000 H100 GPU hours. FlexMDM's ability to insert new tokens in arbitrary positions enables better reasoning capabilities on real-world reasoning tasks such as math (GSM8K) and code infilling (Humaneval-infill). Compared to MDM, FlexMDM achieves superior performance on math (GSM8K, 58%→67%) and code infilling (52%→65%)