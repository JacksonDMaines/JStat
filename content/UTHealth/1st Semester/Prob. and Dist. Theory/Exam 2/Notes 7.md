# Lecture 7: Transition to Continuous Distributions

## 1 Continuous Random Variable

### 1.1 Definition

- Like discrete random variables, continuous random variables are numerical functions of the outcomes of a probability experiment.
- Discrete random variables have supports with **finite** or **countable infinite** number of values, but the support of a continuous random variable has an **uncountably infinite** number of numbers.
- Typically this means that the support of a continuous random variable is composed of **intervals** of real numbers.
- The probability distribution for a discrete random variable can always be given by assigning a non-negative probability to each of the possible values. Unfortunately, the probability distribution for a continuous random variable cannot be specified in the same way. It is mathematically impossible to assign non-zero probabilities to all the points on a line interval while satisfying the requirement that the probabilities of the distinct possible values sum to


- Instead we will develop a different method to describe the probability distribution for a  continuous random variable.
- We will look at the probability that the random variable is in a range of values. Specifically  we will look at $P(X≤x)$.
- We would still like a function like the probability mass function of the discrete random  variable to help us characterize the distribution of a continuous random variable. So, for  continuous random variables we introduce the Probability Density Functions:

### 1.2 Recall: CDF

- Let $x$ denote any random variable. The density function of $x$ denoted by $F(x)$ is given by  
    $F(x) =P(X≤x)$ for any $−∞< x <∞$(c.d.f.)
- If $x$ is discrete, $F(x) =∑_{t≤x}P(t)$
- If $F(x)$ is a c.d.f., then
    1. $F(−∞) =\lim_{ x \to -\infty }F(x) = 0$
    2. $F(+∞) =\lim_{ x \to \infty }F(x)=1$
    3. $F(x)$ is a non-decreasing function of $x$. $F$ is right continuous.
$$
\lim_{ t \to x^+ }F(t) = F(x) \Leftrightarrow \lim_{ h \to 0^+ } F(x+h) = F(x) 
$$
- When $x$ is discrete, c.d.f $F$ is a step function with countable number of discontinuities.
- If $x$ only takes integers, $P(X) = F(X)-F(x-1)$ or $P(a<x\leq b) = P(X\leq b )- P(X\leq a) = F(b) - F(a)$ 
	- **Note:** dont want $x$ to take $a$ thats why no equality  
### 1.3 Probability Density Function

Definition: The probability density function (PDF or p.d.f. for short) of a continuous random  
variable $X$ with CDF $F_{X}$ is defined to be the function $f_{X}$ such that
$$
f_{X}(x) = \frac{d}{dx}F(x) = F'_{X}(x)
$$
or
$$
F_{X}(x) = \int_{-\infty}^{x}f_{X}(t)dt
$$

Remarks:

1. c.d.f. is continuous (not just right continuous). Thus, when $y$ is a continuous r.v.
$P(X=x)=F(x)-\lim_{ t \to x_{-} }F(t) = F(x)-F(x) = 0$
2. Fundamental calculus tells us $F$ is differentiable (except perhaps at countable # points)  
    $F′(x) =f(x)$.
3. $f(x)≥0,∀x$, and $\int_{-\infty}^{\infty}f(x)=1$
4. The p.d.f. $f$ does not represent a probability. In fact, $f(x)$ could be $>1$ for some $x$.
5. $P(a<x<b) = P(a\leq x<b)= P(a<x\leq b) = P(a\leq x\leq b)= \int_{a}^{b}f(x)dx = F(b)-F(a)$


### 1.4 Quantile

- Suppose We have a Random Variable $X$ (discrete or continuous). Sometimes we will want  
    to find the value $y$ such that $P(X≤y) =p$, where $p$ is a value between $0$ and $1$.  
    - This question is asking for a quantile of the distribution of $X$. Formally, we define a  
    quantile as follows:  
    Definition Let $X$ be a random variable with CDF $F_{X}(x)$ and let $p$ be a value between  
    $0$ and $1$. The $p^{th}$ quantile of the distribution of $X$, $\phi_{p}$is the smallest value such that $P(X\leq \phi_{p}) = F_{X}(\phi_{p})\geq p$
    - Sometimes the $p^{th}$ quantile is also referred to as the percentile $(100\cdot p)^{th}$.  
    - Note that, because continuous random variables have continuous CDFs, the $p^{th}$ quantile  
    ($\phi_{p}$) of a continuous random variable will be the smallest value such that $P(X\leq \phi_{p})=F_{X}(\phi_{p})=p$

### 1.5 Expectation of a Continuous Random Variable

- For continuous random variables, we also have expectation, but we define it differently.

**Definition:** $x$ is a continuous r.v. with p.d.f. $f(x)$.
$$
E[X]=\int_{x}x\cdot f(x)dx\text{, if }  \int_{x}|x|\cdot f(x)dx<\infty
$$
**Theorem:**  
1) $g$ is a function of r.v. $x$.
$$
E[g(x)] = \int_{x}g(x)\cdot f(x)dx
$$
2) $E(c) =c$
**Proof:**
$$
E[c] = \int_{-\infty}^{\infty}c \cdot f(x)dx = c\int_{-\infty}^{\infty}f(x)dx = c\cdot (1)= c, \text{ by def. of PDF}
$$


