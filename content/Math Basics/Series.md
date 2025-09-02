$\sum_{i=1}^{n}a_i$


Convergent: Has finite limit

Divergent: Has infinite limit

## Properties
Let $\sum_{}a_n$ and $\sum_{}b_n$ be convergent series, then
 - $c\in \mathbb{R}$
	 - $\sum_{}ca_{n}=c\sum_{}a_n$

- $\sum a_{n} \pm \sum b_{n}=\sum(a_{n}\pm bn)$

	Note:  you can also shift the index for example 
$$
\sum_{i=2}^{k} \frac{i+5}{2^i} = \sum_{n=0}^{k} \frac{(i+2)+5}{2^{i+2}}
$$
	You can also pull out terms from the summation for example
$$
\sum_{n=1}^{\infty} a_{n}=a_{1}+\sum_{n=2}^{\infty}a_{n}
$$
	In general 
$$
\sum_{n=1}^{\infty}a_{n}=\sum_{n=1}^{N}a_{n} + \sum_{n=N+1}^{\infty}a_{n}
$$

## Convergence
If $\sum a_{n}$ converges then $\lim_{ n \to \infty }a_{n}=0$
	Note: this is a implication! So just because $\lim_{ n \to \infty }a_{n}=0$ it doesn't mean $\sum a_{n}$ converges

## Divergence Test
If $\lim_{ n \to \infty }\neq 0$ then $\sum a_{n}$ will diverge

## Geometric Series
$$
\sum_{n=1}^{\infty}ar^{n-1}=\frac{a}{1-r}, \text{ convergent}
$$

## Harmonic Series
$$
\sum_{n=1}^{\infty} \frac{1}{n}, \text{ divergent}
$$
## Integral Test
Suppose $f(x)$ is a continuous, positive and decreasing function on $(k,\infty)$ and $f(n)=a_{n}$, then 
- if $\int_{k}^{\infty}f(x)dx$ is convergent so is $\sum_{n=k}^{\infty}a_{n}$
- if $\int_{k}^{\infty}f(x)dx$ is divergent so is $\sum_{n=k}^{\infty}a_{n}$

### Estimation of Integral Test
Let $s_{n}=\sum_{i=1}^{n}s_{i}$, then
$$
s_{n}+\int_{n+1}^{\infty}f(x)dx\leq S\leq s_{n}+\int_{n}^{\infty}f(x)dx
$$
## P-Series Test
if $k>0$ then $\sum_{n=k}^{\infty} \frac{1}{n^p}$
- converges if $p>0$
- diverges if $p<=1$


## Comparison Test 
Let $\sum a_{n}$ and $\sum b_{n}$ exist with $a_{n},b_{n}>0$ $\forall n$ and $a_{n}\leq b_{n}$ $\forall n$, then
- if $\sum b_{n}$ is convergent then so is $\sum a_{n}$
- if $\sum a_{n}$ is divergent then so is $\sum b_{n}$

### Estimation of Comparison Test
$$
R_{n}\leq T_{n}\leq \int_{n}^{\infty}g(x)dx
$$
where $g(x)=b_{n}$, $R_{n}=\sum_{i=n+1}^{\infty}a_{i}$, and $T_{n}=\sum_{i=n+1}^{\infty}b_{i}$


## General Notes

Decreasing a function
$$
\frac{a}{b} \text{ either}\begin{cases} 
\text{decrease a } \\ 
\text{increase b}

\end{cases} 
$$

to increase a function
$$
\frac{a}{b} \text{ either}\begin{cases} 
\text{increase a } \\ 
\text{decrease b}

\end{cases} 
$$

## Limit Comparison Test
Let $\sum a_{n}$ and $\sum b_{n}$ exist with $a_{n}\geq 0$, $b_{n}>0$ $\forall n$
$$
c=\lim_{ n \to \infty } \frac{a_{n}}{b_{n}}
$$
if $c>0$ and is finite, either both series converge or diverge

