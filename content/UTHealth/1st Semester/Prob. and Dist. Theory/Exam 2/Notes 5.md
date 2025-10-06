## 3 Geometric Distribution

**Definition:** Number of trials until the first success.

**Notation:** $X∼GEO(p)$

**PMF:**
$$
P(X=k) = (1-p)^{k-1}p
$$
for $k = 1,2,3, \dots$

**Example:** Rolling a die until the first “5” appears.
$$
\begin{align}
&P(X=k) = \left( \frac{5}{6} \right)^{k-1}\left( \frac{1}{6} \right) \text{ for k} \in\mathbb{N} \\
 \\
&P(X=4) = \left( \frac{5}{6} \right)^{4-1}\left( \frac{1}{6} \right) \approx .0965 \\
 \\
&P(X>3) = 1-P(X\leq 3) = 1-[P(X=1)+P(X=2)+P(X=3)] \approx .5787
\end{align}
$$

$$
\begin{align}
 & P(\text{1st 5 on even roll}) = P[X=2] + P[X=4] + \dots \\
 & = \left( \frac{5}{6} \right)\left( \frac{1}{6} \right) + \left( \frac{5}{6} \right)^3\left( \frac{1}{6}  \right)+ \dots \\
&= \left( \frac{5}{6} \right)\left( \frac{1}{6} \right)\left(1 + \left( \frac{5}{6} \right)^2+ \dots\right) \\
&Note: S = \sum_{j=0}^{n}q^j = 1+q+q^2 + \dots \\
&qS = q + q^2 + q^3 + \dots \implies S-qS = 1 \implies S = \frac{1}{1-q} \text{ for } 0<q<1 \\
& = \left( \frac{5}{6} \right)\left( \frac{1}{6} \right)\left[ \sum_{j=0}^{n}\left( \frac{5}{6} \right)^{2j} \right] = \left( \frac{5}{6} \right)\left( \frac{1}{6} \right)\left[ \sum_{j=0}^{n}\left( \left( \frac{5}{6} \right)^2 \right)^{j} \right] \\
 & \left( \frac{5}{6} \right)\left( \frac{1}{6} \right)\left( \frac{1}{1-\left( \frac{5}{6} \right)^2} \right) = \frac{5}{11}
\end{align}
$$

**Example:** 15% of job applicants have advanced training. Find the probability the first applicant  
with advanced training is found on the 8th interview.
$$
\begin{align}
&P(X=8) = (1-.15)^7(.15) \\
 \\
 &P(X>6) = P(X = 7) + P(X=8) + \dots \\
&= (.85)^6(.15) + (.85)^7(.15) + \dots \\
&  = (.85)^6(.15)\left(1 + (.85)^1 + \dots\right) \\
& =  (.85)^6(.15)\left( \frac{1}{1-.85} \right) = .85^6
\end{align}

$$

**Conditional Probability:** 
$$
P(X=8|X>6) = \frac{P(X=8 \cap X>6)}{P(X>6)} = \frac{P(X=8)}{P(X>6)} = P(X=2)

$$
### 3.1 Memoryless Property

Let $X$ be a geometric random variable representing the number of trials until the first success.

**Memoryless Property:**

For any integers $m$, $n≥1$,
$$
P(X=m+n|X>n)=P(X=m)
$$

Interpretation:

- The probability of needing more than $m+n$ trials, given that more than $m$ trials have already failed, is the same as starting fresh.
- “ The process forgets the past.”
- No matter how long we’ve already waited, the chance of waiting $n$ more trials is unaffected.

### 3.2 Geometric Distribution - Properties

**Proof:**
$$
\sum_{k=1}^{\infty}P(X=k)=1
$$

