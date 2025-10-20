# Lecture 8: Common Continuous Distributions

## 1 Uniform Distribution

- We will begin to examine various continuous random variables, and we will start with one of the simplest, the continuous uniform random variable.
- Suppose you are waiting for a bus and the schedule says that the bus is to arrive at noon, but admits that the bus may be anywhere between 5 minutes early and 5 minutes late.
- Suppose that the probability density was evenly spread out over the whole range of possible times that the bus could arrive. What would the distribution of the arrival time of the bus look like?
- First, let’s define $X$ to be the arrival time, in terms of minutes from noon.
- This means that the support of $X$ is the interval $(-5,5)$. Note: The support of a continuous random variable $X$ is $\left\{x \in \mathbb{R}: f_{X}(x)>0\right\}$.
- When we say that the probability density is evenly spread out over the range of possible values, that means that the PDF is the same value, no matter what possible value is put into the function (i.e. $f_{X}(x) =c$ for$∀x∈S$, the support of $X$, where $c$ is a constant, and $f_{X}(x) = 0$ for $∀x \not∈S$.)
- But the support is only $(− 5 ,5)$ (which correspond to $11:55$ and $12:05$). So the PDF is just $0$ for all values outside of the support.
- Because the integral of $0$ is just $0$ over the intervals of the real line that aren’t the support of $X$, we have
$$
\int_{-\infty}^{\infty}f_{X}(x)dx = \int_{-5}^{5}f_{X}(x)dx=1
$$
- Furthermore, we know that the PDF is a constant for all values in $S$, so we can substitute $c$ in for $f_{X}(x)$ in $th$ integral and then solve for $c$, $c=10$
- Now suppose that we generalize this problem. Suppose that the bus may arrive any where from $a$ minutes from noon to $b$ minutes from noon, where $a < b$
- This means that our support would then be $(a,b)$.
- Again, we are assuming the probability density is evenly spread out over the possible times that the bus might show up. (i.e. evenly spread over the support)
- So, we will assume that
$$
f_{X}(x)\begin{cases}
c &\text{, if a<x<b} \\
0 & \text{, otherwise}
\end{cases}
$$
- We will again solve for the value of $c$, $c = \frac{1}{b-a}$.
- When a random variable $X$ has the support $(a,b)$ where $a$ and $b$ are real valued constants where $a < b$ and the pdf
$$
f_{X}(x)= \begin{cases}
\frac{1}{b-a} & a<x<b \\
0 & other 
\end{cases}
$$


We say that $X$ has a uniform distribution. (Symbolically, represented as $X∼U(a,b)$.)


### 1.1 Mean, Variance, & MGF

Let $X∼U(a,b)$.

1. **Mean**  
$$
E[X] = \frac{1}{2}(a+b)
$$
Proof.
$$
E[X] = \int_{a}^{b}f_{X}(x)dx = \int_{a}^{b}x \cdot \frac{1}{b-a}dx = \frac{b+a}{2}
$$

2. **Variance**
$$
Var(X) = \frac{(b-a)^2}{12}
$$
3. **MGF**
$$
M_{X}(t) = \begin{cases}
\frac{e^{bt}-e^{at}}{t(b-a)} &t\not=0 \\
0 & t = 0
\end{cases}
$$
## 2 Gamma Distribution

### 2.1 The Gamma Function

- Here we will go over the Gamma function, a function used to define and verify the Gamma distribution. 
**Definition 1.** The Gamma function is the function $Γ$ (defined for positive values) such that
$$
\Gamma(\alpha) = \int_{0}^{\infty}x^{t-1}e^{-x}dx \text{ for t>0}
$$
- This will be useful in solving integrals of the form$\int_{0}^{\infty}x^{t-1}e^{-x}dx$.
- Specially, $Γ(1) =1$.
- The Gamma function also has a useful property summarized in the following theorem:

