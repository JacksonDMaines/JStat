# Lecture 11: Multivariate Expectation

## 1 Expectation of functions of multiple random variables

### 1.1 Definitions

**Definition:** Let $X_{1} ,...,X_{n}$ be discrete random variables with joint pdf $p$ and let $g$ be a real valued multivariate function defined over all possible values of($X_{1} ,...,X_{n}$). Then the expected value of $g(X_{1} ,...,X_{n})$ is defined to be
$$
E[g(X_{1} ,...,X_{n})] = \sum_{x_{1}\in S_{1}}\sum_{x_{2}\in S_{2}}\dots \sum_{x_{n}\in S_{n}}g(X_{1} ,...,X_{n}) \cdot p(X_{1} ,...,X_{n})
$$

**Definition** Let $X_{1} ,...,X_{n}$ be continuous random variables with joint pdf $f$ and let $g$ be a real valued multivariate function defined over all possible values of ($X 1 ,...,Xn$). Then the expected value of $g(X_{1} ,...,X_{n})$is defined to be
$$
E[g(X_{1} ,...,X_{n})] = \int_{-\infty}^{\infty}\int_{-\infty}^{\infty}\dots\int_{-\infty}^{\infty} g(X_{1} ,...,X_{n}) \cdot p(X_{1} ,...,X_{n})dx_{n}\dots dx_{1}
$$
### 1.2 Theorems
- As one might expect, our expectation theorems can be extended into multivariate expectation.  
**Theorem**  Let $X_{1} ,...,X_{n}$ be random variables and let $c$ be a real valued constant. Then
$$
E[c] = c
$$

**Theorem** Let $X_{1} ,...,X_{n}$ be random variables, let $c$ be a real valued constant and let $g$ be a real valued function defined over all possible values of ($X 1 ,...,Xn$). Then
$$
E[cg(x_{1},x_{2}, \dots , x_{n})] = c\cdot E[g(x_{1}, x_{2}, \dots,x_{n})]
$$

**Theorem** Let $X_{1} ,...,X_{n}$ be random variables and let $g_{1} ...g_{k}$ be real valued functions defined over all possible values of ($X_{1} ,...,X_{n}$). Then
$$
E\left[ \sum_{i=1}^{k}g_{i}(x_{1},x_{2}, \dots ,x_{n}) \right] = \sum_{i=1}^{k}E[g_{i}(x_{1},x_{2}, \dots ,x_{n})]
$$
- We also have a theorem for when the random variables are independent.  
**Theorem** Let $X_{1} ,X_{2}$ be random variables and let $g$ and $h$ be real values functions defined over the supports of $X_{1}$ and $X_{2}$ , respectively. If $X_{1}$ and $X_{2}$ are independent, then
$$
E[g(x_{1})h(x_{2})] = E[g(x_{1})]E[h(x_{2})]
$$

Here we will do the proof when $X_{1}$ and $X_{2}$ are continuous with joint PDF $f$ and marginal PDFs $f_{1}$ and $f_{2}$.
The proof when the random variables are discrete is similar
- **Note:** I think when you split expectation you now use marginal pdfs, see proof?
Proof.
$$
\begin{align}
E[g(x_{1})h(x_{2})] &= \int_{-\infty}^{\infty}\int_{-\infty}^{\infty}g(x_{1})h(x_{2})\cdot f(x_{1},x_{2})dx_{1}dx_{2} = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty}g(x_{1})h(x_{2})f_{1}(x_{1})f_{2}(x_{2})dx_{1}dx_{2}  \\
&=\int_{-\infty}^{\infty}g(x_{1})f_{1}(x_{1})dx_{1}\cdot \int_{-\infty}^{\infty}h(x_{2})f_{2}(x_{2})dx_{2} = E[g(x_{1})h(x_{2})] 
\end{align}
$$

## 2 Covariance

### 2.1 Motivation

- While the joint PDF of two random variables fully describes the relationship between two random variables, we would like to have a numerical measurement to summarize how closely related two random variables are.
- When two random variables are independent, there is no relationship between two random variables.
- Covariance is how we will numerically summarize how closely related two random variables are.

