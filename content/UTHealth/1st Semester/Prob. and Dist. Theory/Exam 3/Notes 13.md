# Lecture 13: Order Statistics

## 1 Order Statistics Definition

- A special way that we can transform random variables is by taking a bunch of random variables and finding their maximum and minimum values.
- Because our data is a collection of random variables, the maximum and the minimum values of the measurements will also be random variables.
- Therefore, the max and min will have their own distributions, which we can find if we know the distribution of our data.
- For the sections below, let $X_{1} , X_{2} ,... , X_{n}$be $i.i.d.$ (i.i.d. stands for mutually independent and identically distributed) with pdf $f(x)$ and cdf $F(x)$.
- Saying that $X_{1} ,... , X_{n}$ are $i.i.d.$ means that each random variable has the same probability distribution as the other random variables (i.e., they all have the same distribution) AND all of the random variables are independent from each other.
- Define $X(1)=min(X_{1},\dots, X_{n})=X_{min}$; $X(n)=max(X_{1},\dots,X_{n}) = X_{max}$, and more generally, order $X_{(1)}\leq X_{(2)}\leq\dots\leq X_{(n)}$. Call $X(k)$ the $k^{th}$ order statistic.
### 1.1 The maximum X(n)

The largest order statistic is the maximum value of $X_{1} , X_{2} ,... , X_{n}$, denoted $X(n)$. What we want to know is what the distribution of $X(n)$ is. We will proceed using the CDF transformation technique.
$$
\begin{align}
F_{X_{(1)}} = P(X_{n}\leq x)&= P(X_{1}\leq x_{1}, X_{2}\leq X_{2}, \dots X_{n}\leq x_{n}) \\
&= P(X_{1}\leq x) \cdot P(X_{2}\leq x) \cdot \dots \cdot P(X_{n}\leq x) \\
&= F(X)\cdot F(X)\cdot \dots \cdot F(X) \\
&= [F(x)]^n
\end{align}
$$
$$
f_{X_{(n)}}(x) = \frac{d}{dx}F_{X_{(n)}}(x) = n\cdot F(x)^{n-1}\cdot f(x)
$$
### 1.2 The minimum $X(1)$

The smallest order statistic is the minimum value of from $X_{1} , X_{2} ,... , X_{n}$, denoted $X(1)$. Again, we want to know what the distribution of $X(1)$ is. We will proceed using the CDF transformation technique.
$$
\begin{align}
F_{X_{(1)}}(n)=P(X_{(1)}\leq x) &= 1- P(X_{(1)}> x) \\
&= 1-P(X_{1}>x, X_{2}>x, \dots , X_{n}>x) \\
&= 1- P(X_{1}>x)\cdot P(X_{2}>x)\cdot \dots \cdot P(X_{n}>x) \\
&= 1 - (1-F(x))(1-F(x))\dots(1-F(x)) \\
&= 1 - (1-F(x))^n
\end{align}
$$
$$
f_{X(1)}(x) = \frac{d}{dx}F_{X_{(1)}}(x) = n\cdot (1-F(x))^{n-1}\cdot f(x)
$$
### 1.3 A general $X(j)$

**Definition:** Let $X_{(1)},... , X_{(n)}$ denote the order statistics of a random sample, $X_{1} ,... , X_{n}$, from a continuous population with cdf $F_{X}(x)$ and pdf $f_{X}(x)$. Then the pdf of $X(j)$ is
$$
f_{X_{(j)}}(x) = \frac{n!}{(j-1)!(n-j)!}\cdot f_{X}(x)\cdot [F_{X}(x)]^{j-1}\cdot [1-F_{X}(x)]^{n-j}
$$
**Proof:** We first find the cdf of $X(j)$ and then differentiate it to obtain the pdf. Let $Y$ be a random variable that counts the number of $X_{1} ,... , X_{n}$ less than or equal to $x$. Then, defining a “success” as the event ${Xj≤x}$, we see that $Y ∼binomial(n, F_{X}(x))$. (Note that we can write $P_{i}=F_{X}(x_{i})$. Also, although $X_{1} ,... , X_{n}$ are continuous random variables, the counting variable $Y$ is discrete.) Thus,
$$
F_{X_{j}}(x) = P(Y\geq j) = \sum_{k=j}^n {n \choose k}\cdot [F_{X}(x)]^k\cdot [1-F_{X}(x)]^{n-k}
$$
$$
\begin{align}
f_{X_{j}}(x) = \frac{d}{dx}F_{X_{(j)}}(x) = \sum_{k=j}^n {n \choose k}\cdot [F_{X}(x)]^k\cdot [1-F_{X}(x)]^{n-k}
\end{align}
$$
- Sorry long ass proof I don't wanna do. 