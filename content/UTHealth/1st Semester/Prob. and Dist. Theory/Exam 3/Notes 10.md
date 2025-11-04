# Lecture 10: Multivariate Distribution

Motivation

- Many random variables (measures) can be defined over the high-dimensional sample space.
- It may be useful to know how different measures relate to each other.
- We want to encapsulate the relationships between different measures by examining the joint distribution of multiple random variables.

## 1 Bivariate Discrete Distribution

**Definition:** $Y_{1} , Y_{2}$ are both discrete. The Joint or bivariate probability distribution is given by
$$
P(y_{1},y_{2}) = P(Y_{1}=y_{1}, Y_{2}=y_{2})
$$
It is called joint p.m.f.

**Theorem:**

1. $p(y_{1} , y_{2} )≥ 0 ,∀y_{1} , y_{2}$

2. $∑_{y_{1} , y_{2}}p(y_{1} , y_{2}) = 1$


**Definition:** Joint (bivariate) c.d.f. $F(y_{1} , y_{2}) =P(Y_{1} ≤y_{1} , Y_{2} ≤y_{2} )$
$$
= \sum_{t_{1}=-\infty}^{y_{1}}\sum_{t_{2}=-\infty}^{y_{2}}p(t_{1},t_{2})
$$
## 2 Bivariate Continuous Distribution

**Definition:** $Y_{1} , Y_{2}$ both continuous r.v.’s with joint distribution function $F(y_{1} , y_{2})$, if there exists a non-negative function $f(y_{1} , y_{2})$ such that
$$
F(y_{1}, y_{2}) = \int_{-\infty}^{y_{1}}\int_{-\infty}^{y_{2}}f(t_{1},t_{2})dt_{2}dt_{1}
$$
for all$−∞ < y_{1} < ∞$, $−∞ < y_{2} < ∞$, then $Y_{1}$ and $Y_{2}$ are said to be jointly continuous r.v.’s, function $f(y_{1} , y_{2})$ is called the joint density function.
- **Note:** "joint distribution functions" is same as 'CDF' 

**Theorem:** If $Y_{1}$ and $Y_{2}$ are r.v.’s with joint distribution function $F(y_{1} , y_{2})$ then:

1. $F(−∞,−∞) = 0,\space F(−∞, y_{2} ) = 0,\space F(y_{1} ,−∞) =0$

2. $F(∞,∞) =1$

3. If $y^*_{1} ≥y_{1}$ and $y^*_{2} ≥y_{2}$

$$
F(y^*_{1}, y^*_{2}) -F(y^*_{1}, y_{2})-F(y_{1}, y^*_{2})+F(y_{1},y_{2}) = P(y_{1}\leq Y_{1}\leq y^*_{1}, \space y_{2}\leq Y_{2}\leq y^*_{2})
$$

**Theorem:** If $Y_{1} , Y_{2}$  jointly continuous r.v.’s with a joint density function $f(y_{1} , y_{2})$, then:

1. $f(y_{1} , y_{2})≥0$, for all $y_{1} , y_{2}$

2. $∫^{−∞}_{∞} ∫^{−∞}_{∞} f(y_{1},y_{2})dy_{1} dy_{2} = 1$

3. $\frac{\partial^2F(y_{1},y_{2})}{\partial y_{1}\partial y_{2}}=f(y_{1} , y_{2})$ (mixed second partial derivative)

## 3 General Discrete Joint PMF

- While it is possible to have a joint distribution between a mixture of discrete and continuous random variables, for this course we will focus on the joint distribution between random variables that are either all discrete random variables or all continuous random variables.  
    
**Definition:** Let $X_{1} , X_{2} ,... , X_{n}$ all be discrete random variables, each with the support $S_{1} ,... , S_{n}$, respectively. The joint probability mass function (joint PMF, for short) is