**Example** Suppose $X,Y$ are NOT independent. How can we measure the strength of their dependence? Make an ($x,y$) an consider how far it lies from ($μx,μy$)  

**Question:** Consider deviation$x−μx,y−μy$, $(x−μx)(y−μy)$

| Region | $x-\mu_{x}$ | $y-\mu_{y}$ | $(x−μx)(y−μy)$ |
| ------ | ----------- | ----------- | -------------- |
| I      | -           | +           | -              |
| II     | +           | +           | +              |
| III    | +           | -           | -              |
| IV     | -           | -           | +              |
$$
\begin{cases}
+ &I,IV \\
- &I, III
\end{cases}
$$
### 2.2 Definitions

- First we define the covariance of two random variables.  
**Definition** The covariance between random variables $X_{1}$ and $X_{2}$ is
$$
Cov(x_{1},x_{2}) = E\left[[x_{1}- E[x_{1}]]\cdot [x_{2}- E[x_{2}]] \right]
$$
 **Note:** 
- $Cov(X_{1},X_{1})=Var(X_{1})$
- $Cov(X,a)=0$
- $Cov(X,Y)=Cov(Y,X)$
- $Cov(aX,bY)=ab\cdot Cov(X,Y)$
- $Cov(X+a,Y+b)=Cov(X,Y)$
- $Cov(aX+bY,cW+dV)= ac\cdot Cov(X,W)+ad\cdot Cov(X,V)+bc\cdot Cov(Y,W)+bd\cdot Cov(Y,V)$ 
### 2.3 Theorems

- We have a few theorems to help make finding the covariance easier.
- Our first theorem is akin to our variance formula.  
**Theorem** Let $X_{2}$ and $X_{2}$ be random variables with finite first moments (i.e. $E[X_{1} ]$and $E[X_{2} ]$are real valued). Then
$$
Cov(x_{1},x_{2}) = E[x_{1}\cdot x_{2}] -E[x_{1}]E[x_{2}]
$$
Proof.
$$
\begin{align}
Cov(x_{1},x_{2})&=  E\left[[x_{1}- E[x_{1}]]\cdot [x_{2}- E[x_{2}]] \right] = E[x_{1}x_{2}-x_{1}E[x_{2}]-x_{2}E[x_{1}]+E[x_{1}]E[x_{2}]] \\
&= E[x_{1}x_{2}] -E[x_{1}]E[x_{2}] - E[x_{1}]E[x_{2}] + E[x_{1}]E[x_{2}]  \\
&= E[x_{1}\cdot x_{2}] -E[x_{1}]E[x_{2}]
\end{align}
$$

- Our second theorem relates to the relationship between independence and correlation.  
**Theorem** Let $X_{1}$ and $X_{2}$ be random variables with finite first moments (i.e. $E[X_{1} ]$ and $E[X_{2} ]$are real valued). If $X_{1}$ and $X_{2}$ are independent, then
$$
Cov(x_{1},x_{2}) = 0 
$$
Proof.
$$
\begin{align}
Cov(x_{1},x_{2}) &= E[x_{1}\cdot x_{2}] -E[x_{1}]E[x_{2}] =  \\
&= E[x_{1}]\cdot E[x_{2}] - E[x_{1}]\cdot E[x_{2}] = 0
\end{align}
$$
- The converse of above Theorem is not true!


### 2.4 Correlation Coefficient

$|Cov(X,Y)|$ indicate strength of dependence. But, the value could be quite large if units of measurement are large, even if association is weak.

```
X= Height, Y = Weight
Xin feet, Y in lbs (1)
Xin inches, Y in ozs (2)
```

**Definition** The ***correlation coefficient*** between random variables $X_{1}$ and $X_{2}$ is:
$$
\rho(X,Y) = \frac{Cov(x,y)}{\sqrt{ Var(x)\cdot Var(y) }}
$$
Properties of $ρ(X,Y)$:

