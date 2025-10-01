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

**Expectation:**

**Variance:**

**Additional Properties:**

- Lack of memory: $P(X > s+t|X > s) =P(X > t)$
- Monotonicity: As $x↑,P(X=x)↓$

## 4 Hypergeometric Distribution

**Definition:** Sampling $n$ objects (without replacement) from a finite population of size $N$, which  
contains $K$ elements of type 1 (successes) and $N−K$ elements of type 2 (failures).

Let $X$ be the number of type 1 elements (successes) in the sample.

$Notation:$ $X∼Hyp(N,K,n)$

$PMF:$

### 4.1 Hypergeometric Distribution - Properties

Proof: $\sum_{k}P(X=k)=1$
$$
\begin{align}
\sum_{k}P(X=k) &= \sum_{k}\frac{{K\choose k}{N-k \choose n-k}}{{N \choose n}} \\
& \frac{1}{{N \choose n}} \cdot \sum_{k}{K \choose k}{N-K \choose n-k}
\end{align}
$$

Now we need to show that $\sum_{k}{K \choose k}{N-K \choose n-k}={N \choose n}$.

Let’s think about this combinatorically. The left side counts the number of ways to:

- Choose $k$ items from $K$ success items:$K\choose k$ways
- Choose $n−k$ items from $N−K$ failure items:${N-K \choose n-k}$ ways
- Sum over all possible values of $k$

Therefore:  
$$
\sum_{k}P(X=k)=\frac{1}{{N \choose n}}\cdot {N \choose n} = 1
$$

**Expectation:**

**Variance:**

**Theorem:** The value of $N$ that maximizes $P(X=x)$ (as a function of $N$) occurs approximately  
at:  $\hat{N} = \frac{nK}{x}$

**Proof Outline:**  
$$
P(X=k)=\frac{{K \choose k}{N-K \choose n-k}}{{N \choose n}}
$$


### 4.2 Approximation

Recall  
$$
E[X] = n \cdot \frac{K}{N}, \space Var[X] = n \cdot \frac{K}{N}\cdot\left( 1- \frac{K}{N} \right)\cdot \frac{N-n}{N-1}
$$

For large $N$ and small $n$:

Thus, the hypergeometric distribution can be approximated by a binomial distribution when  
sampling fraction $\frac{N}{n}$ is small.

Example: Suppose $K= 4$ animals are tagged and released. A sample of $n= 3$ animals is taken  
at random. Let $X$ be the number of tagged animals observed in the sample. Find $P(X= 1)$ as a  
function of $N$ and find the value of $N$ that maximizes it.

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

**Example:** Suppose on a given weekend, the number of traffic accidents at a certain intersection  
follows a Poisson distribution with $λ= 0.7$. What is the probability that there will be at least $3$  
accidents at the intersection during the weekend?

### 5.1 Poisson Distribution - Properties

**Proof:** $\sum_{k=0}^{\infty} P(X=k)=1$

**Expectation:**

**Variance:**

**Example:** Among $400$ people, what is the probability that $3$ or more have a birthday on July  
$4th$? (assume $365$ days)

**Assumptions:**

- Probability that any person has a birthday on July 4:
- Let
- Use Poisson approximation:

**Probability of at least 3 birthdays:**

$P(Y ≥3) = 1−P(Y = 0)−P(Y = 1)−P(Y = 2)$

## 6 Negative Binomial Distribution

- The Binomial distribution counts successes in a fixed number of trials.
- The Negative Binomial distribution counts the number of trials needed to achieve a fixed  
    number of successes.
- Arises naturally when:
    - We perform independent $Bernoulli(p)$ trials
    - And stop when we reach the $r-th$ success

**Definition #1:**

Let $X$ be the trial on which the $r-th$ success occurs in a sequence of $Bernoulli(p)$ trials.

Then $X$ has a Negative Binomial distribution:

- : number of successes
- : trial of $r-th$ success
- : probability of success on each trial

**Definition #2:**

Alternatively, define $Y=X−r$, the number of failures before the $r-th$ success.
$$
P(Y=y) = {r+y-1\choose y} p^r(1-p^y), \space y = 0,1,2, \dots
$$
- Random variable $Y$ counts failures instead of trial number

### 6.1 Negative Binomial Distribution - Properties

**Expectation:**

**Variance:**

Reparametrizing with $μ=\frac{r(1-p)}{p}$ gives:

- Variance is a quadratic function of the mean.
- $Var(Y)> E[Y]$, useful in modeling overdispersed count data.

### 6.2 Connection to Poisson Distribution

The Negative Binomial distribution converges to the Poisson distribution as:


$r→∞, p→ 1$ , such that $r(1−p)→λ$

Then:  $E[Y]→λ, Var(Y)→λ$

**Example:** Sampling fruit flies until 100 with vestigial wings are found. Let $X$ be the number of  
trials needed. Then the probability that we will have to examine at least $N$ flies is:

Or equivalently:

- This is a Negative Binomial with $r= 100$.
- Useful for biological population sampling.
- Help to determine how many fruit flies we are likely to look at.