---
title: Tree-structured Parzen Estimator (TPE)
summary: This tutorial aims to introduce the concepts behind the Tree-structured Parzen Estimator (TPE) \citep{bergstra2011algorithms}, the default hyperparameter optimization algorithm in Optuna \citep{akiba2019optuna}. We will delve into key ideas in Bayesian optimization, such as surrogate models and acquisition functions, and demonstrate how TPE differs from Gaussian Processes (GP), another popular method for Bayesian optimization.
date: 2024-10-28
type: docs
math: true
tags:
  - TPE, Bayesian optimization
---

This tutorial aims to introduce the concepts behind the Tree-structured Parzen Estimator (TPE), the default hyperparameter optimization algorithm in Optuna. We will delve into key ideas in Bayesian optimization, such as surrogate models and acquisition functions, and demonstrate how TPE differs from Gaussian Processes (GP), another popular method for Bayesian optimization.

## Bayesian Optimization

Bayesian optimization (BO) is a technique for optimizing unknown functions based on observations. It involves making sequential decisions about which new points to evaluate, aiming to improve the optimization process by focusing on areas of the search space that are likely to yield better results. It utilizes a probabilistic model estimated from the observed data to guide sequential decision-making. In this section, we will introduce the core principles of BO to provide a foundation for understanding how TPE operates within this framework - [pseudo-code](#figure-bo) of the steps of BO.

{{< figure src="bo.png" id="bo" >}}