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

### Probabilistic or surrogate models
Suppose we have a set of samples "${ x\\_1, x\\_2, ..., x\\_n }$"," each with corresponding stochastic observations "{ y\\_1, y\\_2, ..., y\\_n }" in our dataset "$\mathcal{D}$". The surrogate model is a probabilistic model that provides information about the underlying unknown objective function based on the available data. In other words, it helps us approximate the underlying distribution "$p(y|x)$" for any "$x \in \mathcal{D}$". 
<!-- Since $y$ is often a noisy estimate of the true function $f$, we express it as $y = f(x) + \epsilon$, where $\epsilon$ represents the noise or stochasticity in the observations. -->

<!-- In the literature, surrogate models can be broadly categorized into two types: \textbf{parametric} and \textbf{non-parametric}. Parametric models use a fixed number of parameters to approximate the objective function. For example, if we employ $n$ Gaussian mixture models, we need to estimate $2n$ parameters, such as the means $\mu$ and variances $\sigma^2$. In contrast, non-parametric models do not assume a specific form for the underlying function. They do not rely on a predetermined number of parameters but can flexibly increase the number of parameters as more data becomes available. This adaptability makes non-parametric models well-suited for infinite-dimensional spaces, where they effectively use a finite subset of these parameters to approximate the data we have. Instead of fitting the observed data to a pre-defined distribution, non-parametric models estimate what the underlying distribution might be based on the observed data.

Regardless of the approach, the primary objective is to approximate the relationship between $x$ and $y$. Bayes' theorem allows us to update our beliefs of the distribution by the posterior distribution over the surrogate model parameters as new data is observed. Thus, both parametric and non-parametric models utilize the following equation:
\begin{equation*}
    p(y|x) = \frac{p(x|y)p(y)}{p(x)} = \frac{p(x|y)p(y)}{\int p(x|y)p(y)dy}
\end{equation*}
where $p(y)$ is the prior distribution representing our initial beliefs about $y$, $p(x|y)$ is the likelihood of observing $x$ given $y$, and $p(x)$ is the marginal probability of $x$ under all possible values of $y$. Bayesian inference enables us to refine our estimates of the relationship between $x$ and $y$ by combining prior knowledge with new observations. -->