$$
\begin{align}
\sum_{k=1}^{\infty} P(X=k) = \sum_{k=1}^{\infty} (1-p)^{k-1}\cdot p = p\cdot \sum_{k=1}^{\infty}(1-p)^{k-1} = p\left[ \sum_{k=0}^{\infty}(1-p)^k \right] \\
p\cdot\left( \frac{1}{1-(1-p)} \right) = p\cdot\left( \frac{1}{p} \right) 
\end{align}
$$
**Expectation:** 
$$
\begin{align}
E[X] &= \sum_{k=1}^{\infty}k\cdot P(X=k) = \sum_{k=1}^{\infty}k\cdot(1-p)^{k-1}\cdot p = p\sum_{k=1}^{\infty}k\cdot q^k-1 \text{ where }q = 1-p \\
& = p\cdot \sum_{k=1}^{\infty} \frac{d}{dq}q^k = p \cdot \frac{d}{dq}\cdot \sum_{k=1}^{\infty} q^k = p\cdot \frac{d}{dq}\left[ \sum_{k=0}^{\infty}q^k -1 \right] = p \cdot \frac{d}{dq}\left[ \frac{1}{1-q}-1 \right] \\
& =p\cdot \frac{d}{dp}\left[ \frac{1-(1-q)}{1-q} \right] = p \cdot \frac{d}{dp}\left[ \frac{q}{1-q} \right] = p \cdot \frac{1}{(1-q)^2} = p\cdot \frac{1}{p^2} = \frac{1}{p}
\end{align}
$$
**Variance:** No proof in class
$$
Var[X] = \frac{1-p}{p^2}
$$
**Additional Properties:**

- Lack of memory: $P(X > s+t|X > s) =P(X > t)$
- Monotonicity: As $x↑,P(X=x)↓$

## 4 Hypergeometric Distribution

**Definition:** Sampling $n$ objects (without replacement) from a finite population of size $N$, which  
contains $K$ elements of type 1 (successes) and $N−K$ elements of type 2 (failures).

Let $X$ be the number of type 1 elements (successes) in the sample.

$Notation:$ $X∼Hyp(N,K,n)$

$PMF:$
$$
P(X=x) = \frac{{K \choose x}{N-k \choose n-x}}{{N \choose n}} \text{ , } max(0,n+K-N)\leq x\leq min(K,n)
$$

### 4.1 Hypergeometric Distribution - Properties

Proof: $\sum_{k}P(X=k)=1$
$$
\begin{align}
\sum_{k}P(X=k) &= \sum_{k}\frac{{K\choose k}{N-k \choose n-k}}{{N \choose n}} \\
& \frac{1}{{N \choose n}} \cdot \sum_{k}{K \choose k}{N-K \choose n-k}
\end{align}
$$

Now we need to show that $\sum_{k}{K \choose k}{N-K \choose n-k}={N \choose n}$.
- Logic follows, multiple all ways to choose $k$ successes and all ways to choose $n-k$ fails then sum for all $k$  

Let’s think about this combinatorically. The left side counts the number of ways to:

- Choose $k$ items from $K$ success items:$K\choose k$ways
- Choose $n−k$ items from $N−K$ failure items:${N-K \choose n-k}$ ways
- Sum over all possible values of $k$

Therefore:  
$$
\sum_{k}P(X=k)=\frac{1}{{N \choose n}}\cdot {N \choose n} = 1
$$

**Expectation:**
$$
\begin{align}
E[X] &= \sum_{x=0}^{n}x\cdot \frac{{K\choose x}{N-k \choose n-x}}{{N \choose n}} = \sum_{x=1}^{n}x\cdot \frac{{K\choose x}{N-k \choose n-x}}{{N \choose n}}  \\ \\

&Note: x\cdot {K \choose x} = K \cdot {K-1 \choose x-1} \text{ and } {N \choose n} = \frac{N}{n}{N-1 \choose n-1} \\
 \\
&= \sum_{x=1}^{n}\frac{k\cdot {K-1\choose x-1}{N-k \choose n-x}}{\frac{N}{n}\cdot{N-1 \choose n-1}} = \sum_{x=1}^{n} \frac{nk}{N}\cdot \frac{ {K-1\choose x-1}{N-k \choose n-x}}{{N-1 \choose n-1}}  \\
 \\
