# Lecture 4: Discrete Random Variable

## 1 Random Variables

### 1.1 What is a Random Variable?

**Definition:**
- A random variable (r.v) is a real-valued function defined on sample space $S$
- It maps outcomes of a random experiment to real numbers
- Denoted as $X,Y,Z$ (capital)

**Example:**

1. Let $X$ be the maximum of two rolls of a six-sided die.
2. Let $Y$ be the number of heads when tossing the coin 50 times.
3. Let $Z$ be the volume of raindrop at a given day.

### 1.2 Types of Random Variables

- **Discrete:** countable set of possible values (e.g., integers, finite counts).
- **Continuous:** can take any value in an interval.

### 1.3 Random Variables vs. Realized Values

- We use uppercase letters (e.g.,$X$) to denote random variables.
- We use the corresponding lowercase letter (e.g.,$x$) to denote a realized value (or possible  
    outcome) of the random variable.

**Example:**

Let $X$ be a random variable representing the outcome of a die roll. $X$= “outcome of the roll”  
The random variable $X$ could take the specific value $x= 4$.

Thus, we say “$X$ can take the value $x$” or “$X=x$”.

## 2 Discrete Random Variables

**Definition:** A random variable $X$ is said to be discrete if the set of all possible values is a  
countable list: $x_{1},x_{2}, \dots$

The function $f(x)=P[X=x],x=x_{1},x_{2}\dots$ that assigns the probability  
to each possible value $x$ is called the probability mass function(PMF) .

### 2.1 Properties of PMF

**Theorem:** A function $f(x)$ is a valid PMF if:
1. $f(x_{i})\geq 0, \forall x_{i}$
2. $\sum_{i}f(x_{i})=1,\forall x_{i}$
Interpretation:

- All probabilities must be non-negative.

- Total probability across all possible outcomes must equal 1.

**Example:**

Let $X$ be the maximum of two rolls of a four-sided die. The sample space:

Then, for r.v. $X$, we have:

|              | 2nd Roll |       |       |       |
| ------------ | -------- | ----- | ----- | ----- |
| **1st Roll** | **1**    | **2** | **3** | **4** |
| **1**        | 1        | 2     | 3     | 4     |
| **2**        | 2        | 2     | 3     | 4     |
| **3**        | 3        | 3     | 3     | 4     |
| 4            | 4        | 4     | 4     | 4     |


| $X$         | 1              | 2              | 3              | 4              |
| ----------- | -------------- | -------------- | -------------- | -------------- |
| $f(x)=P(X)$ | $\frac{1}{16}$ | $\frac{3}{16}$ | $\frac{5}{16}$ | $\frac{7}{16}$ |



Check:

### 2.2 Cumulative Distribution Function (CDF)

**Definition:** The CDF of a discrete random variable $X$ is:
$$
F(X) = P[X\leq x]=\sum_{x_{i}\leq x}f(x_{i}) 
$$

**Properties:**

1. $\lim_{ x \to \infty }F(x) = 1$ and $\lim_{ x \to -\infty }F(x)=0$
2. F(x) is non-decreasing: $F(a)\leq F(b)$ for $a\leq b$
3. F(x) is right-continuous: $\lim_{ h \to 0^+ }F(x+h)=F(x)$
 

### 2.3 Recovering PMF from CDF

Let $x_{1} < x_{2} < x_{3} <···$ be the possible values of $X$.
$$
\begin{align}
&f(x_{1}) = F(x_{i}) \\
&\vdots \\
&f(x_{j}) = F(x_{j})-F(x_{j-1}) \text{ for }j\geq 2
\end{align}
$$

This shows the step-size (jumps) of the CDF equals the probabilities at those points.

**Example:** Two fair 6-sided dice are rolled. What is the probability of the sum of the two dice?

**PMF:** $P(X=x) = \frac{\text{Number of outcomes with sum of x}}{36}$

|            | Dice 1 |       |       |       |       |       |
| ---------- | ------ | ----- | ----- | ----- | ----- | ----- |
| **Dice 2** | **1**  | **2** | **3** | **4** | **5** | **6** |
| **1**      | 2      | 3     | 4     | 5     | 6     | 7     |
| **2**      | 3      | 4     | 5     | 6     | 7     | 8     |
| **3**      | 4      | 5     | 6     | 7     | 8     | 9     |
| **4**      | 5      | 6     | 7     | 8     | 9     | 10    |
| **5**      | 6      | 7     | 8     | 9     | 10    | 11    |
| **6**      | 7      | 8     | 9     | 10    | 11    | 12    |

| X        | 2              | 3              | $\dots$ | 12             |
| -------- | -------------- | -------------- | ------- | -------------- |
| $P(X=x)$ | $\frac{1}{36}$ | $\frac{2}{36}$ | $\dots$ | $\frac{1}{36}$ |


## 3 Expected Value

**Definition:** Let $X$ be a discrete random variable with probability mass function (PMF) $f(x) =  P[X=x]$. The expected value (or mean) of $X$, denoted by$ $ or $μ$, is defined as:
$$
E[X] = \sum_{x}x\cdot f(x)
$$

provided that the sum exists.

