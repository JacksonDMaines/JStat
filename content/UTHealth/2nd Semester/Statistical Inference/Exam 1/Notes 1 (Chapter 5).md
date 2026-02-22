## Day 1
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


## Day 2
 **Sample Variance:**
$$
S^2_{n} = \frac{1}{n-1}\sum_{i=1}^n(x_{i}-\bar{x}_{n})^2
$$
**Note:** $(n-1)S^2=\sum_{i=1}^n(x_{i}-\bar{x}_{n})^2=\sum_{i=1}^nx_{i}^2-n\bar{x}^2_{n}$

Degrees of freedom:
- Independent variables +1
- Dependent variables -1

**Corollary:**
- $E[\bar{X}_{n}] = \mu$
- $Var(\bar{X}_{n})= \frac{\sigma^2}{n}$

**Unbias:** Mean of estimated quantity is quantity itself
- IDK if this is the right def.

**Theorem:** MGF of $\bar{X}$
$$
M_{\bar{X}}(t) = \left[ M_{X}\left( \frac{t}{n} \right) \right]^n
$$
**Theorem:** Let $r\leq s$ if $E[X^2]<\infty$ (i.e. it exists), then $E[X^r]<\infty$ 
- Basically if the higher order moment exists then all the lower order moments exist. 

## Day 3
$X, Y$ are continuous r.v. $Z=X+Y$
$$
f_{Z}(z) = \int_{-\infty}^{\infty}f_{x}(w)f_{y}(z-w)dw
$$
### **Chi-Squared**
$$
Z_{1}, \dots, Z_{k} ~N(0,1) \implies \sum_{i=1}^kZ_{i} \sim \chi^2_{k}
$$
**PDF**
$$
\frac{1}{\Gamma\left( \frac{k}{2} \right)}\left( \frac{1}{2} \right)^{k/2}x^{k/2-1}e^{\frac{-1}{2}x}\cdot I(0,\infty)(x)
$$
**Note:** If $X\sim \chi^2_{k}$ then $X\sim gamma\left( \frac{k}{2},2 \right)$

$E[X] = k$

$Var(X) = 2k$

$M_{X}(t) = \left(\frac{1}{1-2t}\right)^{k/2}$
- for $t< \frac{1}{2}$


**Theorem:**
$X_{i} \sim N(\mu, \sigma^2)$, i's are independent
$$
\sum_{i=1}^k \left( \frac{x_{i}-\mu}{\sigma} \right)^2 \sim \chi^2_{k}
$$

$Z_{i}$ sampled from $N(0,1)$
- $\bar{Z} \sim N(0,1)$
- $\bar{Z}$ and $\sum(z_{i}-\bar{z})^2$ are independent 
- $\sum(z_{i}-\bar{z})^2\sim \chi^2_{n-1}$

$$
U= \frac{(n-1)S^2}{\sigma^2} \sim \chi^2_{n-1}
$$

If $X_i$'s are independent and $X_{i}\sim \chi^2_{p_{i}}$ then 
$$
X_{1} + X_{2}+ \dots + X_{n} \sim \chi^2_{p_{1}+p_{2}+ \dots p_{n}}
$$


### **t-dist**
- When $Z\sim N(0,1)$ and $U\sim \chi^2_{k}$
- $Z \perp U$ then
$$
\frac{Z}{\sqrt{ \frac{U}{k} }} \sim t_{k}
$$
- $(-\infty, \infty)$
- $E[X] = 0$ (k>1)
- $Var(x) = \frac{k}{k-2}$ (k>2)


### **F-dist**
$U\perp V$
- $U\sim \chi^2_{m}$
- $V\sim X^2_{n}$ then, 
$$
F = \frac{\frac{U}{m}}{\frac{V}{n}} \sim F_{m,n}
$$
- $(0, \infty)$
- $E[X] = \frac{n}{n-2}$ (n>2)
- $Var(X) = \text{some crazy shit}$

- $X\sim F_{p,q}\implies \frac{1}{X} \sim F_{q,p}$
- $X\sim t_{q} \implies X^2 \sim F_{1,q}$
- $X\sim F_{p,q} \implies \frac{\left( \frac{p}{q} \right)x}{\left( 1 + \left( \frac{p}{q} \right)x \right)} \sim Beta\left( \frac{p}{2}, \frac{q}{2} \right)$

## Day 4

### Order Statistics

Single 
$$
f_{Y_{k}}(x) = \frac{n!}{(k-1)!1!(n-k)!} [F(X)]^{k-1}[1-F(x)]^{n-k}f(x)

$$
Joint
$$
f_{Y_{j}Y_{k}}(x,y) = \frac{n!}{(j-1)!(k-j-1)!(n-k)!}[F(x)]^{j-1}[F(y)-F(x)]^{k-j-1}[1-F(y)]^{n-k}f(x)f(y)
$$

