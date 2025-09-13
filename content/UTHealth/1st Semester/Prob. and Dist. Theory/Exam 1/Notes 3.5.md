
|           | Without Replacement | With Replacement                           |
| --------- | ------------------- | ------------------------------------------ |
| Ordered   | $\frac{n!}{(n-r)!}$ | $n^r$                                      |
| Unordered | ${n \choose r}$     | ${n + r -1 \choose r}={n+r-1 \choose n-1}$ |
**Permutations of Repeated Elements:** $\frac{k!}{k_{1}!k_{2}!\dots k_{m}!}$
- "$k$ places with $m$ different numbers repeated $k_{1},k_{2},\dots ,k_{m}$ times, then the number of ordered samples is" - Statistical Inference

**Multinomial Theorem:** 
- The multinomial coefficients have a direct combinatorial interpretation, as the number of ways of depositing $n$ distinct objects into $m$ distinct bins, with $k_1$ objects in the first bin, $k_2$ objects in the second bin, and so on. 
$$
\frac{n!}{k_{1}!k_{2}!\dots k_{m}!}
$$ this is super helpful, its an alternative to Multiplication Rule

# Typical Idea
1. Define $A$
2. Find total number of combinations
3. Find number of combinations for set of interest ($A$)

$$
P(A)=\frac{\text{\# of favorable outcomes}}{\text{total}}
$$
**Note:** If you cant find all combinations easily, try manually finding all of them. This could be really hard in some cases, but a lot faster in other cases. 


**Important:** I need to figure out an easy way to understand how to calculate outcomes in group? Like the [[Notes 3|full house question]]. Cause sometimes its hard to know what values I need to multiply. 