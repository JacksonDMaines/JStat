# Lecture 5: Common Discrete Distributions

## 1 Bernoulli Distribution

**Definition:** A Bernoulli distribution models a single experiment with only two outcomes: success  
(1) and failure (0). E.g. Tossing a coin, success with probability $p$.

Notation:  
$$
X∼Ber(p)
$$

**PMF:**
$$
P(X) = \begin{cases}
p & \text{if x = 1} \\
1-p & \text{if x = 0}
\end{cases}
$$
**Proof:**
$$
\sum_{x=0}^{1}P(X=x) = 1
$$
$$
\sum_{x=0}^{1}P(X=x)=(1-p)+p = 1
$$
**Expectation:**
$$
E[X]=\sum_{x=0}^{1}x\cdot P(X=x) = 0+1\cdot (p) = p
$$
when $X\sim Bern(p)$

**Variance:**
$$
E[X^2] = \sum_{x=0}^{1}x^2 \cdot P(X=x) = 0 +(1^2)\cdot p = p
$$
then
$$
Var[X] = E[X^2]-(E[X])^2 =  p - (p)^2 = p\cdot(1-p)
$$
again when $X\sim Bern(p)$
## 2 Binomial Distribution

Definition: Repeat Bernoulli trials $n$ times, each with the success probability $p$, record the # of  
success.

**Notation:**
$$
X∼Bin(n,p)
$$

**PMF:**
$$
P(X=k) = {n \choose k}\cdot p^k \cdot(1-p)^{n-k}
$$
for $k = 0, 1, 2, 3,\dots$

**Example:** Rolling a die $n$ times, use $X$ to denote the # of 3’s.
$$
X\sim Bin\left( n, \frac{1}{6} \right)
$$


### 2.1 Binomial Expansion Formula

Binomial Theorem

For any real numbers $a,b$, and integer $n≥0$, we have:
$$
(a+b)^n = \sum_{k=0}^{n} {n \choose k}a^{n-k}b^k
$$


- ${n \choose k} = \frac{n!}{k!(n-k)!}$: Binomial coefficient
- The sum runs over $k= 0, 1 , 2 ,...,n$
- Each term is: ${n \choose k}a^{n-k}b^k$

**Example:** $(x+y)^3$ 
$$
= \sum_{k=0}^{3}{3 \choose k}\cdot x^{3-k}\cdot y^k = {3 \choose 0}x^3 + {3 \choose 1}x^2\cdot y + {3 \choose 2}x \cdot y^2 + {3 \choose 3}y^3 = x^3+3x^2y+3xy^2+y^3
$$

### 2.2 Binomial Distribution- Properties

**Proof:**  
$$
\sum _{k=0}^{n}P(X=k)=1
$$
$$
\sum_{k=0}^{n}P(X=k) = \sum_{k=0}^{n} {n \choose k}p^k(1-p)^{n-k} = [p+(1-p)]^n = 1
$$
using binomial theorem.

**Expectation- Method 1**
$$
\begin{align}
E[X] &= \sum_{k=0}^{n}k \cdot P(X=k) = \sum_{k=0}^n k \cdot {n \choose k}p^k(1-p)^{n-k} = \sum_{k=1}^n k \cdot {n \choose k}p^k(1-p)^{n-k} \\
&\text{Note: } k\cdot{n \choose k } = k \cdot \frac{n!}{k!(n-k)!} = \frac{n!}{(k-1)!(n-k)!} = \frac{n\cdot (n-1)!}{(k-1)!(n-k)!} = n \cdot {n-1 \choose k-1} \\
 \\
&= \sum_{k=1}^{n} n \cdot {n-1 \choose k-1}p^k(1-p)^{n-k} = np \cdot \sum_{k=1}^{n} {n-1 \choose k-1}p^{k-1}(1-p)^{n-k} \space \text{  let j = k-1}\\
& =np \cdot \sum_{j=0}^{n-1} {n - 1 \choose j}p^j(1-p)^{(n-1)-j} = np \cdot(p+(1-p))^{n-1} = np
\end{align}
$$


**Expectation - Method 2**
$$
\begin{align}
&X = X_{1}+X_{2}+\dots+X_{n} \text{ where }X_{i}\sim Bern(p) \\
&E{[X]} = E[X_{1}]+E[X_{2}] + \dots + E[X_{n}] = p + p + \dots +p = np 
\end{align}
$$
**Variance:**
$$
\begin{align}
Var[X] &= Var[X_{1}+X_{2}+\dots+X_{n}] =  \\
&= Var[X_{1}] + Var[X_{2}] + \dots Var[X_{n}]  \\
&= p(1-p) + p(1-p) + \dots + p(1-p)  \\
&= np(1-p)
\end{align}
$$