**Range and Midrange?**
$$
\text{Range = }R = X_{(n)}-X_{(1)}
$$
$$
\text{Midrange = }V = \frac{X_{n}+X_{1}}{2}
$$
$$
f(R,V) = f_{X,Y}(r,v)\cdot|J|
$$
## Day 5
### Convergence
$$
\forall \epsilon < 0  \space \exists N \in \mathbb{N}_{0} \space s.t.\space  \forall n>N \space |a_{n}-a|< \epsilon
$$


#### Convergence in Probability 
$\forall \epsilon < 0$
$$
\lim_{ n \to \infty } P(|X_{n}-x|\geq \epsilon) = 0
$$
or 
$$
\lim_{ n \to \infty } P(|X_{n}-x|< \epsilon) = 1
$$
then $X_{n}- > x$ in probability
- **Note:** Second one is more useful

#### Chebyshev's Inequality 
$$
P(|X-\mu|\geq t) \leq \frac{Var(x)}{t^2}
$$
#### Weak Law of Large Numbers
$X_{i}$ are iid with $E[X_{i}]= \mu$ and $Var(X_{i})<\infty$, Let $\bar{X}_{n}= \frac{1}{n}\sum_{i=1}^nx_{i}$ then $\forall \epsilon < 0$ 
$$
\lim_{ n \to \infty } P(|\bar{X}_{n}-\mu| < \epsilon) =1
$$
then $\bar{X}_{n} \to \mu$ in probability

#### Unbiased
$T(X)$ if an unbiased estimator of $\theta$ if $E[T(X)] = \theta$

#### Consistency
$T_{n}(X)$ is a consistent estimator of $\theta$ if $T_{n}(X) \to \theta$ in probability

#### Almost Sure Convergence
$$
P(\lim_{ n \to \infty } |X_{n}-x|< \epsilon) = 1
$$
then $X_{n}\to x$ almost surely

- **Note:** almost surely implies convergence in probability

#### Strong Law of Large Numbers
$X_{1},X_{2}, \dots$ are iid and $\forall \epsilon<0$
$$
P(\lim_{ n \to \infty } |\bar{X}_{n}-\mu|<\epsilon) = 1
$$
that is $\bar{X}_{n}\to \mu$ almost surely


#### Convergence in Distribution
$$
\lim_{ n \to \infty } F_{X_{n}}(x) = F_{X}(x) 
$$
$\forall x$ where $F_{X}(x)$ is continuous then $X_{n}\to x$ in distribution


## Day 6
#### Convergence of MGF's
$Y_{n}$ has cdf $F_{Y_{n}}$ and MGF $M_{Y_{n}}(t)$ exists for all $|t|<h $ and $\forall n$
$$
\lim_{ n \to \infty } M_{Y_{n}}(t) = M(t)
$$
then $F_{Y_{n}}\to F_{Y}$ in distribution


#### Central Limit Theorem
$X_{i}\sim iid$ distribution and MGF exists
$$
\frac{\sqrt{ n }(\bar{X}-\mu)}{\sigma} \to N(0,1)
$$
in distribution when both $\mu$ and $\sigma^2$ exist

Also Note:
- $\sqrt{ n }(\bar{X}-\mu) \to N(0,\sigma^2)$ in distribution
- $\sqrt{ n }(\bar{X}) \to N(\mu,\sigma^2)$ in distribution
- $\frac{\sqrt{ n }(\bar{X})}{\sigma} \to N(\mu,0)$ in distribution


#### Continuous Mapping Theorem
- $X_{n}\to x$ in distribution $\implies$ $g(X_{n})\to g(x)$ in distribution
- $X_{n}\to x$ in probability $\implies$ $g(X_{n})\to g(x)$ in probability
- $X_{n}\to x$ almost surely $\implies$ $g(X_{n})\to g(x)$ almost surely
when $g$ is a continuous function

#### Slutsky's Theorem
$X_{n}\to x$ in distribution and $Y_{n}\to c$ in probability, then
- $X_{n}+Y_{n}\to X+c$ in distribution 
- $X_{n}Y_{n}\to X\cdot c$ in distribution 
- $\frac{X_{n}}{Y_{n}}\to \frac{X}{c}$ in distribution if $c\neq 0$


#### Delta Method
$\sqrt{ n }(Y_{n}-\theta) \to N(0,\sigma^2)$ in distribution then $g(\theta)$ exists and $g'(\theta) \neq 0$ then 
$$
\sqrt{ n }(g(Y_{n})-g(\theta)) \to N(0, [g'(\theta)]^2\sigma^2)
$$

#### Second Delta Method
$\sqrt{ n }(Y_{n}-\theta) \to N(0,\sigma^2)$ in distribution then $g(\theta)$ exists and $g'(\theta) = 0$ and $g''(\theta) \neq 0$ then
$$
n[g(Y_{n})-g(\theta)]\to \sigma^2 \cdot \frac{g''(\theta)}{2}\cdot \chi^2_{1}
$$