& Note: \frac{ {K-1\choose x-1}{N-k \choose n-x}}{{N-1 \choose n-1}} \sim Hyp(N-1, K-1, n-1)  \\
&\text{and } \sum P(X=k) = 1, \text{ so } \\
 \\
 \\
&=\frac{nk}{N}(1) = \frac{nk}{N}
\end{align}

$$

**Variance:** No proof in class
$$
Var[X] = n \cdot \frac{k}{N} \cdot\left( 1-\frac{k}{N} \right) \cdot\frac{N-n}{n-1}
$$

**Theorem:** The value of $N$ that maximizes $P(X=x)$ (as a function of $N$) occurs approximately  
at:  $\hat{N} = \frac{nK}{x}$

**Proof Outline:**  
$$
P(X=k)=\frac{{K \choose k}{N-K \choose n-k}}{{N \choose n}}
$$

$$
\text{if you can prove F(N)=P(X=k) is increasing when } N< \frac{nk}{x} \text{ and decreasing when } N > \frac{nk}{x} 
$$
$$
\begin{align}
\text{Consider:} &\frac{P\left( x=\frac{k}{n} \right)}{P\left( x= \frac{k}{N-1} \right)} = \frac{\frac{{K \choose k}{N-k \choose n-k}}{{N \choose n}}}{\frac{{K \choose k}{N-1k \choose n-k}}{{N-1 \choose n}}} \\
& = \frac{(N-K)(N-n)}{N(N-K-n+K)}>1  \\
&\implies (N - K)(N-n) > N(N-K-n+K) \\
&\implies N^2-Nn-Nk+nK>N^2-NK-Nn+Nk \\
&\implies Kn>Nk \implies N< \frac{nK}{k} \\
&\text{ so } N= \frac{nK}{x} \text{ maximizes P(X=x)}
\end{align}
$$

### 4.2 Approximation

Recall  
$$
E[X] = n \cdot \frac{K}{N}, \space Var[X] = n \cdot \frac{K}{N}\cdot\left( 1- \frac{K}{N} \right)\cdot \frac{N-n}{N-1}
$$

For large $N$ and small $n$: $E[X]\approx np$ and $Var[X] \approx np(1-p)$ when $N$ is very large, $\frac{k}{N}=p$

Thus, the hypergeometric distribution can be approximated by a binomial distribution when  
sampling fraction $\frac{N}{n}$ is small.

Example: Suppose $K= 4$ animals are tagged and released. A sample of $n= 3$ animals is taken  
at random. Let $X$ be the number of tagged animals observed in the sample. Find $P(X= 1)$ as a  
function of $N$ and find the value of $N$ that maximizes it.
$$
P(X=1) = \frac{{4 \choose 1}{N-4 \choose 2}}{{N \choose 3}} = \frac{4 \cdot {N-4 \choose 2)}}{N\choose 3}
$$
maximized when
$$
\hat{N} = \frac{nK}{x} = \frac{3\cdot 4}{1} = 12
$$
best estimate of population size is $N=12$

## 5 Poisson Distribution

Suppose $3,000$ people are watching a parade on a very hot day. The probability that any one  
person suffers heat exhaustion is $p= 0.005$.

Let $X=$ number of people who suffer heat exhaustion. Then $X∼Bin(3000, 0 .005)$.

**Question:** What is the probability that $18$ people suffer heat exhaustion?
$$
P(Y=18) = {3000 \choose 18}(.005)^{18}(1-.005)^{2982}
$$

But as $n→ ∞,p→0$, such that $np=λ$ remains constant, we approximate the binomial using  
the Poisson distribution.

**Definition:** Models the number of events in a fixed interval of time/space with a constant rate.

**PMF:**
$$
P(X=k)=\frac{\lambda^ke^{-\lambda}}{k!}, \space k = 0,1,2,3 \dots 
$$


### 5.1 Poisson Distribution - Properties

