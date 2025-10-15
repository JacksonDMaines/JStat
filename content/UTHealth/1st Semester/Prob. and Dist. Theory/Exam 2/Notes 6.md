# Lecture 6: Moments of Discrete Distributions

## 1 Introduction to Moments

**Definition:** Moments are numerical measures that describe the shape and characteristics of a  
probability distribution.

The $k-th$ moment about the origin is defined as:
$$
\mu'_{k} = E[X^k] = \sum_{x}x^k\cdot P(X=x)
$$

Special Cases:

- $1st$ moment: $\mu'_{1} = E[X^1] = \mu = mean$
- $2nd$ moment: $\mu'_{2} = E[X^2]$

### Central Moments

The $k-th$ central moment is defined as:
$$
\mu_{k} = E[(x-\mu)^k], \text{ where } \mu = E[X]
$$

Special Cases:

- $1st$ central moment: $\mu_{1} = E[(X-\mu)^1] = E[X]- \mu = 0$
- $2nd$ central moment: $\mu_{2} = E[(X-\mu)^2] = Var(X)$

**Theorem:** Under some general conditions, the sequence of moments uniquely determines the  
distribution.

**Statement:** Let $X$ and $Y$ be two random variables. If their $i-th$ moments are equal for all  
$i∈{ 1 , 2 , 3 ,...}$, that is,
$$
\mu'_{ix} = \mu'_{iy}, \forall i\geq0
$$
then $X$ and $Y$ follow the same distribution

## 2 Recall Taylor Series Expansion

**General Taylor Series:**
$$
f(x) = f(x_{0}) + f'(x_{0})(x-x_{0}) + \frac{f''(x_{0})}{2!}(x-x_{0})^2 + \dots + \frac{f^{(n)}(x_{0})}{n!}(x-x_{0})^n + \dots
$$
**Maclaurin Series (when $X_{0} = 0$):**  
$$
f(x) = f(0) + f'(0)(x-0) + \frac{f''(0)}{2!}(x-0)^2 + \dots + \frac{f^{(n)}(0)}{n!}(x-0)^n + \dots
$$

## 3 Moment Generating Function (MGF)

**Definition:** If $X$ is a random variable, then the expected value:
$$
M_{X}(t) = E[e^{tx}]
$$

is called the **moment generating function (MGF)** of $X$, if this expected value exists for all  
values of $t$ in some interval: $−h < t < h$ for $h >0$.

Using the Taylor series expansion at zero of $e^{tx}$:

$$
\begin{align}
M_{X}(t) &= E[e^{tx}] = E\left[ 1 + \frac{tx}{1} + \frac{t^2x^2}{2!} + \frac{t^3x^3}{3!} \right]  \\
& = 1 +t\cdot E[x] + \frac{t^2}{2!}\cdot E[X^2] + \frac{t^3}{3!}\cdot E[X^3] + \dots \\
&= 1 + t\mu'_{1} + \frac{t^2}{2!}\mu'_{2} + \frac{t^3}{3!}\mu'_{3} + \dots
\end{align}
$$

### 3.1 MGF and Moments via Derivatives

**Result 1:** If $M_{X}(t) =M_{Y}(t)$ for all $t∈(−h,h)⊂\mathbb{R}$, then:
- $X$ and $Y$ follow same distribution

**Theorem:** If $M_{X}(t)$ exists, then for any integer $k≥1$,
$$
\frac{d^k}{dt^k} \left. M_{X}(t) \right|_{t=0} = E[X^k]= \mu'_{k} 
$$

**MGF Expansion and Derivatives:**
$$
M_{X}(t) = 1 + \mu'_{1} + \frac{t^2}{2!}\mu'_{2} + \frac{t^3}{3!}\mu'_{3} + \dots 
$$

**Taking derivatives:**
$$
\begin{align}
&M'_{X}(t) = 0 + \mu'_{1} + t\mu'_{2} + \frac{t^2}{3!}\mu'_{3} + \dots \\
 & M'_{X}(0) = 0 + \mu'_{1} + 0 + 0 + \dots  \\
 & M''_{X}(0) = 0 + 0+ \mu''_{2} + 0 + \dots  \\
&\vdots
\end{align}
$$

**General Rule:**
$$
E[X^k] = M_{X}^{(k)}(0) = \frac{d^k}{dk}=\left. M_{X}(t)\right|_{t=0}
$$