3) $E[∑_{i=1}^{n}=c_{i}g_{i}(x)] =∑_{i=1}^{n}c_{i}E[g_{i}(x)]$
**Proof:**
$$
E[∑_{i=1}^{n}=c_{i}g_{i}(x)] = \int_{-\infty}^{\infty}\sum_{i=1}^{n}c_{i}g_{i}(x)\cdot f(x)dx = \sum_{i=1}^{n}c_{i}\int_{-\infty}^{\infty}g_{i}(x)\cdot f(x)dx = ∑_{i=1}^{n}c_{i}E[g_{i}(x)]
$$

4) Variance:
**Proof:**
$$
Var(X) = E[X^2]-E[X]^2 = \int_{x}x^2\cdot f(x)dx - \left( \int_{x}x\cdot f(x)dx \right)^2
$$
## 2 Moment Generating Function of a Continuous RV

- Recall the Taylor expansion of $e^{tX}$
$$
e^{tX} = \sum_{i=0}^{\infty} \frac{(tX)^i}{i!}
$$
- Taking the expectation on both sides of this equation:
$$
E[e^{tX}] = E\left[ \sum_{i=0}^{\infty}\frac{(tx)^i}{i!} \right] = \sum_{i=0}^{\infty}\frac{t^i}{i!}E[X^i]
$$
- The moment generating function is a sum of terms involving all of the moments of $X$.
- This means that if we differentiate the MGF with respect to $t$ and then set $t$ to zero, we will be left with just a moment of $X$.

$$
\begin{align} 
&E[e^{tX}] = 1+ tE[X] +\frac{t^2}{2}E[X^2] \dots,  \\
&\frac{d}{dt}E[e^{tX}] = E[X] + tE[X^2] + \frac{t^2}{2!}E[X^3] + \dots,  \\
& \left.\frac{d}{dt}E[e^{tX}]\right|_{t=0} = E[X]
\end{align}  
$$


- If we were to take further derivatives, we would be able to get higher order moments.

**Theorem:** Let $X$ be a random variable with support $S$, PDF $p_{X}(x)$ and MGF $M_{X}(t)$. Then
$$
E[X^k] = \left[ \frac{d}{dt}M_{X}(t) \right]_{t=0}
$$
**Definition:** Let $k$ be a non-negative integer, and let $X$ be a continuous random variable with  PDF $f_{X}(x)$. Then if that moment exists, the $kth$ moment of $X$ is:
$$
E[X^k]=\int_{-\infty}^{\infty}x^k\cdot f_{X}(x)dx
$$
**Definition:** The Moment Generating Function(or just MGF for short) of a continuous  
random variable $X$ with PDF $f_{X}(x)$ is defined to be:
$$
M_{X}(t) = E[e^{tX}] = \int_{-\infty}^{\infty}e^{tx}\cdot f_{X}(x)dx
$$
where there exists $a,b >0$ such that $M_{X}(t)<∞$ for $|t|< b$.

- Not surprisingly, the definition of of the moment generating function for continuous random variables is also similar to that of discrete random variable distributions.
- and this moment generating function has the exact same properties that the moment generating function of discrete random variables do, namely

**Theorem:** Let $X$ be a continuous random variable with PDF $f_{X}(x)$ and MGF $M_{X}(t)$. Then
$$
E[X^k] = \left. \frac{d^k}{dt^k}M_{X}(t)\right|_{t=0}
$$