**Proof:** $\sum_{k=0}^{\infty} P(X=k)=1$
$$
\begin{align}
&\sum_{k=0}^{\infty}\frac{\lambda^k\cdot e^{-\lambda}}{k!} = e^{-\lambda}\sum_{k=0}^{\infty}\frac{\lambda^k}{k!} \\ \\

& Note: \sum_{k=0}^{\infty} \frac{\lambda^k}{k!} = e^\lambda \\
 \\
&= e^{-\lambda}\cdot e^\lambda = 1
\end{align}
$$
**Expectation:**
$$
\begin{align}
E[X]&= \sum k \cdot P(X=k) = \sum_{k=0}^{\infty}k \cdot \frac{\lambda^k\cdot e^{-\lambda}}{k!}  \\
& = e^{-\lambda}\sum_{k=1}^{\infty} \frac{\lambda^k}{(k-1)!} = e^{-\lambda}\cdot \lambda \sum_{k=1}^{\infty} \frac{\lambda^{k-1}}{(k-1)!}  \\
& = e^{-\lambda} \cdot \lambda \cdot e^{\lambda} = \lambda  
\end{align}
$$

**Variance:**
$$
E[X^2] = \lambda^2 + \lambda 
$$
$$
Var[X] = \lambda 
$$



## 6 Negative Binomial Distribution

- The Binomial distribution counts successes in a fixed number of trials.
- The Negative Binomial distribution counts the number of trials needed to achieve a fixed  
    number of successes.
- Arises naturally when:
    - We perform independent $Bernoulli(p)$ trials
    - And stop when we reach the $r-th$ success

**Definition #1:**
$$
P(X=x|r,p) = {x-1 \choose r-1} p^r (1-p)^{x-r} \text{ for x = r, r+1, . . .}
$$

Let $X$ be the trial on which the $r-th$ success occurs in a sequence of $Bernoulli(p)$ trials.

Then $X$ has a Negative Binomial distribution:

- : $r$ number of successes
- : $x$ trial of $r-th$ success
- : $p$ probability of success on each trial

**Definition #2:**

Alternatively, define $Y=X−r$, the number of failures before the $r-th$ success.
$$
P(Y=y) = {r+y-1\choose y} p^r(1-p^y), \space y = 0,1,2, \dots
$$
- Random variable $Y$ counts failures instead of trial number

### 6.1 Negative Binomial Distribution - Properties

**Expectation:**
$$
\begin{align}
E[Y] &= \sum_{y=0}^{\infty}y\cdot P(X=y) = \sum_{y=0}^{\infty}y \cdot {r+y-1\choose y} p^r(1-p)^y  \\
& = \sum_{y=1}^{\infty}\frac{(r+y-1)!}{(y-1)!(r-1)!} p^r(1-p)^y = \sum_{y=1}^{\infty}\frac{r\cdot(r+y-1)!}{r\cdot (y-1)!(r-1)!} p^r(1-p)^y \\
&=\sum_{y=1}^{\infty }r\cdot {r+y-1\choose y-1} p^r(1-p)^y \text{ let z = y-1 then,} \\
 E[Y] &= r\cdot \sum_{z=0}^{\infty } {r+z\choose z} p^r(1-p)^{z+1}  \\
& = \frac{r(1-p)}{p}  \sum_{z=0}^{\infty } {r+1 +z-1\choose z} p^{r+1}(1-p)^{z} = \frac{r(1-p)}{p} \\
 \\
&Note: \text{ look at proof of pmf for that last line}
\end{align}

$$

**Variance:**

Reparametrizing with $μ=\frac{r(1-p)}{p}$ gives: $E[Y] = \frac{r(1-p)}{p} =\mu$ and $Var(Y) = \mu + \frac{1}{r}\mu^2$ therefore $Var(Y)>E[Y]$ 

- Variance is a quadratic function of the mean.
- $Var(Y)> E[Y]$, useful in modeling overdispersed count data.

### 6.2 Connection to Poisson Distribution

The Negative Binomial distribution converges to the Poisson distribution as:


$r→∞, p→ 1$ , such that $r(1−p)→λ$

Then:  $E[Y]→λ, Var(Y)→λ$
