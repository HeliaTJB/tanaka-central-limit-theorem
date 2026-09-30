# Tanaka Central Limit Theorem

[![Course](https://img.shields.io/badge/Course-Probability%20and%20Statistics-blue)](https://github.com/HeliaTJB/tanaka-central-limit-theorem)
[![University](https://img.shields.io/badge/University-Sharif%20University%20of%20Technology-red)](https://www.sharif.edu/)
[![Topic](https://img.shields.io/badge/Topic-Probability%20Theory-purple)](https://github.com/HeliaTJB/tanaka-central-limit-theorem)

## Overview

This project studies the **Tanaka Central Limit Theorem** and its relationship to the classical Central Limit Theorem through the framework of **Wasserstein distance**.

The classical Central Limit Theorem describes convergence of normalized sums of independent and identically distributed random variables to a Gaussian distribution in the sense of **weak convergence**. The Tanaka Central Limit Theorem provides a stronger form of convergence by considering the **Wasserstein distance**, which also captures information related to moments.

The project focuses on developing the probabilistic framework required to understand this stronger notion of convergence and following the main ideas behind the proof of the Tanaka Central Limit Theorem.

---

## Project Goals

The main goals of the project were to:

* Review the mathematical foundations of probability theory required for the analysis.
* Understand weak convergence of probability measures.
* Study Wasserstein distance and its optimal-transport interpretation.
* Examine the relationship between weak convergence and Wasserstein convergence.
* Understand the role of couplings and quantile representations.
* Study the main arguments leading to the Tanaka Central Limit Theorem.
* Compare the Wasserstein formulation with the classical weak form of the Central Limit Theorem.

---

## Mathematical Background

As preparation, we studied probability theory using:

> Lasse Leskelä, *Probability Theory: A Fast Course*, Aalto University, 2024.

The topics most relevant to the project included:

* Probability spaces and probability measures
* Random variables and their distributions
* Expectation and integration
* Independence
* Moments
* Weak convergence
* Probability metrics
* Couplings
* Wasserstein distances
* Central Limit Theorems

This theoretical preparation provided the background needed to move from the classical formulation of the Central Limit Theorem toward stronger modes of convergence.

---

## From Weak Convergence to Wasserstein Convergence

A central theme of the project is the distinction between **weak convergence** and **Wasserstein convergence**.

For a sequence of probability measures $\mu_n$, weak convergence describes convergence in distribution. However, weak convergence alone does not generally guarantee convergence of moments.

For probability measures with finite $p$-th moments, the $p$-Wasserstein distance is defined by

$$
W_p(\mu,\nu)
=
\inf_{(X,Y)\in\Gamma(\mu,\nu)}
\left(\mathbb{E}|X-Y|^p\right)^{1/p}.
$$

Here, $\Gamma(\mu,\nu)$ denotes the set of all couplings of $\mu$ and $\nu$.

For this project, particular attention was given to the case $p=2$.

The Wasserstein framework therefore provides a way to study convergence that contains information beyond convergence in distribution.

---

## Tanaka Central Limit Theorem

Let $X_1,X_2,\ldots$ be independent and identically distributed random variables satisfying

$$
\mathbb{E}[X_1]=0,
\qquad
\mathbb{E}[X_1^2]=1.
$$

Consider the normalized sums

$$
\zeta_n
=
\frac{X_1+\cdots+X_n}{\sqrt{n}}.
$$

The classical Central Limit Theorem states that

$$
\zeta_n \Rightarrow Z,
$$

where $Z$ is a standard Gaussian random variable.

The Tanaka formulation studies this convergence in the Wasserstein metric, providing a stronger form of convergence under the appropriate moment assumptions.

---

## Main Proof Strategy

The project follows the proof through several intermediate ideas.

### 1. Dyadic Subsequence

A key step is to first consider the dyadic subsequence

$$
\eta_k = \zeta_{2^k}.
$$

This leads to the recursive representation

$$
\eta_{k+1}
=
\frac{\eta_k+\eta_k'}{\sqrt{2}},
$$

where $\eta_k'$ is an independent copy of $\eta_k$.

This recursive structure makes it possible to analyze how the relevant distance to the Gaussian distribution evolves as the number of summed random variables increases.

### 2. Wasserstein-Based Distance

The proof introduces a quantity measuring the distance between the distribution of the normalized sum and the Gaussian distribution.

Using the properties of Wasserstein distance and the behavior of sums of independent random variables, the sequence of these distances can be controlled along the dyadic subsequence.

### 3. Equality and the Gaussian Case

An important ingredient is an inequality for the relevant functional under normalized addition of independent random variables.

The equality case is particularly important: equality occurs in the relevant setting only for Gaussian distributions.

This characterization connects the behavior of the distance functional with the Gaussian distribution appearing in the Central Limit Theorem.

### 4. Moment Bounds

Moment estimates are used to control the sequence and establish the required limiting behavior.

In particular, bounded higher moments provide the necessary control for passing from the dyadic construction to the limiting result.

### 5. From Powers of Two to General $n$

After establishing the result for the dyadic subsequence, the argument is extended to arbitrary $n$.

The binary representation of $n$ provides a way to decompose a general normalized sum into components associated with powers of two, allowing the dyadic result to be transferred to the full sequence.

---

## An Alternative Perspective

The project also considers another route to the Wasserstein version of the Central Limit Theorem.

The classical CLT already gives

$$
\zeta_n \Rightarrow Z.
$$

Under the appropriate convergence of second moments, weak convergence can then be combined with the characterization of Wasserstein convergence to obtain convergence in $W_2$.

This provides two complementary perspectives:

```text
                 Classical CLT
                      |
                      v
              Weak Convergence
                      |
             + Moment Control
                      |
                      v
            Wasserstein Convergence


             Tanaka's Approach
                      |
                      v
          Wasserstein-Based Analysis
                      |
                      v
           Direct Control of the
           Distance to the Gaussian
```

Studying both perspectives helped clarify the relationship between different modes of convergence in probability theory.

---

## Key Concepts

The project brings together several concepts from probability theory:

| Concept                 | Role in the Project                                       |
| ----------------------- | --------------------------------------------------------- |
| Weak convergence        | Classical mode of convergence in the CLT                  |
| Wasserstein distance    | Metric for comparing probability distributions            |
| Couplings               | Mathematical construction underlying Wasserstein distance |
| Quantile representation | Characterization of Wasserstein distance on the real line |
| Moments                 | Additional information required for stronger convergence  |
| Gaussian distribution   | Limiting distribution in the CLT                          |
| Dyadic subsequences     | Main structure used in the proof                          |
| Independent sums        | Recursive structure of normalized sums                    |

---

## What I Learned

This project provided a deeper look at probability theory beyond the standard statement of the Central Limit Theorem.

In particular, it helped develop an understanding of:

* how different notions of convergence compare;
* why convergence in distribution does not by itself control moments;
* how Wasserstein distance connects probability theory with optimal transport;
* how couplings can be used to compare probability distributions;
* how recursive structures can simplify the analysis of normalized sums;
* how Gaussian distributions arise as a distinguished equality case in the relevant inequalities.

More broadly, the project strengthened my interest in the mathematical structure underlying probabilistic models and statistical learning.

---

## References

### Main Text

Lasse Leskelä, *Probability Theory: A Fast Course*, Aalto University, 2024.

### Original Tanaka Paper

Hiroshi Tanaka,
“An Inequality for a Functional of Probability Distributions and Its Application to Kac’s One-Dimensional Model of a Maxwellian Gas,”
*The Annals of Probability*, 6(2), 1978, 283–292.

DOI: `10.1214/aop/1176995535`

### Additional Reference

Cédric Villani, *Optimal Transport: Old and New*, Springer, 2009.

---

## Project Information

**Course:** Probability and Statistics (25732)
**Department:** Electrical Engineering
**University:** Sharif University of Technology
**Semester:** Fall 2025

### Team

* **Helia Tajabadi** — [GitHub](https://github.com/HeliaTJB)
* Behrad Mohammadian
* **Amirali Jahanbakhsh** — [GitHub](https://github.com/AmirAli-jb)
* Hana Akhavan

---

## Repository Contents

```text
tanaka-central-limit-theorem/
│
├── TanakaCLT.pdf
│   └── Project report
│
└── README.md
    └── Project overview and mathematical summary
```
