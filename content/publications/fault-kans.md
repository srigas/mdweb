+++
authors = ["Spyros Rigas", "Michalis Papachristou", "Ioannis Sotiropoulos", "Georgios Alexandridis"]
title = "Explainable Fault Classification and Severity Diagnosis in Rotating Machinery using Kolmogorov-Arnold Networks"
date = "2025-04-09"
math = true
description = "Explainable Fault Classification and Severity Diagnosis in Rotating Machinery using Kolmogorov-Arnold Networks"
+++


In this open-access paper, available [here](https://www.mdpi.com/1099-4300/27/4/403), we introduce an explainable, efficient and adaptive framework based on Kolmogorov-Arnold Networks (KANs) for fault detection, classification and severity diagnosis in rotating machinery. The framework utilizes automatic feature selection and symbolic regression techniques to create interpretable models suitable for real-time condition monitoring.

## What Are Kolmogorov-Arnold Networks (KANs)?

KANs are neural network architectures inspired by the Kolmogorov-Arnold representation theorem, distinguished by their use of trainable symbolic activation functions. This design makes KANs highly interpretable, overcoming the common "black-box" limitations of traditional neural networks.

## Main Contributions

- **Automatic and Explainable Feature Selection**: 
  We employ sparsity-inducing regularization coupled with an explicit feature attribution mechanism, enabling our framework to automatically select the most informative features from extensive sensor data.

- **Unified Fault Diagnosis Framework**:
  Our approach handles multiple tasks seamlessly; fault detection, detailed fault classification (e.g., bearing faults, imbalance, misalignment), and severity estimation, all within a consistent, unified methodology.

- **Interpretable Symbolic Models**:
  Activation functions trained in KANs are approximated by symbolic mathematical expressions, significantly enhancing the interpretability of our models. 

- **High Performance and Real-world Applicability**:
  Tested extensively on the widely-recognized CWRU and MaFaulDa datasets, our models consistently achieved perfect or near-perfect F1-scores, demonstrating adaptability across diverse fault scenarios and highlighting potential applications in industrial monitoring systems.

## Framework Overview

Our methodology comprises distinct stages, including data augmentation, automated feature extraction and selection, adaptive hyper-parameter tuning and symbolic regression, ensuring both interpretability and predictive performance.

Below is a visualization of the complete KAN-based fault diagnosis framework, illustrating how the different phases integrate into an interpretable and efficient pipeline:


![Framework Overview](/images/Paper3/framework.png)


{{< highlight html >}}
@article{e27040403,
      author = {Rigas, Spyros and Papachristou, Michalis and Sotiropoulos, Ioannis and Alexandridis, Georgios},
      journal = {Entropy}, 
      title = {Explainable Fault Classification and Severity Diagnosis in Rotating Machinery Using Kolmogorov–Arnold Networks}, 
      year = {2025},
      volume = {27},
      number = {4},
	  article-number = {403},
      doi = {10.3390/e27040403}
}
{{< /highlight >}}