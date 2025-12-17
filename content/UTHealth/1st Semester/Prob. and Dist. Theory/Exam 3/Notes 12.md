# Lecture 12: Bivariate Transformations

## 1 Basic Distribution Function Approach involving two r.v.




1. IfU=X−Y, find the p.d.f ofU
2. IfU= 2X−Y, find the p.d.f ofU.

## 2 Bivariate Transformations

$(U,V)$ is a function of $(X,Y)$. $(U,V) =g(X,Y)$ where $g:\mathbb{R}^2 →\mathbb{R}^2$ .Given the distribution of (X,Y), find the distribution of $(U,V)$.

### 2.1 First principles
Define $g^{-1} (B) =\{(x,y) :g(x,y)∈B\}$, for any set $B⊂\mathbb{R}^2$.  
Then,
$$
P((U,V)\in B) = P((X,Y)\in g^{-1}(B))
$$
Formula for joint density  
Suppose:

1. **(X,Y)** has a joint pdf $f_{X,Y}(x,y)$.
2. $g$ is 1-to-1 and “smooth” from $\mathbb{A}=\{(x,y) :fX,Y(x,y)> 0 \}$to $\mathbb{B}$ = image of $\mathbb{A}$ under the map $g=\{(u,v) : (u,v) =g(x,y) \text{ for some } (x,y)∈A\}$

Then $g$ has an inverse $h=g^{-1}$ and $h$ is also smooth.  
**Notation:** Let $g = (g_{1} ,g_{2})$ with $u=g_{1} (x,y)$ and $v=g_{2}(x,y)$ and $h= (h_{1} ,h_{2} )$ with $x=h_{1} (u,v)$ and $y=h_{2} (u,v)$  
**Result:** If 1 and 2 are true, then (U,V) has a joint pdf given by
$$
f_{U,V}(u,v) = f_{X,Y}(h_{1}(u,v),h_{2}(u,v)) \cdot |J|
$$
- for $(u,v)\in\mathbb{B}$
where $J$ is the Jacobian of the inverse transformation $h$. $|J|$ is the absolute value of $J$.

### 2.2 The Jacobian
$$
J = J(u,v) = \left|\frac{\partial(x,y)}{\partial(u,v)}\right| = \left|\begin{matrix}
\frac{\partial x}{\partial u} & \frac{\partial y}{\partial u} 
\\ \frac{\partial x}{\partial v} & \frac{\partial y}{\partial v} 

\end{matrix} \right | = \frac{\partial x}{\partial u} \left(\frac{\partial y}{\partial v} \right) - \frac{\partial y}{\partial u} \left(\frac{\partial x}{\partial v} \right)
$$

where $x=h_{1}(u,v)$, $y=h_{2}(u,v)$.  
Comments:

1. $f_{U,V}(u,v) = f_{X,Y}(h_{1}(u,v),h_{2}(u,v))|J|$ for $(u,v)\in \mathbb{B}$ is the "vector" version of $f_{Y}(y)=f_{X}(g^{-1}(y))\left| \frac{d}{dy}g^{-1}(y)\right|$ for $y\in Y$  
2. $f_{X,Y}(h_{1}(u,v),h_{2}(u,v))$ is simply $f_{X,Y}(x,y)$ re-expressed in terms of $u$ and $v$. Just replace $x$ and $y$ by expressions in terms of $u$ and $v$. 

### 2.3 Heuristic derivation of the density of $(U, V) =g(X, Y)$

Let $(u,v)$ be a particular point in the $(U,V)$ plane. Suppose the function $g$ maps $(x,y)$ to the point $(u,v)$ (so that $(x,y) =h(u,v)$ where $h=g^{-1}$ ). Let $A$ be a small (infinitesimal) region containing $(x,y)$. Suppose $g$ maps $A$ into the small region $B$ containing $(u,v)$.  
Then:
$$$P((x,y)\in A)=P((x,y)\in B)$$
- We also know:
$$P((x,y)\in A) \approx f_{X,Y}(x,y) \cdot Area(A) \text{ and } P((x,y)\in b) \approx f_{U,V}(u,v) \cdot Area(B)$$
and the approximations can be made as accurate as we please by making the areas sufficiently small.  
Equating the two expressions leads to
$$
f_{X,Y}(x,y) \cdot Area(A) = f_{U,V}(u,v)\cdot Area(B)
$$

so that
$$
f_{X,Y}(x,y) = f_{U,V}(u,v) \cdot \frac{Area(B)}{Area(A)}
$$

This ratio of areas is (in the limit of areas going to zero) just the absolute value of the Jacobian $|J(u,v)|$ of the inverse transformation $h$, which tells us the amount of contraction or expansion produced by the mapping $h$ at the point $(u,v)$.  

Thus we have:
$$
f_{U,V}(u,v) = f_{X,Y}(h(u,v)) \cdot |J(u,v)|
$$

as desired.

**Lemma:** If $f_{X,Y}(x,y) =cp(x)q(y)$ for $−∞< x <∞$ and $−∞< y <∞$, then $X$ and $Y$ are independent r.v.’s with marginal densities found by “normalizing” $p(x)$ and $q(y)$.  

**Lemma:** If the support of $f_{X,Y}(x,y)$ is a Cartesian product set, and on this support ,
$$
f_{X,Y}(x,y) =cp(x)q(y)
$$
then $X$ and $Y$ are independent.  

A more precise and detailed wording:  

**Lemma:** If 
$$
f_{X,Y}(x,y) = \begin{cases}
cp(x)q(x),  & (x,y)\in A \times B \\
0,  & otherwise
\end{cases}
$$then $X$ and $Y$ are independent, and
$$
\begin{align}
&f(X)(x) = ap(x) \text{ for }x\in A \\
&f(Y)(y) = bq(y) \text{ for }y\in B
\end{align}
$$
where $a,b$ are normalizing constants.

## 3 Distributions of Sums and Ratios

IfXandY have joint pdffX,Y(x,y), then  
1. $Z=X+Y$ has pdf
$$
f_{Z}(z) = \int_{-\infty}^{\infty}f_{X,Y}(x,z-x)dx
$$
2. $Z = \frac{Y}{X}$ has pdf
$$
f_{Z}(z) = \int_{-\infty}^{\infty}|x|f_{X,Y}(x,zx)dx
$$
When $X,Y$ are independent,


$$
\begin{align}
&f_{X,Y}(x,z−x) =f_{X}(x)f_{Y}(z−x) \\
&f_{X,Y}(x,zx) =f_{X}(x)f_{Y}(zx).

\end{align}
$$

In this case $1.$ is known as a ‘convolution integral’ or as the ‘convolution of two densities’.