- **Note:** The probability $P(X_{1} =x_{1} , X_{2} =x_{2} ,... , X_{n}=x_{n})$ is equivalent to the statement.
- Let$X_{1} ,... , X_{n}$ be discrete random variables with joint PMF $p(x_{1} ,... , x_{n})$. Let $S_{1} ,... , S_{n}$ be their corresponding supports. Then,  
    1. $p(x_{1} ,... , x_{n})≥ 0, ∀x_{1} ∈S_{1} ,... , x_{n}∈S_{n}$.  
    2. $\sum_{x_{1}\in S_{1}}\sum_{x_{2}\in S_{2}}\dots\sum_{x_{n}\in S_{n}}p(x_{1},\dots, x_{n}) = 1$x
## 4 General Joint CDF

**Definition:** Let $X_{1} , X_{2} ,... , X_{n}$ be (discrete or continuous) random variables. The joint cumulative distribution function for $X_{1} , X_{2} ,... , X_{n}$ is

for $−∞< x-1 , x_{2} ,... , x_{n}<∞$.

1. If any of the values input into the CDF is−∞, the result is 0, i.e.,  
$$
\begin{align}
F(-\infty, \dots , -\infty) &= F(x_{1}, -\infty, \dots, -\infty) \\
&= F(x_{1}, x_{2}, -\infty, \dots, -\infty) \\
&\vdots \\
& = F(x_{1}, \dots, x_{n-1}, -\infty) \\
& = 0
\end{align}
$$
2. $F(∞,... ,∞) = 1.$

## 5 General Continuous Joint PDF

Definition: Let $X_{1} , X_{2} ,... , X_{n}$ be continuous random variables with joint cumulative distribution function $F(x_{1} , x_{2} ,... , x_{n})$. If there exists a non-negative function $f(x_{1} , x_{2} ,... , x_{n})$ such that

for all real values $x_{1},... , x_{n}$, then the function $f(x_{1} , x_{2} ,... , x_{n})$ is called the joint  
probability density function of $X_{1} , X_{2} ,... , X_{n}$.

- Let $X_{1} ,... , X_{n}$ be continuous random variables, and let $f$ be their joint PDF.
    1. $f(x_{1} ,... , x_{n})≥0 \space for\space ∀x_{1} ,... , x_{n}$.
    2. $\int_{-\infty}^{\infty}\dots \int_{-\infty}^{\infty}f(x_{1}, \dots, x_{n})dx_{1}\dots dx_{n}=1$
- It is worth noting that sometimes we only consider doing integration on the support of $X_{1} ,... , X_{n}$, where the support $S=\left\{(x_{1} ,... , x_{n}) :f(x_{1} ,... , x_{n})> 0 \right\}$is a region of $\mathbb{R}^n$.  

**Theorem.** Let $X_{1} , X_{2} ,... , X_{n}$ be continuous random variables with joint PDF $f$, and let $A$ be a region in $S$. Then


- Specially,

## 6 Marginal Distribution and Conditional Distribution

### 6.1 Motivation

- We began this section of the course discussing the situation in which we take multiple measurements at the same time and would like to model how they relate to each other.
- In these cases, sometimes we would like to look at the underlying distribution of just one of those measurements. Other times we want to look at the distribution of a measurement, given the observation of a different measurement.
- The first concept is encapsulated in what we call the_____ of a random variable, while the second concept is addressed with what we call the____.

### 6.2 Definitions

- We will focus on defining marginal and conditional distributions when we are working with two random variables at a time (the bivariate case).
- Let $X_{1} , X_{2}$ be random variables with supports $S_{1} , S_{2}$.
- For this section, we will assume that $X_{1} , X_{2}$ are both the same kind of random variables. In other words, we will assume that $X_{1} , X_{2}$ are either both discrete, or are both continuous.

### 6.3 Marginal Distributions

- First, we will give the definition when $X_{1} , X_{2}$ are both discrete.  