1. $− 1 ≤ρ(X,Y)≤ 1$
2. If $|ρ|$ is close to $1$, then strong correlation.
3. If $|ρ|= 0$⇔**No correlation.**(But, could still be dependent.)
4. $ρ > 0 ⇔Cov(X,Y)> 0 ⇔X↑,Y ↑, X↓,Y ↓$  
	1. $ρ < 0 ⇔Cov(X,Y)< 0 ⇔X↑,Y ↓, X↓,Y ↑$
5. If $X^*=\frac{X-\mu _{x}}{\sigma_{X}}$, $Y^*=\frac{Y-\mu_{y}}{\sigma_{Y}}$  
$$
\rho(X,Y) = Cov(X^*,Y^*)
$$
$$
\begin{align}
Cov(x^*, y^*) &= E[x^*y^*]-E[x^*]E[y^*] = E\left[ \frac{x-\mu_{x}}{\sigma _{x}} \cdot  \frac{y-\mu_{y}}{\sigma _{y}} \right] -E\left[\frac{x-\mu_{x}}{\sigma _{x}}\right]E\left[\frac{y-\mu_{y}}{\sigma _{y}}\right]  \\
&=  \frac{E\left[[x- E[\mu_{x}]]\cdot [y- E[\mu_{y}]] \right]}{\sigma_{x}\cdot \sigma_{y}} = \frac{Cov(x,y)}{\sigma_{x}\sigma_{y}} = \rho(X,Y)
\end{align} 
$$
6. $|ρ|= 1⇔Y=aX+b$ ,$a,b$ constants, i.e. perfect linear association between $X,Y$

## 3 Expectation of Linear Combinations

### 3.1 Motivation

- Next we will cover the expectation, variance and covariance of random variables that are actually the linear combination of other random variables.
- This is useful because we often combine measurements into a summary measurement (for example, the sample mean).

### 3.2 Theorems

- All of these theorems will be based on  
$$
U_{x} = \sum_{i=1}^{n}a_{i}X_{i} \text{ and }U_{y}=\sum_{j=1}^{m}b_{j}Y_{j}
$$
where $X_{1} ,...,X_{n}$ and$Y_{1} ,...,Y_{m}$ are random variables and $a_{1} ,...,a_{n}$, $b_{1} ,...,b_{m}$ are all real valued constants

- Expectation
- Variance
$$
V[U_{x}]= \sum_{i=1}^{n}a_{i}^2V[X_{i}] + 2 \sum_{i=1}^{n-1}\sum_{j=i+1}^{n}a_{i}a_{j}Cov(X_{i},X_{j})
$$
Or, Equivalently
$$
V[U_{x}]= \sum_{i=1}^{n}a_{i}^2V[X_{i}] + 2 \sum\sum_{1\leq i<j\leq n}a_{i}a_{j}Cov(X_{i},X_{j})
$$

Or, Equivalently
$$
V[U_{x}]= \sum_{i=1}^{n}a_{i}^2V[X_{i}] + 2 \sum_{i=1}^{n}\sum_{j=1,i
 \not=j}^{n}a_{i}a_{j}Cov(X_{i},X_{j})
$$


Proof.
$$
\begin{align}
Var(U_{x}) &= E[(U_{x}-E[U_{x}])^2] = E\left[ \left( \sum_{i=1}^n a_{i}x_{i} - \sum_{i=1}^{n}a_{i}\mu_{i} \right)^2 \right] = E\left[ \left( \sum_{i=1}^n a_{i}(x_{i}-\mu_{i})\right)^2 \right]  \\
&= E\left[ \sum_{i=1}^n \sum_{j=1}^n a_{i}a_{j}(x_{i}-\mu_{i})(x_{j}-\mu_{j})\right]  \\
&= \sum_{i=1}^n a_{i}^2E[(x_{i}-\mu_{i})^2] + \sum_{i=1}^n\sum_{j=1}^na_{i}a_{j}E[(x_{i}-\mu_{i})(x_{j}-\mu_{j})] \\
&= \sum_{i=1}^n a_{i}^2Var(x_{i}) + \sum_{i=1}^n \sum_{j=1,i\not=1}^na_{i}a_{j}Cov(x_{i},x_{j})
\end{align}
$$
Proof.
$$
Cov[U_{x},U_{y}] = \sum_{i=1}^{n}\sum_{j=1}^{m}a_{i}b_{j}Cov[X_{i},Y_{j}]
$$
$$
\begin{align}
Cov(U_{x},U_{y}) &= E[(U_{x}-E[U_{x}])(U_{y}-E[U_{y}])] \\
& = E\left[ \left( \sum_{i=1}^na_{i}x_{i} - \sum_{i=1}^na_{i}\mu_{i} \right)\left( \sum_{j=1}^mb_{j}y_{j} - \sum_{j=1}^mb_{j}\mu_{j} \right) \right]  \\
&= E\left[ \sum_{i=1}^na_{i}(x_{i}-\mu_{xi}) \cdot \sum_{j=1}^m  b_{j}(y_{j}-\mu_{yj}) \right] \\
& = \sum_{i=1}^n\sum_{j=1}^ma_{i}b_{j}E[(x_{i}-\mu_{xi})(y_{j}-\mu_{yj})] = \sum_{i=1}^n\sum_{j=1}^ma_{i}b_{j}\cdot Cov(x_{i},y_{j})
\end{align}
$$
## 4 Conditional Expectation

### 4.1 Motivation

- Here we formally introduce the concept of conditional expectation, and some related theorems.
- The concept is really just recognizing that the conditional distribution is itself a distribution.

### 4.2 Definitions

- The definition of the conditional expectation for discrete random variables is as follows:  
**Definition** Let $X_{1}$ and $X_{2}$ be discrete random variables where the conditional distribution of $X_{1} |X_{2} =x_{2}$ is $p_{1 | 2} (x_{1} |x_{2} )$, and let $g$ be a real valued function defined for all possible values of $X_{1} |X_{2} =x_{2}$. Then the conditional expectation of $g(X_{1} )|X_{2} =x_{2}$ is
$$
E[g(X_{1})|X_{2}=x_{2}] = \sum_{x_{1}\in S_{i}}g(x_{1})\cdot P_{1|2}(x_{1}|x_{2})
$$
- And the definition of the conditional expectation for continuous random variables is as follows:  
Definition Let $X_{1}$ and $X_{2}$ be continuous random variables where the conditional distribution of $X_{1} |X_{2} =x_{2}$ is $f_{1 | 2} (x_{1} |x_{2})$, and let $g$ be a real valued function defined for all possible values of $X_{1} |X_{2} =x_{2}$. Then the conditional expectation of $g(X_{1} )|X_{2} =x_{2}$ is
$$
E[g(x_{1})|X_{2}=x_{2}] = \int_{-\infty}^{\infty}g(x_{1})\cdot f_{1|2}(x_{1}|x_{2})dx_{1}
$$

### 4.3 Theorems