**Common Applications:**

- First moment (mean): $M'_{X}(0) = E[X] = \mu$
- Second moment: $M''_{X}(0) = E[X^2]$
- Variance: $Var(X) = M''_{X}(0) - (M'_{X}(0))^2 = E[X^2] - E[X]^2$

## 4 MGF of Common Discrete Distributions

### 4.1 Poisson Distribution

Let $X∼Poisson(λ)$, then $P(X=x) = \frac{\lambda^xe^{-\lambda}}{x!}$ for $x= 0, 1 , 2 ,...$

**Derivation of MGF:**
$$
\begin{align}
M_{X}(t) &= E[e^{tx}] = \sum_{x=0}^{\infty}e^{tx}\cdot P(X=x) = \sum_{x=0}^{\infty}e^{tx}\cdot \frac{\lambda^xe^{-\lambda}}{x!} \\
 & = e^{-\lambda}\sum_{x=0}^{\infty}\frac{(\lambda e^t)^x}{x!} = e^{-\lambda}\cdot e^{\lambda e^t} = e^{\lambda(e^t-1)}
\end{align}
$$

#### Computing Moments:

**First derivative:**
$$
M'_{X}(t) = e^{\lambda(e^t-1)}\cdot \lambda e^t
$$

**Second derivative:**
$$
M''_{X}(t) = e^{\lambda(e^t-1)}\cdot \lambda^2e^{2t} + \lambda e^t\cdot e^{\lambda(e^t-1)}
$$

Therefore:

- **Mean:** $E[X] =M'_{X}(t) = \lambda$
- **Variance:** $Var(X) =M''_{X}(t)-(M'_{X}(t))^2 = \lambda^2 + \lambda - \lambda^2=\lambda$ 

### 4.2 Bernoulli Distribution

Let $X∼Bernoulli(p)$, where $P(X= 0) = 1−p$ and $P(X= 1) =p$.

**MGF:**  
$$
MX(t) =E[e^{tX}] = \sum_{x}e^{tx}\cdot P(X=x) = e^{t\cdot 0 }(1-p) + e^{t\cdot 1}\cdot p = 1-p+e^tp
$$

Computing Moments:
- $M'_{X}(t) =pe^t⇒M'_{X}(0)=p = E[X]$
- $M''_{X}(t) =pe^t⇒M''_{X}(0)=p=E[X^2]$


**Variance:**  
$$Var(X) =M''_{X}(0)−(M'_{X}(0))^2 =p-p^2=p(1-p)$$

### 4.3 Binomial Distribution

Let $X∼Binomial(n,p)$. The PMF is $P(X=x) ={n \choose x}p^x(1−p)^{n−x}$ for $x= 0, 1 ,...,n$.

**Derivation of MGF:**
$$
\begin{align}
M_{X}(t) &= E[e^{tX}] = \sum_{x}e^{tx}\cdot P(X=x) = \sum_{x=0}^{\infty}e^{tx} \cdot {n \choose x}p^x(1−p)^{n−x}  \\
 & = \sum_{x=0}^{\infty} {n \choose x}(pe^t)^x(1−p)^{n−x}= (pe^t+1-p)^n
\end{align}
$$

#### Computing Moments:

**First derivative:**
$$
M'_{X}(t)= n(pe^t+1-p)^{n-1}\cdot pe^t
$$

**Second derivative:**
$$
M''_{X}(t) = n(n-1)(pe^t+1-p)^{n-2}\cdot (pe^t)^2 + pe^t\cdot n(pe^t+1-p)^{n-1}
$$

Therefore:

- **Mean:** $E[X] =np$
- **Variance:** $Var(X) =M''_{X}(0)−(M'_{X}(0))^2 = n(n-1)p^2+np-(np)^2=np(1-p)$ 

### 4.4 Geometric Distribution

Let $X∼Geometric(p)$, with PMF:


$$P(X=x) =q^{x−1} p, \space x= 1, 2 , 3 ,..., where\space q= 1−p$$


**Derivation of MGF:**
$$
\begin{align}
M_{X}(t) &= E[e^{tX}] = \sum e^{tx}\cdot P(X=x) = \sum_{x=1}^{\infty} e^{tx}\cdot (q)^{t-1}p \\
 & = \frac{p}{q}\cdot \sum_{x=1}^{\infty}e^{tx}\cdot q^x = \frac{p}{q}\cdot \sum_{x=1}^{\infty}(e^{t}\cdot q)^x = \frac{p}{q} \cdot qe^t\cdot \sum_{x=0}^{\infty}(e^{t}\cdot q)^x  \\
& = pe^t \cdot \frac{1}{1-qe^t} = \frac{pe^t}{1-qe^t} \text{ for } t<-\ln(1-p)
\end{align}
$$

**Computing the Mean:**
$$
M'_{X}(t) = \frac{pe^t}{(1-qe^t)^2}
$$

**Mean from MGF:**  
$μ=E[X] =M'_{X}(0) = \frac{1}{p}$

## 5 Properties of the MGF

**Theorem:** MGF of Linear Transformation

Let $Y=aX+b$. Then:  
$$
M_{Y}(t) =e^{tb}·M_{X}(at)
$$

**Proof:**  
$$
M_{Y}(t) =E[e^{tY}] =E[e^{t(aX+b)}] = E[e^{atX+tb}] = E[e^{atX}e^{tb}]= e^{tb}E[e^{atX}] =e^{tb}\cdot M_{X}(at)
$$


## 6 Chebyshev’s Theorem

**Theorem:** For any random variable $Y$ with finite mean $μ$ and variance $σ^2$ , for any $k >0$,
$$
P(|Y-\mu|\geq k\sigma) \leq \frac{1}{k^2}
$$

Equivalently:
$$
P(|Y-\mu|< k\sigma) \geq 1- \frac{1}{k^2}
$$

Use case: This theorem is useful when $k$ and $\sigma$^2 are known, but not the exact distribution.

Note: Chebyshev’s inequality is mostly useful when $k$ is large (typically $k\geq 2$.

### 6.1 Proof of Chebyshev’s Theorem

**Goal:** Prove that $P(|Y−μ|≥kσ)≤ \frac{1}{k^2}$.

**Proof:**
$$
\begin{align}
\sigma^2 &= E[(Y-\mu)^2] = \sum_{Y}(y-\mu)^2\cdot P(Y) \\
&= \sum_{|Y-\mu|\geq k \sigma} (y-\mu)^2\cdot P(Y) + \sum_{|Y-\mu|< k \sigma} (y-\mu)^2\cdot P(Y)  \\
&\geq \sum_{|Y-\mu|\geq k \sigma} (y-\mu)^2\cdot P(Y) \geq \sum_{|Y-\mu|\geq k \sigma} (k\sigma)^2\cdot P(Y) = k^2\sigma^2 \sum_{|Y-\mu|\geq k \sigma} P(Y) \\
& = k^2\sigma^2\cdot P(|Y-\mu|\geq k\sigma) \\
 \\
&\implies \sigma^2 \geq k^2\sigma^2\cdot P(|Y-\mu|\geq k\sigma) \\
& \implies 1 \geq k^2\cdot P(|Y-\mu|\geq k\sigma) \\
& \implies \frac{1}{k^2} \geq  P(|Y-\mu|\geq k\sigma)
\end{align}

$$
### 6.2 General Inequality for Functions

A more general form (Markov’s inequality):

If $X$ is a random variable and $h(X)≥0$, then for any $c >0$,
$$
P(h(x)\geq c) \leq \frac{E[h(x)]}{c}
$$

Chebyshev’s theorem is a special case where $h(x) = (x-\mu)^2$ and $c=k^2\sigma^2$.

### 6.3 Applications of Chebyshev’s Theorem

Example 1:Let $Y$ be a random variable with $μ= 100$ and $\sigma^2=100$ (so $\sigma=10$). Find values $a$  
and $b$ such that $P(a≤Y ≤b)≥ \frac{5}{9}$.

Using Chebyshev’s inequality:  
$$
P(|Y−μ|< kσ)≥ 1 − \frac{1}{k^2}
$$

Let $\frac{5}{9} = 1- \frac{1}{k^2} \implies k=\frac{3}{2}$ and $P(\mu-k\sigma < Y<\mu + k\sigma)$ therefore, 
- $a=\mu-k\sigma \implies a = 100 -\frac{3}{2}(10) = 85$
- $b =\mu+k\sigma \implies b = 100 + \frac{3}{2}(10) = 115$