**Theorem 1.** For all $t > 1$ ,  
$$Γ(t) = (t−1)Γ(t−1)$$

Proof.
$$
\begin{align}
\Gamma(t) &= \int_{0}^{\infty}x^{t-1}e^{-x}dx = - \int_{0}^{\infty}x^{t-1}de^{-x} \\
&\text{ by integration by parts } \\
&= -x^{t-1}e^{-x}|_{0}^{\infty} + \int_{0}^{\infty}e^{-x}(t-1)x^{t-2}dx  \\
&= (t-1)\Gamma(t-1) 
\end{align}

$$

- Note that this property has a particular implication when $t$ is an integer:  

**Theorem 2.** Let $t$ be a positive integer. Then:
$$Γ(t) = (t−1)!$$

- One other property about the Gamma Function that we will need is summarized in the following theorem:  

**Theorem 3.** $\Gamma\left( \frac{1}{2} \right) = \int_{0}^{\infty}x^{-1/2}e^{-x}dx = \sqrt{ \pi }$

### 2.3 The Gamma Distribution

- Some random variables are always non-negative and skewed to the right. To describe this kind to positive and right-skewed distribution, we define a new type of distribution call Gamma distribution.  


**Definition 2.** A continuous random variable $X$ is said to have a Gamma distribution with parameters $α > 0$ and $β > 0$, if and only if the density function of $X$ is
$$
f_{X}(x) = \begin{cases}
\frac{1}{\Gamma(\alpha)\beta^\alpha}x^{\alpha-1}e^{-x/\beta} &x>0 \\
0 & other
\end{cases}
$$


where $\Gamma(\alpha) = \int_{0}^{\infty}x^{\alpha-1}e^{-x}dx$.


- We can write $X∼Gamma(α,β)$ in short.
- Since this is a valid PDF, immediately we can get $\int_{0}^{\infty}x^{\alpha-1}e^{-x/\beta}= \Gamma(\alpha)\beta^\alpha$.
- The parameter $α >0$ is sometimes called the shape parameter, and the parameter $β >0$ is sometimes called the scale parameter.

### 2.4 Verification, Mean, Variance, and MGF

1. **Verification**
$$
\begin{align}
\int_{-\infty}^{\infty}f_{X}(x)dx & = \int_{0}^{\infty} \frac{1}{\Gamma(\alpha)\beta^\alpha}x^{\alpha-1}e^{-x/\beta} = \frac{1}{\Gamma(\alpha)\beta^\alpha} \int_{0}^{\infty}x^{\alpha-1}e^{-x/\beta} \\
 \\
& \text{ by U-Sub, u =}x/\beta \text{ and du=} \frac{1}{\beta}dx \\
 \\
&= \frac{\beta}{\Gamma(\alpha)\beta^\alpha} \int_{0}^{\infty}(\beta u)^{\alpha-1}e^{u}du = \frac{\beta- \beta^{\alpha -1 }}{\Gamma(\alpha)\beta^\alpha} \int_{0}^{\infty}u^{\alpha-1}e^{u}du  \\
&= \frac{\beta^\alpha}{\Gamma(\alpha)\beta^\alpha} \Gamma(\alpha) = 1
\end{align}

$$
1. **Mean**  
$$E[X] =αβ$$

Proof.
$$
\begin{align}
E[X] &= \int_{-\infty}^{\infty}x \cdot f_{X}(x)dx = \int_{0}^{\infty}x \cdot \frac{1}{\Gamma(\alpha)\beta^\alpha}x^{\alpha-1}e^{-x/\beta} \\
& = \frac{1}{\Gamma(\alpha)\beta^\alpha}\int_{0}^{\infty}x^{\alpha}e^{-x/\beta} = \frac{1}{\Gamma(\alpha)\beta^\alpha}\int_{0}^{\infty}x^{(\alpha + 1) -1}e^{-x/\beta} \\
&= \frac{1}{\Gamma(\alpha)\beta^\alpha} \Gamma(\alpha+1)\beta^{\alpha+1} = \alpha \beta
\end{align}
$$

