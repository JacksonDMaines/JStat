# Lecture 14: Useful Inequalities in Probability Theory

## 1 Probability inequalities

**The Gaussian Tail Inequality:** Let $X∼N(0,1)$. Then
$$
Pr(|X| > \epsilon) \leq \frac{\exp(-\epsilon ^2 / 2 )}{\epsilon}
$$

 **Markov’s inequality:** Let $X$ be a non-negative random variable and suppose $E(X)$ exists. For any $t >0$:
$$
Pr(X\geq t) \leq \frac{E[X]}{t}
$$
**Chebyshev’s inequality:** Let $μ=E(X)$ and $σ^2 = var(X)$. Then
$$
Pr(|X−μ|≥t)≤
\frac{σ^2}{t^2}
$$
and
$$
Pr(|Z|≥k)≤ \frac{1}{k^2} 
$$
where $Z= (X−μ)/σ$. In particular, $Pr(|Z|>2)≤ 1 /4$ and $Pr(|Z|>3)≤ 1 /9$.

### Hoeffding’s Inequality

- Hoeffding’s Inequality: Let $Y_{1} ,...,Y_{n}$be i.i.d. random variables such that $E(Y_{i}) =μ$and $a≤Y_{i}≤b$, where $a < 0 < b$. Then for any $\epsilon > 0$

$$
Pr(|\bar{Y}_{n}−μ|≥ \epsilon)≤ 2 exp\left\{ \frac{2n\epsilon^2}{(b-a)^2}\right\}
$$
where $\bar{Y}_{n} = (Y_{1}+\dots+Y_{n})/n$

## 2 Bounds on Expected Values

### Numerical Inequalities

The inequalities in this subsection, although often stated in terms of expectations, rely mainly on properties of numbers. In fact, they are all based on the following simple lemma.

**Lemma:** Let $a$ and $b$ be any positive numbers, and let $p$ and $q$ be any positive numbers (necessarily greater than 1) satisfying
$$
\begin{align}
&\frac{1}{p} + \frac{1}{q} = 1 \quad\quad\quad \text{ (1)} \\
&\frac{1}{p}a^p + \frac{1}{q}b^q\geq ab \quad (2)
\end{align}
$$

with equality if and only if $a^p=b^q$.

**Holder’s Inequality** Let $X$ and $Y$ be any two random variables, and let $p$ and $q$ satisfy (1). Then

$$
|EXY|≤E|XY|≤(E|X|^p)^{1/p}(E|Y|^q)^{1 /q} \quad\quad (3)
$$

**Cauchy-Schwartz Inequality:** If $X$ and $Y$ have finite variances then

$$
E|XY|≤ \sqrt{ E(X^2)E(Y^2) }
$$
### Jensen’s Inequality:

**Definition of convex & concave:** A function $g(x)$ is convex if $g(λx+ (1−λ)y)≤λg(x) + (1−λ)g(y)$ for all $x$ and $y$, and $0< λ <1$. The function $g(x)$ is concave if $−g(x)$ is convex.

Informally, we can think of convex functions as functions that “hold water” — that is, they are bowl-shaped ($g(x) =x^2$ is convex), while concave functions “spill water” ($g(x) = logx$ is concave). More formally, convex functions lie below lines connecting any two points. As $λ$ goes from $0$ to $1$, $λg(x_{1}) + (1−λ)g(x_{2})$ defines a line connecting $g(x_{1})$ and $g(x_{2})$. This line lies above $g(x)$ if $g(x)$ is convex. Furthermore, a convex function lies above all of its tangent lines , and that fact is the basis of Jensen’s Inequality.

If $g$ is convex, then
$$
E[{{{g(X)}}}]≥g(E(X))
$$

If $g$ is concave, then

$$
E[g(X)]≤g(E(X))
$$