- Here we introduce some theorems related to conditional expectations.  
**Theorem** Let $X_{1}$ and $X_{2}$ be random variables and let $g$ be a real valued function defined for all possible values of $X_{1}$ , then  
$$
E[g(X_{1} )] =E[E[g(X_{1} )|X-2 =x_{2}]]
$$  
Proof.  
$$
\begin{align}
E[g(x_{1})] &= \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x_{1})\cdot f(x_{1},x_{2})dx_{1}dx_{2} = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x_{1})\cdot f_{1|2}(x_{1},x_{2})\cdot f_{2}(x_{2})dx_{1}dx_{2} \\
&=\int_{-\infty}^{\infty}\left[\int_{-\infty}^{\infty}g(x_{1})\cdot f_{1|2}(x_{1},x_{2})dx_{1} \right]f_{2}(x_{2})dx_{2}  \\
&= \int_{-\infty}^{\infty} E[g(X_{1})|X_{2}=x_{2}]\cdot f_{2}(x_{2})dx_{2} = E[E[g(X_{1})|X_{2}=x_{2}]]
\end{align}
$$
- Here we present the proof when $X_{1}$ and $X_{2}$ are continuous. The proof is similar when $X_{1}$ and$X_{2}$ are discrete.
- Conditional variance is defined in a similar fashion to conditional mean.  
**Definition** $X_{1}$ and $X_{2}$ are two random variables, the conditional variance of $X_{1}$ given $X_{2} =x_{2}$ is
$$
V[X_{1} |X_{2} =x_{2} ] =E[X^2_{1} |X_{2} =x_{2} ]−(E[X_{1} |X_{2} =x_{2} ])^2  
$$
**Theorem** Let $X_{1}$ and $X_{2}$ be random variables and let $g$ be a real valued function defined for all possible values of $X_{1}$ , then
$$
V[g(X_{1} )] =E[V[g(X_{1} )|X_{2} =x_{2} ]] +V[E[g(X_{1} )|X_{2} =x_{2} ]].
$$
Proof.
$$
\begin{align}
Var(g(X_{1})) &= E[g(x_{1})^2]-E[g(x_{1})]^2 = E\left[E[g(x_{1})^2|X_{2}=x_{2}]\right] - E[E[g(x_{1})|X_{2}=x_{2}]]^2 \\
&= E\left[E[g(x_{1})^2|X_{2}=x_{2}]\right] - E[E[g(x_{1})|X_{2}=x_{2}]]^2 + E[E[g(x_{1})|X_{2}=x_{2}]^2]- E[E[g(x_{1})|X_{2}=x_{2}]^2] \\
&= E[E[g(x_{1})^2|X_{2}=x_{2}]- E[g(x_{1})|X_{2}=x_{2}]^2] + \Big[E[E[g(x_{1})|X_{2}=x_{2}]^2]- E[E[g(x_{1})|X_{2}=x_{2}]]^2\Big]  \\
&= E[V[g(X_{1} )|X_{2} =x_{2} ]] +V[E[g(X_{1} )|X_{2} =x_{2} ]]
\end{align}
$$
### 4.4 Useful Facts

1. $f_{X,Y}(x,y) =f_{X}(x)f_{Y|X}(y|x)$
2. $E(E(Y|X)) =E[Y]$
3. $Var(Y) =E(Var(Y|X)) +Var(E(Y|X))$

Interpretation of (2) and (3):

- $E(Y|X=x)$ is a function of $x$.
- $E(Y|X)$ is a random variable which is a function of the r.v. $X$
- $Var(Y|X=x)$ is a function of $x$.
- $Var(Y|X)$ is a random variable which is a function of the r.v. $X$
## 5 Bivariate Normal Distribution

- Let $−∞< μ_{x}<∞,−∞< μ_{y}<∞,σ_{x},σ_{y}>0$, and$− 1 < ρ <1$ be five real numbers. The bivariate normal pdf with means $μ_{x}$ and μ_y, variance $σ^2_{x}$and $σ_{y}^2$ and correlation $ρ$ is the bivariate pdf given by  
$$
f(x,y) = \left(2\pi \sigma_{x}\sigma_{y}\sqrt{ 1-\rho^2 }\right)^{-1} \times \exp\left( - \frac{1}{2(1-\rho^2)}\left( \left( \frac{x-\mu_{x}}{\sigma_{x}} \right)^2 - 2\rho\left(  \frac{x-\mu_{x}}{\sigma_{x}} \right)\left(  \frac{x-\mu_{y}}{\sigma_{y}} \right) + \left( \frac{y - \mu_{y}}{\sigma_{y}} \right)^2 \right) \right)
$$

- Properties of this distribution
1. The marginal distribution of $X$ is $N(μ_{x},σ^2_{x})$.
2. The marginal distribution of $Y$ is $N(μ_{y},σ^2_{y})$.
3. The correlation between $X$ and $Y$ is $ρ$
4. For any constants $a$ and $b$, the distribution of $aX+bY$ is $N(aμ_{x}+bμ_{y},a^2 σ_{x}^2 + 2abρσ_{x}σ_{y}+b^2 σ_{y}^2 )$
5. Conditional distribution $Y|X=x$ is $N(μ_{y}+ρ\frac{\sigma_{y}}{\sigma_{x}}(x−μ_{y}),σ^2_{y}(1−ρ^2 ))$
6. Conditional distribution $X|Y =y$ is $N(μ_{x}+ρ\frac{\sigma_{x}}{\sigma_{y}}(y−μ_{x}),σ_{x}^2 (1−ρ^2 ))$
