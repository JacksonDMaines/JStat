Population Mean $(\mu)$ --> Sample Mean $(\bar{X})$
- **Population:** <u>Well defined set</u> of element
- **I.I.D.:** Independent and Identically distributed 
-  **Sampled Population:** $X_{1}, \dots, X_{n}$ 
$$
f(x_{1}, \dots, x_{n}) = \prod_{i=1}^{n}f(x_{i})
$$
when $X_{1}, \dots ,X_{n}$ are independent!

- **Statistics:** Function of observable random variables which cannot contain any unknown parameter. 
	- Needs to be observable
- $r^{th}$ Sample moment about $0$ (Raw Moment)
$$
M_{r}' = \frac{1}{n} \sum_{i=1}^n x_{i}^r = \bar{X}_{n}^r
$$
	- **Note:** When $r=1$ $M_{1}'=\bar{X}_{n}$
- $r^{th}$ Sample moment about $\bar{X}_{n}$ (Central Moment)
$$
M_{r} = \frac{1}{n} \sum_{i=1}^n (x_{i}-\bar{x}_{n})^r
$$
	- **Note:** When $r =1$ $M_{1}=0$
- Expectation of $r^{th}$ sample moment is equal to $r^{th}$ population moment
$$
E[M_{r}'] = \mu_{r}'
$$
Equally Variance of $r^{th}$ sample moment is equal to 
$$
Var(M_{r}') = \frac{1}{n}(\mu_{2r}' - (\mu_{r}')^2)
$$
- **Note:** Remember $Var(X) = E(X^2)-E(X)^2$



**Theorem:** 
$$
min_{a}\sum_{i=1}^n (x_{i}-a)^2=\sum_{i=1}^n(x_{i}-\bar{x})^2
$$
and
$$
(n-1)s^2 = \sum_{i=1}^n (x_{i}-\bar{x})^2 = \sum_{i=1}^nx^2-n\bar{x}^2
$$
