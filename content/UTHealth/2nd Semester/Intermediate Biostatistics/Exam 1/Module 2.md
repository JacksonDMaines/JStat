# Random Vars/ Binomial Dist.
R.V.: Variable that takes numeric quantity that depends on the outcome of a random event

**Expected Value of discrete R.V.**
$$
E[X] = \sum x\cdot P(X=x)
$$
- Weighted averages of expected values 
**Variance value of discrete R.V.**
$$
Var(X) = \sum(X-E[X])^2\cdot P(X=x)
$$
- How far data is from expected point

**Properties of Expectation/Variance**
- $E[aX+bY] = aE[X] + bE[Y]$

When X is independent to Y
$$
Var(aX+bY) = a^2Var(X) + b^2Var(Y)
$$
When X is dependent to Y
$$
Var(aX+bY) = a^2Var(X) + b^2Var(Y) + 2ab\cdot Cov(X,Y)
$$


**Alternate form of Variance:**
$$
Var(X) = E[X^2] -E[X]^2
$$
