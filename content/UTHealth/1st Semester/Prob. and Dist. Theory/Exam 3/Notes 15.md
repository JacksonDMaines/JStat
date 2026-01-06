# Lecture 15: Modes of Convergence

## 1 Motivation

In statistical theory, we often analyze sequences of random variables, especially sample means, and study how they

behave as the sample size $n→∞$. This requires a precise understanding of several modes of convergence:

1. Convergence in probability
2. Almost sure convergence
3. Convergence in distribution

These modes form the foundation of the Laws of Large Numbers (LLNs), the Central Limit Theorem (CLT), and asymptotic inference.

## 2 Convergence in Probability

**Definition** A sequence of random variables $X_{n}$ converges in probability to a random variable $X$ if for all $ε >0$,
$$
\lim_{ n \to \infty } P(|X_{n}-X| \geq \epsilon) = 0

$$
or equivalently,
$$
P(|X_{n}-X|< \epsilon) \rightarrow 1
$$

### 2.1 Weak Law of Large Numbers

**Theorem:**  Let $X_{1}, X_{2}, \dots$ be i.i.d. random variables with $E(X_{i}) = \mu$ and variacne $Var(X_{i}) = \sigma^2<\infty$. Let $\bar{X} = \frac{1}{n}\sum_{i=1}^n X_{i}$. THen for every $\epsilon > 0$ 
$$
P(|X_{n}-X|) \rightarrow 1
$$
that is, $\bar{X}_{n} converges in probability to $\mu$. Donate: $\bar{X}_{n}\rightarrow^P \mu$

Properties

- The Weak Law of Large Numbers (WLLN) quite elegantly states that, under general conditions, the sample mean approaches the population mean as $n→∞$.
- The property summarized by the WLLN, that a sequence of the “same” sample quantity approaches a constant as $n→∞$, is known as **consistency**.

## 3 Almost Sure Convergence

**Definition:** A sequence of random variables $X_{1} ,X_{2} ,...,X_{n}$ converges almost surely to a random variable $X$ if, for every $\epsilon > 0$ 
$$
P(\lim_{ n \to \infty } |X_{n}-X|<\epsilon) = 1
$$

### Strong Law of Large Numbers (SLLN)

**Definition:** Let $X_{1} ,X_{2} ,...$be iid random variables with $E[X_{i}]=μ$ and $Var(X_{1})= σ^2<\infty$, and define $\bar{X}_{n} = \frac{1}{n}\sum_{i=1}^n X_{i}$. Then, for every $\epsilon > 0$, 
$$
P(\lim_{ n \to \infty } |X_{n}-\mu|<\epsilon) = 1
$$
that is, $\bar{X_{n}}$ converges almost surely to $\mu$. 

Convergence almost surely, being a strong er criterion, implies convergence in probability. 

## 4 Convergence in Distribution

**Definition:** A sequence of random variables, $X_{1} ,X_{2} ,...$, converges in distribution to a random variable $X$ if

$$
\lim_{ n \to \infty }F_{X_{n}}(x) = F_{X}(x)
$$
at all points $x$ where $F_{X}(x)$ is continuous.


## 6 Central Limit Theorem (CLT)

**Theorem:** If $X_{1} ,...,X_{n}$ are i.i.d. with mean $μ$ and variance $σ^2<\infty$, then
$$
\sqrt{ n }(\bar{X}_{n}-\mu) \rightarrow^d N(0,\sigma^2)
$$ 




## 7 The Delta Method

Using these Taylor series approximations for the mean and variance, we get the following useful generalization of the Central Limit Theorem, known as the Delta Method.

**Theorem:** Let $Y_{n}$ be a sequence of random variables that satisfies $\sqrt{ n }(Y_{n}-\theta)\rightarrow N(0,\sigma^2)$ in distribution. For a given function $g$ and a specific value for $\theta$, suppose that $g'(\theta)$ exists and is not zero. Then

$$
\sqrt{ n }|g(Y_{n})-g(\theta)| \rightarrow N(0,\sigma^2[g'(\theta)]^2) \text{ in distribution}
$$

## 8 Summary Table


| Convergence Type | Notation                   | Meaning                                  |
| ---------------- | -------------------------- | ---------------------------------------- |
| Almost Sure      | $X_{n}\rightarrow^{a.s.}X$ | Pointwise w.p. 1                         |
| In Probability   | $X_{n}\rightarrow^P X$     | Probability of deviation $\rightarrow$ 0 |
| In Distribution  | $X_{n} \rightarrow^D X$    | CDF convergence                          |

| Result       | Convergence                                                |
| ------------ | ---------------------------------------------------------- |
| WLLN         | $\bar{X}_{n}\rightarrow ^P \mu$                            |
| SLLN         | $\bar{X}_{n}\rightarrow ^{a.s.} \mu$                       |
| CLT          | $\frac{\sqrt{ n }(\bar{X}_{n}-\mu)}{\sigma} \to ^D N(0,1)$ |
| Delta Method | $g(Y_{n})$ asymptotics                                     |