**Definition:** Let $p$ be the joint PMF of $X_{1} , X_{2}$. Then the marginal distribution of $X_{1}$ is
- Now we will give the definition when $X_{1} , X_{2}$ are continuous.

**Definition:** Let $f$ be the joint PDF of $X_{1} , X_{2}$. Then the marginal distribution
of $X_{1}$ is

- **Note:** when you are looking for a marginal distribution, the random variable you integrate out will depend on the question you are trying to answer.

### 6.4 Conditional Distributions

- Now, we will give the definition of the conditional distribution when $X_{1} , X_{2}$ are both discrete.  

**Definition:** Let p be the joint PMF (PDF) of $X_{1} , X_{2}$ , and let $p_{2}$ be the marginal PDF of $X_{2}$. Then the conditional distribution of $X_{1}$ given $X_{2} =x_{2}$ (denoted $X_{1} |X_{2} =x_{2}$ ), where $x_{2}$ is in the support of $X_{2}$ , is

- And when $X_{1} , X_{2}$ are continuous, the definition is as follows:  
**Definition:** Let $f$ be the joint PDF of $X_{1} , X_{2}$ , and let $f_{2}$ be the marginal  PDF of $X_{2}$. Then the conditional distribution of $X_{1}$ given $X_{2} =x_{2}$ (denoted  $X_{1} |X_{2} =x_{2}$ ), where $x_{2}$ is in the support of $X_{2}$ , is

### 6.5 Notes

- **Note:** both marginal and conditional distributions are still distributions in their own right.
- This means that they adhere to all of the properties that PDFs do.
- This means that we can talk about the expectations of these distributions.


## 7 Independence

### 7.1 Motivation

- Much like how we discussed the concept of two events being independent of each other, we also discuss the idea of random variables being independent.
- When we say that two random variables are independent, we are conveying that the value of one of the random variables does not in any way affect the value of the other.
- If we can show that two measures are independent, then that means one measurement will be a useless predictor of the other measurement.

### 7.2 Definition

- Let $X_{1} , X_{2}$ be random variables with joint CDF $F$, and with marginal CDFs $F_{1}$ and $F_{2}$ , respectively.  

**Definition:** $X_{1}$ and $X_{2}$ are said to be *independent* if


**Definition:** If two random variables are not independent, then they are said
to be *dependent*.

### 7.3 Theorems

- There are a few theorems that make showing the independence of random variables somewhat easier.
- The first theorem has to do with when $X_{1}$ and $X_{2}$ are discrete.  

**Theorem:** Let $X_{1}$ and $X_{2}$ be discrete random variables with joint PDF $p$ and marginal PDFs $p_{1}$ and $p_{2}$ , respectively. Then $X_{1}$ and $X_{2}$ are independent iff

- The second theorem has to do with when $X_{2}$ and $X_{2}$ are continuous.

**Theorem:** Let $X_{1}$ and $X_{2}$ be continuous random variables with joint PDF $f$ and marginal PDFs $f_{1}$ and $f_{2}$ , respectively. Then $X_{1}$ and $X_{2}$ are independent iff


- The third theorem gives us an extra tool when $X_{1}$ and $X_{2}$ are continuous.


**Theorem:** Let $X_{1}$ and $X_{2}$ be continuous random variables with joint PDF
$f$. If for constant values $a, b, c, d$ ($a < b, c < d$) the pdf $f$ is positive only
when $a ≤x_{1} ≤ b$ and $c≤x_{2} ≤d$, and zero otherwise, then $X_{1}$ and $X_{2}$ are
independent iff


for some functions $g$ and $h$.

- The theorem specifically applies when the support of $X_{1}$ and $X_{2}$ do not depend on each other.
- Basically, if the PDF is positive over a square region of space, then if the PDF can be written as the product of a function of $x_{1}$ and a (different) function of $x_{2}$ , then $X_{1}$ and $X_{2}$ are independent.