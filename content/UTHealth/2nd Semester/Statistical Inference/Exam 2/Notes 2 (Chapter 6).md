
# Sufficiency

If $T(X)$ is a sufficient statistics for $\theta$, then any inference about $\theta$ should depend on the sample $X$ only through the value $T(X)$. 

**Def:** $T(X)$ is a sufficient statistic for $\theta$ if the conditional distribution of the sample $X$ given the value of $T(X)$ doesn't depend on $\theta$ 

**Theorem:** Let $p(x|\theta)$ be pdf/pmf for $X$ and $q(t|\theta)$ be pdf/pmf of $T(X)$ then $T(X)$ is a sufficient statistics for $\theta$ if $\forall x \in S$ 
$$
\frac{p(x|\theta)}{q(T(x)|\theta)}
$$
doesn't depend on $\theta$


## Factorization Theorem
Let $f(x|\theta)$ be pdf/pmf of $X$. $T(X)$ is a sufficient statistics of $\theta$ iff $\exists \space g(t|\theta)$ and $h(x)$ s.t. $\forall \space x,\theta$
$$
f(x|\theta) = g(T(x)|\theta)h(x)
$$