3. **Variance**  
$$V[X] =αβ^2$$

Proof.
$$
\begin{align}
E[X^2] &= \int_{0}^{\infty}x^2\cdot f_{X}(x)dx = \int_{0}^{\infty}x^2 \cdot \frac{1}{\Gamma(\alpha)\beta^\alpha}x^{\alpha-1}e^{-x/\beta} \\
&= \frac{1}{\Gamma(\alpha)\beta^\alpha}\int_{0}^{\infty}x^{\alpha+1}e^{-x/\beta} = \frac{1}{\Gamma(\alpha)\beta^\alpha} \cdot \Gamma(\alpha + 2)\beta^{\alpha+2} = (\alpha + 1)\alpha \beta^2
\end{align}
$$
$$
Var(X) = E[X^2] - E[X]^2 = (\alpha + 1)\alpha \beta^2 - (\alpha \beta)^2 = \alpha \beta^2
$$

4. **Moment generating function**
$$
M_{X}(t) = (1-\beta t)^{-\alpha}, \text{ for } t< \frac{1}{\beta}
$$

### 2.5 Special Cases

**Definition 3.** Let $ν$ be a positive integer. A random variable $X$ is said to have a chi-square  
distribution with $ν$ degrees of freedom if and only if $X$ is a gamma-distributed random variable with parameters $α=ν/ 2$ and $β= 2$.

- It can be written by $X∼χ^2 (ν) =Gamma\left( \frac{ν}{2},2 \right)$.
- $E[X] =\nu$ , $V[X]=2\nu$.

**Definition 4.** A random variable $X$ is said to have an exponential distribution with parameter $β > 0$ if and only if the density function of $X$ is
$$
f_{X}(x) = \begin{cases}
\frac{1}{\beta} \cdot e^{-x/\beta} &x>0 \\
0 & other
\end{cases}
$$
- It can be written by $X∼Exp(β) =Gamma(1,β)$.
- $E[X] =\beta$, $V[X] =\beta^2$.
- CDF function
- It is a very useful distribution to model the length of life of electronic components.

## 3 Exponential Distribution

- **pdf:** $f_{X}(x) = \frac{1}{\beta}e^{-x/\beta}$ for $x>0$, $\beta>0$
- **cdf:** $F_{X}(x) = 1-e^{-x/\beta}$ for $x>0$
- $P(X > x) =1-F_{X}(x)=e^{-x/\beta}$, for $x>0$.
- **mgf:** $M_{X}(t) = \frac{1}{1-\beta t}$ for $t< \frac{1}{\beta}$
- Memoryless Property If $X∼Exp(β)$, then $P(X-t>s|X>t) = P(X>s)$ or equivalently,$P(X>s+t) = P(X>s)P(X>t)$ for $s,t>0$.  
Simple Proof: Assume $X∼Exp(β)$ 
$$
P(X-t>s|X>t) = \frac{P(\{X-t>s\}\cap\{X>t\})}{P(X>t)}= \frac{e^{-(t+s)/\beta}}{e^{-t/\beta}} = e^{-s/\beta} = P(X>s)
$$
- Hazard rate (Failure rate): Suppose $X$ has pdf $f(x)$, cdf $F(x)$, and $f(x) = 0$ for $x >0$.  
Define the hazard function
$$
h(t) = \lim_{ s \to 0^+ } \frac{P((t<x<t+\delta)|X>t)}{\delta} = \frac{f(t)}{1-F(t)} 
$$
- Fact: $X∼Exp(β)$ iff $h(t) = 1/β$ for all $t$.

## 4 Normal Distribution

### 4.1 Definition & Motivation

- Known by several names including Normal, Gaussian, the normal distribution is probably the most influential and important probabilistic distribution in statistics.

