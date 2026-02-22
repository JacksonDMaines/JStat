# Random Vars/ Binomial Dist.
R.V.: Variable that takes numeric quantity that depends on the outcome of a random event

**Expected Value of discrete R.V.**
$$
E[X] = \sum x\cdot P(X=x)
$$
- Weighted averages of expected values 
**Variance value of discrete R.V.**
$$
Var(X) = \sum(X-E[X])^2\cdot P(X=x)
$$
- How far data is from expected point

**Properties of Expectation/Variance**
- $E[aX+bY] = aE[X] + bE[Y]$

When X is independent to Y
$$
Var(aX+bY) = a^2Var(X) + b^2Var(Y)
$$
When X is dependent to Y
$$
Var(aX+bY) = a^2Var(X) + b^2Var(Y) + 2ab\cdot Cov(X,Y)
$$


**Alternate form of Variance:**
$$
Var(X) = E[X^2] -E[X]^2
$$

## Bernoulli 
+ Single Case of binomial dist. 
+ PMF $P(X=x)= p^x(1-p)^{1-x}$ when $x=0,1$
+ Sum of Bernoulli -> Binomial
+ $E[X]=p$ and $Var(X) = p(1-p)$

## Binomial
- Counts # of Success 
- $P(X=x)={n \choose x}p^x (1-p)^{n-x}$ for $x=0,\dots,n$
- $E[X]=np$ and $Var(X)=np(1-p)$

# Poisson
Applies to the number of events over a period of time, where the $\lambda$ is the average of the number of events
$$
P(X=k) = \frac{e^{-\mu}\mu^k}{k!}
$$
$k= 0,1,2,3, \dots$
- Where $\mu = \lambda t$
	- $\lambda is the rate$
- **Assumption:**
	- Rate is homogeneous over time 
	- Independence
- When $X\sim Pois(X)$
	- $E[X]=\mu$
	- $Var(X)=\mu$


## Approximate Binomial with Poisson
When $n$ is large and $p$ is small we can approximate a Binomial distribution with a Poisson distribution
- $n\geq 100$
- $p\leq 0.01$
Then $\mu=np$