- $x$: a possible value of the random variable.
- $f(x)$: the probability that $X=x$.
- The expected value is a **weighted average** of the possible values of $X$, weighted by their probabilities.

Interpretation: If the experiment is repeated many times, the average value of $X$ will approach  
$E[X]$.

**Example:** Let $X$ be the outcome of rolling a fair six-sided die. Possible values: $x= 1, 2 , 3 , 4 , 5 ,6$.  
Each has probability: $P(X=x) =\frac{1}{6}$ 
$$
E[X] = \sum_{x=1}^{6}x\cdot P(X=x) = \sum_{x=1}^{6}x \cdot \frac{1}{6} = \frac{21}{6 }= 3.5 
$$


**Example:** Let a random variable $X$ have the following PMF: $P(X= 1) = 0. 2$ , $P(X= 2) =.15$ , $P(X= 3) = 0. 3$
$$
E[X] = \sum_{x=1}^{3}x \cdot P(X=x) = 1(.2) + 2(.5)+3(.3) = 2.1
$$
### 3.1 Functions on Expected Value

#### 3.1.1 Linearity of Expectation

Let $X$ and $Y$ be random variables, and let $a$ and $b$ be constants. Then:
$$
E[aX+bY] = a\cdot E[X] + b\cdot E[Y]
$$
#### 3.1.2 Function of a Random Variable

Let $g(X)$ be a real-valued function of a discrete random variable $X$. Then:
$$
E[g(x)] = \sum_{x}g(x)\cdot f(x)
$$
**Note:** $g(E[X]) \not= E[g(X)]$ 

You can compute the expectation of any function of $X$, such as $E[X^2 ]$, $E[lnX]$, etc.

Example: Flip a fair coin 100 times. Let:

$$Xi=\begin{cases}
1,&\text{if toss i is heads} \\
0 & \text{otherwise} 
\end{cases}$$

Let $H=\sum_{i=1}^{100}X_{i}$: total number of heads

Step 1: Compute expected value of each $Xi$
$$
E[X_{i}]= \sum_{x=0}^{100}x \cdot \frac{1}{2} = 0\left( \frac{1}{2} \right) + 1\left( \frac{1}{2} \right) = \frac{1}{2}
$$

Step 2: Use linearity of expectation for the function $H=\sum_{i=1}^{100}X_{i}$
$$
E[H] = E\left[ \sum_{i=1}^{100}X_{i} \right] = \sum_{i=1}^{100}E[X_{i}] = 100 \cdot \frac{1}{2} = 50 
$$
**Example:** Let $X$ be a random variable with known expected value:

$$
E[X] = 10
$$

Now define a new variable:  
$$Y = 3X+ 7$$

Use linearity of expectation:
$$
E[Y] = E[3X+7] = 3 \cdot E[X] + 7 = 3 \cdot 10 + 7 = 37
$$

Linearity of expectation allows direct computation without knowing the full distribution of the  
new variable $Y$.

**Note:** Expectation of a constant is the constant itself. 

## 4 Variance

**Definition:** Let $X$ be a discrete random variable with expected value $μ=E[X$]. The variance  
of $X$, denoted by $Var(X)$ or $σ^2$ , is defined as:
$$
Var(X) = E[(X-\mu)^2] = \sum_{x}(x-\mu)^2\cdot f(x)
$$

- It measures the spread or dispersion of the values of $X$ around the mean.
- A higher variance indicates values are more spread out; A lower variance means they are  
    clustered near the mean.
- The variance is in squared units, which is why we often use the square root — the standard  
    deviation. $\sigma = \sqrt{ Var(X) }$

Alternative Formula for Variance


$Var(X) =E[X^2 ]−(E[X])^2$ ,where $E[X^2 ] =\sum_{x}x^2\cdot f(x)$

Derivation:
$$
\begin{align}
Var(X) &= E[(X-\mu)^2]  = E[X^2-2X\mu+\mu^2] \\
&=E[X^2]-2\mu E[X] +\mu^2 = E[X^2] - 2\mu \cdot \mu +\mu^2 \\
&=E[X^2] - \mu^2 = E[X^2]-(E[X]^2) 
\end{align}
$$

### 4.1 Variance of a Linear Transformation

Let $Y=aX+b$, where $a,b∈\mathbb{R}$, and $X$ is a random variable.

Key Result:
$$
Var(Y) = Var(aX+bY) = a^2\cdot Var(X)
$$

Implications:

- Adding a constant (b) shifts the mean but does not affect variance.
- Scaling by $a$ stretches or compresses variability by a factor of $a^2$.

**Example:** If $Var(X) = 4$, then:  
$$Var(3X+ 5) = 3^2 \cdot 4 = 36$$

### 4.2 Variance of a Sum: Independent Random Variables

Let $X$ and $Y$ be independent random variables. Then:
$$
Var(X+Y) = Var(X) + Var(Y)
$$
More generally:
$$
Var(aX+bY) = a^2\cdot Var(X) + b^2\cdot Var(Y)
$$

Without independence, include a covariance term:
$$
Var(X+Y) = Var(X) + Var(Y) +2\cdot Cov(X,Y)
$$