**Definition 5.** We say that the continuous random variable $X$ is normally distributed with parameters $μ$ and $σ^2$ when $X$ has the PDF
$$
f_{X}(x) = \frac{1}{\sqrt{ 2\pi \sigma^2 }}e^{\frac{-(x-\mu)^2}{2\sigma^2}}
$$
for any $x∈R$, where$-\infty<\mu<\infty$ and $0<\sigma^2<\infty$. We denoted this by$X\sim N(\mu,\sigma^2)$.

- The density of $X$ is symmetric and bell-shaped, centered at $μ$. We will show that $μ$ is the mean of $X$, $σ^2$ is the variance of $X$ later.
- By the property of a valid PDF, we have
$$
\int_{-\infty}^{\infty}e^{-\frac{(x-\mu)^2}{2\sigma^2}} = \sqrt{ 2\pi }\sigma
$$
### 4.2 Notes

- For our proofs of the verification, Mean, and variance of the normal distributions, we will be making use of a few mathematical properties of functions and integration.

- First, we will define odd and even functions:  
**Definition 6.** A function $g$ is an odd function if $g(-x)=-g(x)$ for all real values of $x$.  


**Definition 7.** A function $g$ is an even function if $g(-x) = g(x)$ for all real values of $x$.
- Functions can make integration easier, which we will highlight the following theorems:  

**Theorem 4.** Let $g$ be an even function defined for all real values, and let $a$ be a real constant. Then, 
$$
\int_{-a}^{a}g(x)dx = 2\cdot \int_{0}^{a}g(x)dx
$$



**Theorem 5.** Let $g$ be an odd function defined for all real values, and let $a$ be a real constant. Then,
$$
\int_{-a}^{a}g(x)dx = 0
$$


### 4.3 Verification, Mean, Variance, and MGF

1. **Verification**

Proof.

2. **Mean**  
$$E[X] =μ$$

Proof.

3. **Variance**

4. **MGF**

### 4.4 Standard Normal Distribution

- Standard normal distribution $N(0,1)$  
**Definition 8.** If $Z$ is a normally distributed random variable with parameters $μ= 0$ and  $σ= 1$, then $Z$ is said to have a standard normal distribution, whose density function is


for−∞< z <∞.

- Normal distribution is preserved for linear transformations. In other words, if $X∼N(μ,σ^2)$, then , for $a \not= 0$.
- We can always transform a normal random variable $X ∼N(μ,σ^2 )$ to a standard normal random variable $Z$ by using the relationship
- All problems about normal distribution can be transferred to standard normal distribution.

## 5 Beta Distribution

### 5.1 The Beta Function

- To help us define the Beta distribution, we will make use of what we call the Beta function.  
**Definition 9.** The Beta function $B(a,b)$ is a function of two positive values $a$ and $b$, and is defined to be:

**Theorem 6.** Let $a$ and $b$ be positive real values. Then,

### 5.2 Beta Dist’n & Motivation

- The Beta distribution is very useful for modeling bounded random variables with a nonuniform density.
- The Beta density is a two-parameter density function defined between $0$ and $1$. It is often used to model proportions, such as the proportion of impurities in a chemical product or the proportion of time that a machine is under repair.  
**Definition 10.** We say that the continuous random variable **X** has a Beta distribution with parameters $α$ and $β$ when $X$ has the PDF

,where $α > 0$ ,$β > 0$. We denote this.

- Often times the pdf of $X∼Beta(α,β)$ is simplified to be:
$$
f_{X}(x) = \begin{cases}
\frac{1}{B(\alpha,\beta)}x^{\alpha -1}(1-x)^{\beta-1} &0<x<1 \\
0 & other
\end{cases}
$$
- The uniform distribution between $0$ and $1$ is a special case of the Beta distribution. That is, $U(0,1) =Beta(1,1)$.

### 5.3 Verify, Mean, Variance

Let $X∼Beta(α,β)$.

1. **Verify**

Proof.

2. **Mean**
$$
E[X] = \frac{\alpha}{\alpha + \beta}
$$

Proof.

3. **Variance**  
$$
Var(x) = \frac{\alpha \beta}{(\alpha \beta + 1)(\alpha + \beta)^2}
$$
Proof

### 5.4 Special Cases

- If $α=β= 1$, then $f(x) =\frac{1}{B(1 ,1)}$.  
Since:


We have$f(x) =\frac{1}{B(1 ,1)}= 1$, which is a uniform distribution on $(0,1)$.

- If $α=β$, then $f(x) = \frac{x^{\alpha-1}(1-x)^{\alpha -1}}{B(\alpha, \alpha)}$ is symmetric about $x= 0.5$.

## 6 Log-Normal Distribution

### 6.1 Definition

A random variable $X$ has a log-normal distribution if $ln(X)∼N(μ,σ^2 )$.

### 6.2 PDF and CDF

The probability density function is:

The cumulative distribution function is:

### 6.3 Moments

**Expectation:** $E[X] =$.

**Variance:** $Var(X) =$.

## 7 Weibull Distribution

- **pdf:**
$$
f_{X}(x) = \begin{cases}
\frac{\beta x^{\beta-1}}{\theta^\beta}e^{-(x/\theta)^\beta} & x\geq 0 \\
0 &x<0
\end{cases}
$$
- Denote as $X∼WEI(θ,β)$ , $θ$ scale parameter, $β$ shape parameter
- $β= 1$, the Weibull distribution reduce to Exponential distribution.
- **CDF:**
$$
F(X) = \begin{cases}
1-e^{-(x/\theta)^\beta} & x\geq 0  \\
0 &x<0 
\end{cases}
$$
- $E(X) =θΓ(1 + 1/β)$
- $Var(X) =θ^2 [Γ(1 + 2/β)−(Γ(1 + 1/β))^2 ]$

## 8 Pareto Distribution

- **pdf:** 
$$
f_{X}(x) = \begin{cases}
\frac{\kappa}{\theta}\left( 1+ \frac{x}{\theta} \right)^{-(\kappa+1)} & x\geq 0 \\
0 & x<0 
\end{cases}
$$
• **CDF:**
$$
F(X) = \begin{cases}
1- \frac{1}{\left( 1+ \frac{x}{\theta} \right)^\kappa} & x\geq 0 \\
0 & x<0 
\end{cases}
$$

- $E(X) = \frac{\theta}{\kappa -1}$
- $Var(X) = \frac{\theta^2 \kappa}{(\kappa -2)(\kappa -2)^2}$

## 9 Location Scale Parameter

### 9.1 Location parameter

- A quantity $η$ is a location parameter of the distribution of $X$ if where $F_{0}$ and $f_{0}$ are valid cdf and pdf.
- $X∼N(μ,1)$. Then $μ$ is a location parameter. $F_{X}(x;μ) =F_{Z}(x−μ)$, where $F_{Z}$ is the cdf of standard normal distribution.
- Exponential distribution models the waiting time for event. Suppose an event only occurs after $η$ hours. Then, we can model this event waiting time by $f(x;η) = exp(−(x−η))$, for  $x > η$. $f_{0}$ we can define as $Exp(1)$.

### 9.2 Scale parameter

- A positive quantity $θ$ is a scale parameter for the distribution of $X$ if, where $F_{0}$ and $f_{0}$ are valid cdf and pdf.
- $X∼Exp(θ)$ is a scaled distribution of $Exp(1)$ PDF:.

### 9.3 Location-Scale Parameter

- Quantities $η$ and $θ$ are called location-scale parameter for the distribution of $X$ if, where $F_{0}$ and $f_{0}$ are valid cdf and pdf.
- $μ$ and $σ$ are location-scale parameter of $X∼N(μ,σ^2 )$.