## Alternating Series Test
Let $\sum a_{n}$ and 
$$
a_{n} = \begin{cases}
(-1)^nb_{n}  \\
(-1)^{n+1}b_{n}
\end{cases}
$$
where $b_n \geq 0$ $\forall a_{n}$, then if
- $\lim_{ n \to \infty }b_{n}=0$ and
- $b_{n}$ is a decreasing sequence
then $\sum a_{n}$ is convergent

### Estimation Alternating Series Test
$|R_{n}|=|s-s_{n}|\leq b_{n+1}$


## Absolute Convergent
$\sum a_{n}$ is absolute convergent if $\sum|a_{n}|$ is convergent 

if 
- $\sum a_{n}$ is convergent and
- $\sum |a_{n}|$ is divergent 
then its conditionally convergent

## Ratio Test
Let $\sum a_{n}$ exist and
$$
L=\lim_{ n \to \infty } \Big| \frac{a_{n+1}}{a_{n}}\Big|
$$
then, 
- if $L<1$ the series is absolutely convergent (thus convergent)
- if $L>1$ the series is divergent
- if $L=1$ the series may be divergent, conditionally convergent, or absolutely convergent

### Estimation Ratio Test
Let $r_{n}=\frac{a_{n+1}}{a_{n}}$ 

if $\{r_{n}\}$ is decreasing and $r_{n+1}<1$ 
$$
R_{n}\leq \frac{a_{n+1}}{1-r_{n+1}}
$$
else
$$
R_{n}\leq \frac{a_{n+1}}{1-L}
$$
where $L=\lim_{ n \to \infty } |\frac{a_{n+1}}{a_{n}}|$ 


## Root Test
Let $\sum a_{n}$ exist, and $L=\lim_{ n \to \infty }\sqrt[n]{|a_{n}|}=\lim_{ n \to \infty }|a_{n}|^{\frac{1}{n}}$ then, 
- if $L<1$ the series is absolutely convergent (thus convergent)
- if $L<1$ the series is divergent
- if $L=1$ the series may be divergent, conditionally convergent, or absolutely convergent 

Note: $\lim_{ n \to \infty }n^{\frac{1}{n}}=1$


## Power Series
$$
\sum_{n=0}^{\infty}c_{n}(x-a)^n
$$

## Radius of Convergence
$\exists R$ s.t. the series converges for $|x-a|<R$ and diverges of $|x-a|>R$, so

	$a-R<x<a+R$ Converges

	$x<a-R\text{ and }x>a+R$ Diverges


## Taylor Series
$$

f(x) = \sum _{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n
$$
Note: Maclaurin series is when $a=0$ 

nth degree taylor polynomial
$$
T_{n}(x)=\sum_{i=0}^{\infty} \frac{f^{(i)}(a)}{i!}(x-a)^i
$$

### Theorem:
Suppose $f(x)=T_{n}(x)+R_{n}(x)$, then 
	if $\lim_{ n \to \infty }R_{n}(x) = 0$ for $|x-a|<R$ then, 
$$
f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(x)}{n!}(x-a)^n
$$
	on $|x-a|<R$


## Some Useful Formulas
$$
e^x=\sum_{n=0}^{\infty} \frac{x^n}{n!}
$$
$$
\cos(x) = \sum_{n=0}^{\infty} (-1)^n\cdot \frac{x^{2n}}{(2n)!}
$$

$$
\sin(x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!}
$$

$$
\frac{1}{1-x}=\sum_{n=0}^{\infty}x^n
$$
$$
\ln(1+x)=\sum_{n=0}^{\infty}(-1)^n\frac{x^n}{n}
$$


## Binomial
### Theorem
if $n \in \mathbb{Z}^{+}$ then, 
	$(a+b)^n= \sum_{i=0}^{n} {n\choose i}a^{n-i}b^{i}$

where
	${n\choose i} =\frac{n!}{i!(n-i)!}$ 

Note: ${n \choose_{0}} = 1$



### Series
if K is any number and $|x|<1$ then, 
$$
(1+x)^k=\sum_{n=0}^{\infty} {k\choose n}{x^n}
$$
	what a horrible variable choice? why????


