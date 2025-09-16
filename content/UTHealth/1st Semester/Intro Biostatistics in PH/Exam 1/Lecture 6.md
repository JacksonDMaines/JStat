# Random Variables
Function that assign values to different events.

$$
P(X=x)
$$
where $X$ "big X" is the random variable and $x$ "little x" is the event.

**Ex:** Toss a coin 3 times 
- $P(X=1)$, "the probability you observe 1 head in 3 tosses"

## Discrete Random Variables
- Only Integers $\mathbb{Z}$
- Probability Mass Function (PMF)

### Expectation
- $E[x]=\mu=mean$
$$
E[X]=\sum_{i=1}^{k}x_{i}\cdot P(X=x_{i})
$$
### Variance
- $Var[X]=\sigma^2=\text{avg. SD}$
$$
Var[X]=E[(x_{i}-\mu)^2]= \sum_{i=1}^{k}(x_{i}-\mu)^2 \cdot P(X=x_{i})
$$

### Binary
- Yes or No
$$
x = \begin{cases} 1& heads \\
0&tails \end{cases}
$$
$$
\begin{align}
&P(X=1)=\frac{1}{2}=p \\
&P(X=0)=\frac{1}{2}=q=1-p 
\end{align}
$$
### Combinations
- "n choose k"
$$
{n \choose k}=\frac{n!}{k!(n-k)!}
$$
- Number of ways to get $k$ success in $n$ trials (think binary)
- Number of ways to choose $k$ items out of $n$ total items (not binary)

