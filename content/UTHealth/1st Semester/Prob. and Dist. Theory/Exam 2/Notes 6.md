# Lecture 6: Moments of Discrete Distributions

## 1 Introduction to Moments

**Definition:** Moments are numerical measures that describe the shape and characteristics of a  
probability distribution.

The $k-th$ moment about the origin is defined as:

Special Cases:

- $1st$ moment
- $2nd$ moment

Central Moments

The $k-th$ central moment is defined as:

Special Cases:

- $1st$ central moment
- $2nd$ central moment

**Theorem:** Under some general conditions, the sequence of moments uniquely determines the  
distribution.

**Statement:** Let $X$ and $Y$ be two random variables. If their $i-th$ moments are equal for all  
$i∈{ 1 , 2 , 3 ,...}$, that is,

**Key Idea:**

## 2 Recall Taylor Series Expansion

**General Taylor Series:**

f(x) =f(x 0 ) +f′(x 0 )(x−x 0 ) +f  
′′(x 0 )  
2! (x−x^0 )

(^2) +f′′′(x^0 )  
3! (x−x^0 )  
(^3) +···+f(n)(x^0 )  
n! (x−x^0 )  
n+···  
**Maclaurin Series (whenx 0 = 0):**  
**Example:**

## 3 Moment Generating Function (MGF)

**Definition:** If $X$ is a random variable, then the expected value

is called the moment generating function (MGF)of $X$, if this expected value exists for all  
values of $t$ in some interval: $−h < t < h$ for $h >0$.

Using the Taylor series expansion ofet $X$:

### 3.1 MGF and Moments via Derivatives

Result 1:If $MX(t) =MY(t)$ for all $t∈(−h,h)⊂\mathbb{R}$, then

Theorem: If $MX(t)$ exists, then for any integer $k≥1$,

MGF Expansion and Derivatives:

Taking derivatives:

General Rule:

Common Applications:

- First moment (mean):
- Second moment:
- Variance: Var(X) =

## 4 MGF of Common Discrete Distributions

### 4.1 Poisson Distribution

Let $X∼Poisson(λ)$, then P(X=x) =λxxe−!λ for $x= 0, 1 , 2 ,...$

Derivation of MGF:

Computing Moments:

First derivative:

Second derivative:

Therefore:

- Mean:E[X] =
- Variance: Var(X) =

### 4.2 Bernoulli Distribution

Let $X∼Bernoulli(p)$, where P(X= 0) = 1−pandP(X= 1) =p.

MGF:  
MX(t) =E[etX] =

Computing Moments:

```
MX′(t) =pet⇒
MX′′(t) =pet⇒
```

Variance:  
Var(X) =MX′′(0)−(MX′(0))^2 =

### 4.3 Binomial Distribution

Let $X∼Binomial(n,p)$. The PMF isP(X=x) =(nx)px(1−p)n−xforx= 0, 1 ,...,n.

Derivation of MGF:

Computing Moments:

First derivative:

Second derivative:

Therefore:

- Mean:E[X] =np
- Variance: Var(X) =MX′′(0)−(MX′(0))^2 =

### 4.4 Geometric Distribution

Let $X∼Geometric(p)$, with PMF:

```
P(X=x) =qx−^1 p, x= 1, 2 , 3 ,..., whereq= 1−p
```

Derivation of MGF:

Computing the Mean:

Mean from MGF:  
μ=E[X] =MX′(0) =

## 5 Properties of the MGF

Theorem: MGF of Linear Transformation

LetY=aX+b. Then:  
MY(t) =etb·MX(at)

Proof:  
MY(t) =E[etY] =E[et(aX+b)]

Example: Suppose a random variableXhas MGF:

```
MX(t) =^4 e
```

```
t
5 −et=
```

Comparing with the MGF of the Geometric Distribution:

```
M(t) =
```

Now letY =X 2 + 3. Using the linear transformation property witha=^12 andb= 3:

Example: Given MGF:  
M(t) =^16 et+^26 e^2 t+^36 e^3 t

SinceM(t) =E[etY] =∑yety·P(Y =y), we can read off the PMF directly:

PMF ofY:

Example: Given MGF:  
M(t) =^16 e−t+^36 e^0 +^26 e^1.^5 t

PMF ofY:

## 6 Chebyshev’s Theorem

Theorem:For any random variableY with finite meanμand varianceσ^2 , for anyk >0,

Equivalently:

Use case:This theorem is useful when , but not the exact distribution.

Note:Chebyshev’s inequality is mostly useful whenk.

### 6.1 Proof of Chebyshev’s Theorem

Goal:Prove thatP(|Y−μ|≥kσ)≤k^12.

Proof:

Therefore:

Dividing both sides byk^2 σ^2 :

or equivalently:

### 6.2 General Inequality for Functions

A more general form (Markov’s inequality):

IfXis a random variable andh(X)≥0, then for anyc >0,

Chebyshev’s theorem is a special case where.

### 6.3 Applications of Chebyshev’s Theorem

Example 1:LetY be a random variable withμ= 100 andσ^2 = 100 (soσ= 10). Find valuesa  
andbsuch thatP(a≤Y ≤b)≥^59.

Using Chebyshev’s inequality:  
P(|Y−μ|< kσ)≥ 1 −k^12

Example 2: For a section of forest, the number of diseased trees per acre,Y, follows a Poisson  
distribution with meanλ= 10. Each diseased tree costs$3.00 to treat with insecticide, and there  
is also a fixed overhead of$50 equipment cost. LetC= 50 + 3Y be the total cost for a randomly  
selected acre.

Questions:

1. Find the expected value and standard deviation ofC.
2. Within what interval would you expectCto be with probability at least 0.75?

Solution: