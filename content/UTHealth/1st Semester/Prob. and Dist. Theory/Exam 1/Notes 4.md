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

Example:

Let $X$ be the maximum of two rolls of a four-sided die. The sample space:

Then, for r.v. $X$, we have:

Check:

### 2.2 Cumulative Distribution Function (CDF)

**Definition:** The CDF of a discrete random variable $X$is:

**Properties:**

1. ___
2. F(x) is non-decreasing:
3. F(x) is right-continuous:

Step function:$F(x) =P[X≤x]$, where $X=max(\text{two 4-sides dices})$ 

### 2.3 Recovering PMF from CDF

Let $x_{1} < x_{2} < x_{3} <···$ be the possible values of $X$.

This shows the step-size (jumps) of the CDF equals the probabilities at those points.

**Example:** A die is rolled once. What is the probability of each outcome from 1 to 6? How does  
the probability accumulate?

**PMF:**

**CDF:**

**Example:** Two fair 6-sided dice are rolled. What is the probability of the sum of the two dice?

**PMF:**

Selected PMF values:

**CDF:**

## 3 Expected Value

**Definition:** Let $X$ be a discrete random variable with probability mass function (PMF) $f(x) =  P[X=x]$. The expected value (or mean) of $X$, denoted by$ $ or $μ$, is defined as: provided

that the sum exists.

- $x$: a possible value of the random variable.
- $f(x)$: the probability that $X=x$.
- The expected value is a of the possible values of $X$, weighted  
    by their probabilities.

Interpretation: If the experiment is repeated many times, the average value of $X$ will approach  
$E[X]$.

**Example:** Let $X$ be the outcome of rolling a fair six-sided die. Possible values: $x= 1, 2 , 3 , 4 , 5 ,6$.  
Each has probability: $P(X=x) =^16$

**Example:** Let a random variable $X$ have the following PMF: $P(X= 1) = 0. 2$ , $P(X= 2) =.15$ , $P(X= 3) = 0. 3$

### 3.1 Functions on Expected Value

#### 3.1.1 Linearity of Expectation

Let $X$ and $Y$ be random variables, and let $a$ and $b$ be constants. Then:

#### 3.1.2 Function of a Random Variable

Let $g(X)$ be a real-valued function of a discrete random variable $X$. Then:

You can compute the expectation of any function of $X$, such as $E[X^2 ]$, $E[lnX]$, etc.

Example: Flip a fair coin 100 times. Let:

$$Xi=\begin{cases}
1,&\text{if toss i is heads} \\
0 & \text{otherwise} 
\end{cases}$$

Let $H=\sum_{i=1}^{100}X_{i}$: total number of heads

Step 1: Compute expected value of each $Xi$

Step 2: Use linearity of expectation for the function $H=\sum_{i=1}^{100}X_{i}$

**Example:** Let $X$ be a random variable with known expected value:

$$
E[X] = 10
$$

Now define a new variable:  
$$Y = 3X+ 7$$

Use linearity of expectation:

Linearity of expectation allows direct computation without knowing the full distribution of the  
new variable $Y$.

## 4 Variance

**Definition:** Let $X$ be a discrete random variable with expected value $μ=E[X$]. The variance  
of $X$, denoted by $Var(X)$ or $σ^2$ , is defined as:

- It measures the spread or dispersion of the values of $X$ around the mean.
- A higher variance indicates values are more spread out; A lower variance means they are  
    clustered near the mean.
- The variance is in squared units, which is why we often use the square root — the standard  
    deviation.

Alternative Formula for Variance


$Var(X) =E[X^2 ]−(E[X])^2$ ,where $E[X^2 ] =\sum_{x}x^2\cdot f(x)$

Derivation:

### 4.1 Variance of a Linear Transformation

Let $ $, where $a,b∈\mathbb{R}$, and $X$ is a random variable.

Key Result:

Implications:

- Adding a constant (b) shifts the mean but does not affect variance.
- Scaling by $a$ stretches or compresses variability by a factor of $a^2$.

**Example:** If $Var(X) = 4$, then:  
$$Var(3X+ 5) =$$

### 4.2 Variance of a Sum: Independent Random Variables

Let $X$ and $Y$ be independent random variables. Then:

More generally:

Without independence, include a covariance term: