
# Normal Distribution (Gaussian)
- Takes any real number
- Probability Density Function (PDF)
- Total area under curve = 1

## Normal Distribution
- Symmetric and Unimodal
**Denoted:** $X \sim N(\mu,\sigma)$

### Standard Normal Distribution
$$
X\sim N(0,1)
$$
- $\mu= mean = 0$
- $\sigma=sd =1$
$$
f(x)= \frac{1}{\sqrt{2\pi \sigma^2 }}e^{\frac{-(x-\mu)^2}{2\sigma^2}}
$$
## Z-Score
- Standardizing to a $N(0,1)$
$$
Z=\frac{x-\mu}{\sigma}
$$
- 68% of data is within 1 SD of the mean
- 95% of data is within 2 SD of the mean
- 99.7% of data is within 3 SD of the mean

**Note:** $|Z|>2$ is considered unusual

- Z-tables always show left area under curve, same with Stata 
You can normalize like the following
$$
P(X<x) = P(\frac{X-\mu}{\sigma}<\frac{x-\mu}{\sigma}) = P(Z<\frac{x-\mu}{\sigma}) 
$$
- **Note:** The equality here doesn't matter cause the probability of a continuous random variable at a single is point is 0. 
- Same idea works in a range **Ex:** $24<X<65$

## Approximate Binomial with Normal
If $X\sim Bin(n,p)$ then if 
- $np\geq 10$ and 
- $n(1-p)\geq 10$ 
then $X\sim N(np, \sqrt{np(1-p) })$ as n increases

#### Continuity Correction
$\pm .5$ for ranges of values before standardizing or approximating with normal. Example: 
$$
\begin{align}
&P(69<X<71) \\
&\text{then apply continuity correction} \\
&P(69-.5<X<71+.5)
\end{align}
$$

Then standardize with the new $\pm.5$ values. 
- **Note:** Really on used when you have ranges between values

Applying a continuity correction before standardizing can improve the accuracy of the  approximated probability. 



