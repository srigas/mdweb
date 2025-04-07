+++ 
authors = ["Spyros Rigas", "Michalis Papachristou"] 
title = "jaxKAN: A Unified JAX Framework for Kolmogorov-Arnold Networks" 
date = "2025-04-07" 
math = true 
description = "jaxKAN: A Unified JAX Framework for Kolmogorov-Arnold Networks" 
+++ 

In this open-access JOSS paper, available [here](https://doi.org/10.21105/joss.07830), we introduce **jaxKAN**, a high-performance JAX-based library for building and training Kolmogorov-Arnold Networks (KANs). Designed for both general-purpose and scientific applications, jaxKAN supports adaptive training, hybrid KAN architectures and Physics-Informed Kolmogorov-Arnold Networks (PIKANs).


## Highlights

- **Multiple Layer Types**: Includes B-spline, Chebyshev, Legendre, RBF, Fourier and other layer types, all available through a consistent API.
- **Adaptive Training Routines**: Grid updates, basis order extension and optimizer-aware state transitions are built-in.
- **Specialized PDE Tools**: High-level utilities for solving PDEs using PIKANs are included, e.g., the `train_PIKAN` function.
- **Performance**: Achieves significant speedups over prior work and supports batched least-squares operations not natively available in JAX.


{{< highlight html >}}
@article{Rigas2025,
  title = {jax{KAN}: A unified {JAX} framework for {K}olmogorov-{A}rnold Networks},
  journal = {Journal of Open Source Software},
  year = {2025},
  volume = {10},
  number = {108},
  pages = {7830},
  doi = {10.21105/joss.07830}
}
{{< /highlight >}}
