# tanaka-central-limit-theorem


This repository contains our study and mathematical analysis of the **Tanaka Central Limit Theorem**, with a focus on understanding the role of **Wasserstein distance** and its relationship to weak convergence in probability.

The project was carried out as part of the **Probability and Statistics (25732)** course at **Sharif University of Technology**. Our main goal was to study a stronger form of the classical Central Limit Theorem and understand the mathematical ideas underlying its proof.

## Overview

The classical Central Limit Theorem states that, under suitable assumptions, normalized sums of independent and identically distributed random variables converge to a Gaussian distribution.

In the standard formulation studied in class, this convergence is understood in the sense of **weak convergence**. The Tanaka Central Limit Theorem provides a stronger perspective by considering convergence with respect to the **Wasserstein distance**.

This project therefore focuses on the mathematical framework needed to move from weak convergence to Wasserstein convergence and to understand the proof of the Tanaka Central Limit Theorem.

## Theoretical Preparation

As preparation for the project, we studied probability theory using:

> Lasse Leskelä, *Probability Theory: A Fast Course*, Aalto University, 2024.

The book provides a rigorous introduction to probability theory with particular emphasis on measure-theoretic probability, probability measures, convergence, and metrics between probability measures.

Our study focused on the concepts that were directly relevant to the project, including:

* Probability spaces and measures
* Sigma-algebras and Borel sets
* Random variables and their laws
* Expectation and integration
* Independent random variables
* Second-moment analysis
* Random sequences and limits
* Weak convergence of probability measures
* Probability metrics
* Couplings
* Wasserstein distances
* Central Limit Theorems
* The Tanaka Central Limit Theorem

These topics form the theoretical foundation for the arguments developed in the project.

## From Weak Convergence to Wasserstein Convergence

One of the central ideas of the project is the distinction between different notions of convergence of probability distributions.

Weak convergence can be characterized through convergence of expectations of bounded continuous functions. However, weak convergence alone does not guarantee convergence of moments.

We therefore studied the **Wasserstein distance**, defined for probability measures with finite \(p\)-th moments by

$$
W_p(\mu,\nu)
=
\inf_{(X,Y)\sim\Gamma(\mu,\nu)}
\left(
\mathbb{E}[|X-Y|^p]
\right)^{1/p},
$$

where \(\Gamma(\mu,\nu)\) denotes the set of all couplings of \(\mu\) and \(\nu\).

We also developed the interpretation of Wasserstein distance as an **optimal transportation cost** between two probability distributions.

## Main Mathematical Ingredients

The proof was developed through several intermediate results.

### 1. Couplings and Wasserstein Distance

We introduced couplings of probability distributions and used them to define the Wasserstein metric.

The optimal-transport interpretation provides an intuitive way to understand the distance: probability mass is transported from one distribution to another, with the transportation cost determined by the distance between the corresponding points.

### 2. Weak and Wasserstein Convergence

We examined the relationship between weak convergence and Wasserstein convergence.

In particular, we showed how convergence in Wasserstein distance implies weak convergence and investigated the additional moment condition required to obtain Wasserstein convergence.

### 3. Quantile Representation

For probability distributions on the real line, we studied the representation of Wasserstein distance using quantile functions. This provides a convenient way to construct optimal couplings and calculate Wasserstein distances.

### 4. A Subadditivity Property

An important ingredient in the proof is the inequality for independent random variables

$$
\mathbb{E}[X+Y]
\leq
\mathbb{E}[X]+\mathbb{E}[Y],
$$

with equality characterized by the Gaussian case in the relevant setting.

This property allows the behavior of normalized sums to be controlled through the corresponding Wasserstein distances.

## Tanaka Central Limit Theorem

Let \(X_1,X_2,\ldots\) be independent and identically distributed random variables satisfying

$$
\mathbb{E}[X_i]=0,
\qquad
\operatorname{Var}(X_i)=1,
$$

and define the normalized partial sums

$$
\zeta_n
=
\frac{X_1+\cdots+X_n}{\sqrt n}.
$$

The classical Central Limit Theorem gives convergence of the distribution of \(\zeta_n\) to the standard Gaussian distribution in the weak sense.

The objective of this project was to understand how this convergence can be strengthened to convergence in the **Wasserstein metric**.

For the main argument, we considered the sequence

$$
\eta_k = \zeta_{2^k}.
$$

Using the decomposition of sums at consecutive powers of two, we obtained a recursive relation between successive elements of this sequence. Combined with the subadditivity property and moment bounds, this allowed us to show that the corresponding Wasserstein distance converges to zero.

The argument was then extended from powers of two to arbitrary \(n\) by expressing \(n\) in its binary representation.

## Proof Strategy

The overall structure of the proof can be summarized as:

```text
Probability Theory
       │
       ▼
Couplings
       │
       ▼
Wasserstein Distance
       │
       ▼
Weak Convergence
       │
       ▼
Moment Conditions
       │
       ▼
Subadditivity / Gaussian Characterization
       │
       ▼
Normalized Sums
       │
       ▼
Dyadic Subsequence ηₖ = ζ₂ᵏ
       │
       ▼
Convergence of the Subsequence
       │
       ▼
Extension to Arbitrary n
       │
       ▼
Tanaka Central Limit Theorem
```

## Alternative Proof Perspective

We also considered an alternative route.

Once the classical Central Limit Theorem is established under weak convergence, the result concerning Wasserstein convergence can be obtained by combining weak convergence with the appropriate convergence condition on the second moments.

This provides a useful comparison between:

1. proving the Wasserstein version directly, and
2. deriving it from the classical weak form of the Central Limit Theorem together with the characterization of Wasserstein convergence.

## References

### Main Text

Lasse Leskelä,
*Probability Theory: A Fast Course*,
Aalto University, 2024.

### Original Tanaka Paper

Hiroshi Tanaka,
“An Inequality for a Functional of Probability Distributions and Its Application to Kac’s One-Dimensional Model of a Maxwellian Gas,”
*The Annals of Probability*, 6(2), 1978, pp. 283–292.

DOI: `10.1214/aop/1176995535`

### Additional Reference

Cédric Villani,
*Optimal Transport: Old and New*,
Springer, 2009.

## Project Team

* Helia Tajabadi
https://github.com/HeliaTJB



* Behrad Mohammadian


* Amirali Jahanbakhsh
  https://github.com/AmirAli-jb


  
* Hana Akhavan



**Course:** Probability and Statistics - Dr. Mojahedian (25732)
**Department:** Electrical Engineering, Sharif University of Technology
**Semester:** Fall 2025


