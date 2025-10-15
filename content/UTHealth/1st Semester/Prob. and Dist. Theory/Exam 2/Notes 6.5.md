# Additional Properties of MGF

## 1 MGF of independent RV’s

If $X,Y$ are **independent** and $M_{X}(·),M_{Y}(·)$ **exist** , then $M_{X+Y}(·)$ exists and is given by
$$
M_{X+Y}(t) = M_{X}(t) + M_{Y}(t)
$$
**General Version**

If $X_{1},X_{2} ,...,X_{n}$ are independent rv’s, then
$$
M_{\sum_{i}x_{i}}(t) = \prod_{i}M_{X_{i}}(t)
$$

If $X,Y,Z$ are mutually independent rv’s:

- $E(X+Y+Z) =E[X] + E[Y] + E[Z]$
- $E(XY Z) =E[X]E[Y]E[Z]$ ,whenever $E[X],E[Y],E[Z]$ are finite.
- $V ar(X+Y+Z) =Var(X) + Var(Y) + Var(Z)$
- $M_{X+Y+Z}(t) =M_{X}(t)M_{y}(t)M_{Z}(t)$
- $g(X),h(Y),k(Z)$ are mutually independent rv’s for any functions $g,h,k$, and therefore:
$$
E[g(X)h(Y)k(Z)] = E[g(X)]E[h(Y)]E[k(Z)]
$$

whenever $E\{g(X)\},E\{h(Y)\},E\{k(Z)\}$ are finite


If $X_{1},X_{2} ,...,X_{n}$ are $i.i.d.$(**independent and identically distributed**), if they are mutually independent and have the same distribution, then

- $E\left( \sum_{i=1}^{n}X_{i} \right) =\sum_{i}E[X_{i}] = n \cdot E[X_{1}]$
- $V ar\left( \sum_{i=1}^{n}X_{i} \right) =\sum_{i}Var(X_{i}) = n\cdot Var(X_{1})$
- $M_{\sum_{i=1}^{n}X_{i}}(t) =\prod_{i}M_{X_{i}}(t) = \left( M_{x_{1}}(t)\right)^n$

## 2 Closure Properties for Binomial and Negative Binomial

Suppose $X_{1},X_{2}$ are independent.

1. If $X_{1} ∼Binomial(n 1 ,p)$ and $X_{2} ∼Binomial(n 2 ,p)$, then:
$$
X_{1}+X_{2} \sim Bin(n_{1}+n_{2}, p)
$$

**Proof:** If $X_{1}$ and $X_{2}$ are independent. Then:
$$
\begin{align}
M_{X_{1}+X_{2}}(t) &= M_{X_{1}}(t)M_{X_{2}}(t) = (1-p+pe^t)^{n_{1}}(1-p+pe^t)^{n_{2}} \\
& = (1-p+pe^t)^{n_{1}+n_{2}} \\
 \\
&\text{ this is MGF of binomial}(n_{1}+n_{2}, p) \\
 \\
&\implies X_{1}+X_{2} \sim Bin(n_{1}+n_{2}, p)
\end{align}

$$


2. If $X_{1} ∼NB(r_{1} ,p)$ and $X_{2} ∼NB(r_{2} ,p)$,then:

**Proof:**
$$
\begin{align}
M_{X_{1}+X_{2}}(t) &= M_{X_{1}}(t)M_{X_{2}}(t) = \left( \left( \frac{e^t}{1-(1-p)e^t} \right)^{r_{1}}\left( \frac{e^t}{1-(1-p)e^t} \right)^{r_{2}} \right) \\
& = \left( \frac{e^t}{1-(1-p)e^t} \right)^{r_{1}+r_{2}} \\
 \\
& \text{ this is MGF of Negatvie Binomial}(r_{1}+r_{2}, p) \\
&\implies X_{1} +X_{2} ∼Neg.Bin(r 1 +r 2 ,p)
\end{align}
$$


## 3 Closure Property of Poisson

If$X_{1} ∼Poisson(λ_{1})$, $X_{1} ∼Poisson(λ_{1})$, and $X_{1}$ and $X_{2}$ are independent, then:
$$
X_{1}+X_{2} \sim Pois(\lambda_{1}+\lambda_{2})
$$
**Proof:**
$$
\begin{align}
M_{X_{1}+X_{2}}(t) &= M_{X_{1}}(t)M_{X_{2}}(t) = (e^{\lambda_{1}(e^t-1)})(e^{\lambda_{2}(e^t-1)}) = e^{(\lambda_{1}+\lambda_{2})(e^t-1)} \\
 \\
& \text{ this is MGF of poisson}(\lambda_{1}+\lambda_{2}) \\
&\implies X_{1}+X_{2} \sim Pois(\lambda_{1}+\lambda_{2})
\end{align}
$$

## 4 The Poisson Process

A process of arrivals (clicks, events, etc.) is called a Poisson process with constant rate $λ$ if

1. The number of arrivals in any given fixed period of time of duration $t$ has a $Poisson(λt)$  
    distribution.
2. Disjoint intervals of time are independent.

Consequence of (1): The expected number of arrivals in a period of length $t$ is $λt$. The arrivals  
occur at rate $λ$ (on average).

**Examples:**
- Clicks on a Geiger counter (under uniform conditions).
- Number of patients arriving at a hospital.
- Accidents on a highway (under uniform conditions).

Remember Koshevnik! 