# Lecture 9: Transformation

## Transformation

- We have a random variable,$X$, with a given distribution. Then we apply some function $h(.)$ to that random variable.
- What we are concerned with is what is the distribution of the new random variable $h(X)$.
- There are multiple methods that we could determine what the distribution of $h(X)$ is.

## 1: Method of Distribution Function (CDF Approach)

Let $X$ be a R.V. with CDF $F_{X}(x)$, and let $U=h(X)$. Steps:

1. Find the formula for the CDF of $U$ based on the distribution of $X$. i.e., find $F_{U}(u)=P(U\leq u)=P(h(x)\leq u)$

2. Differentiate $F_{U}(u)$ to find the pdf of $U$(only works in the continuous case).
## 2: Method of Transformation (Formula Approach)

Let $X$ be a random variable with pdf $f_{X}(x)$ and let $U=h(X)$. Steps:

1. Verify that $h(X)$ is either increasing or decreasing over the support of $X$. ($h$ should be monotonous function over support of $X$)


2. Find $h^{-1}(u)$ s.t. $h(X)= U \implies h^{-1}(U)=X$
3. Find derivative $\frac{d}{du}h^{-1}(u)$
4. Final step: $f_{U}(u) =f_{X}(h^{-1}(u))\left|\frac{d}{du}h^{-1}(u)\right|$

## 3: Method of MGF

Let $X$ be a R.V. with MGF $M_{X}(t)$, and let $U=h(X)$. Steps:

1. Note:
$$
M_{U}(t) = E[e^{tU}] = E[e^{th(X)}]
$$

2. Identify the form of $M_{U}(t)$ as that of a known MGF.
3. Based on the MGF, identify the pdf of $U$.
