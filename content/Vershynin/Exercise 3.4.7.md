---
title: Exercise 3.4.7
draft: false
tags:
  - Probability
---

## Problem 
Exercise 3.4.7 (Uniform distribution on the Euclidean ball) Extend Theorem 3.4.6 for the uniform distribution on the Euclidean ball $B(0, \sqrt{n})$ in $\mathbb{R}^n$ centered at the origin and with radius $\sqrt{n}$. Namely, show that a random vector

$$
X \sim \operatorname{Unif}(B(0, \sqrt{n}))
$$

is sub-gaussian, and

$$
\|X\|_{\psi_2} \leq C
$$

## Proof
As in the proof of Theorem 3.4.6, we first represent $X$ in the polar coordinates.
Let $R \sim U([0,1]), \; Y \sim U(\sqrt{n} S^{n-1})$ be independent random variables. Then, we can represent $X$ as $X = R^{1/n} Y$. (This is because radius $R$ has a distribution on $[0,1]$ with density $f_R(r) = n r^{n-1}$, which is proved using polar coordinate representation of the volume of the ball $dg = r^{n-1} dr d\sigma(\theta)$.) 

Thus, we have, for all $t > 0$ and $x \in S^{n-1}$,
$$ \mathbb{E}[ \langle X , x\rangle^2 / t^2 ] \leq \mathbb{E}[ R^2 \langle Y , x\rangle^2 / t^2 ] \leq \mathbb{E}[ \langle Y , x\rangle^2 / t^2 ] $$ because $R \in [0,1]$.

Therefore, $$|| \langle X, x \rangle ||_{\psi_2} \leq || \langle Y, x \rangle ||_{\psi_2} \leq C. $$


Or equivalently, since $\mathbb{P} ( |X| \geq t ) = \mathbb{P} ( |R^{1/n} Y| \geq t ) \leq \mathbb{P} ( |Y| \geq t )$ for all $t > 0$, we have $||X||_{\psi_2} \leq C$.