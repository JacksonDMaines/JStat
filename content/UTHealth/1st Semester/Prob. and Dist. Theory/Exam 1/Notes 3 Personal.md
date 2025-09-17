
|           | Without Replacement | With Replacement                           |
| --------- | ------------------- | ------------------------------------------ |
| Ordered   | $\frac{n!}{(n-r)!}$ | $n^r$                                      |
| Unordered | ${n \choose r}$     | ${n + r -1 \choose r}={n+r-1 \choose n-1}$ |
**Permutations of Repeated Elements:** $\frac{k!}{k_{1}!k_{2}!\dots k_{m}!}$
- "$k$ places with $m$ different numbers repeated $k_{1},k_{2},\dots ,k_{m}$ times, then the number of ordered samples is" - Statistical Inference

**Multinomial Theorem:** 
- The multinomial coefficients have a direct combinatorial interpretation, as the number of ways of depositing $n$ distinct objects into $m$ distinct bins, with $k_1$ objects in the first bin, $k_2$ objects in the second bin, and so on. 

$$
\frac{n!}{k_{1}!k_{2}!\dots k_{m}!} = {n \choose k_{1}}\cdot {n-k_{1} \choose k_{2}}\cdot {n-k_{1}-k_{2} \choose k_{3}}\cdot \dots \cdot {n-k_{1}-k_{2}-\dots - k_{m-1} \choose k_{m}}
$$
this is super helpful, its an alternative to Multiplication Rule
- **Note:** The last term of the expanded version should just be ${k_{m} \choose k_{m}}=1$


### Theorem 1.2.14
If a jobs consists of k separate tasks, the $ith$ of which can be done is $n_i$ ways, $i=1,\dots,k$, then the entire job can be done in $n_{1}\times n_{2} \times\dots \times n_{k}$ ways. 
- Same as [[Notes 3#1.2 Fundamental Theorem of Counting|Fundamental Theorem of Counting]] 


# Typical Idea
1. Define $A$
2. Find total number of combinations
3. Find number of combinations for set of interest ($A$)

$$
P(A)=\frac{\text{\# of favorable outcomes}}{\text{total}}
$$

**Note:** If you cant find all combinations easily, try manually finding all of them. This could be really hard in some cases, but a lot faster in other cases. 

**Note:** This is really only useful when the events are all equally likely.


**Question:** I need to figure out an easy way to understand how to calculate outcomes in group? Like the [[Notes 3|full house question]]. Cause sometimes its hard to know what values I need to multiply. 
- **Answer:** Because of [[Notes 3 Personal#Theorem 1.2.14|Theorem 1.2.14]] or [[Notes 3#1.2 Fundamental Theorem of Counting|Fundamental Theorem of Counting]] 


# Stars and Bars
## No Minimum
$$
{n+k-1 \choose k-1}
$$
- How to organize $n$ items in $k$ number of bins, with no minimum for any bin.
## Minimum
$$
{n-1 \choose k-1}
$$
- How to organize $n$ items in $k$ number of bins such that each bin as at least 1 item. 
- Pretty sure this scales, like ${n-2 \choose k-2}$ would be ways to organize $n$ items into $k$ bins such that each bin gets at least 2 items.
- **Note:** This is pretty much the same thing as **No Minimum**, ${n-1 \choose k-1}={(n-k\cdot min)+k-1 \choose k -1}$

## Maximum 

yea idk. ill need to ask.


### Question: You have 7 balls and 4 urns. You randomly place each ball into an urn. What is the prob. each urn has at most 2 balls? 

##### Answer: 
- Total number of ways to organize 7 balls in 4 urns: ${7+ 4 -1 \choose 4-1}= 120$ 
- Ways to arrange 7 balls into 4 urn s.t. each urn has at most 2: 
	- The only options is that 3 urns have 2 balls and 1 urn has 1 ball. 
	- So its just how can you arrange that one ball? 4 different ways.?  

$$
= \frac{4}{{7+ 4 -1 \choose 4-1}}=\frac{4}{120}=\frac{1}{30}
$$

### Question: You have 13 balls and 4 urns. You randomly place each ball into an urn. What is the prob. each urn has at most 5 balls? 

### Answer: 
 - Total number of ways to organize 13 balls into 4 urns: ${13 + 4 -1 \choose 4-1}=560$
 - Ways to arrange 13 balls into 4 urns s.t. each urn as at most 5 balls. 
	 - Might be easier to find complement here?
		 - So 13 balls into 4 urns s.t. at least one urn as at least 6 balls? 

Let $x_{i} =6 + y$ for some $y=0,\dots,7$, then
$$
\begin{align}
&x_{i}+x_{j}+x_{k}+x_{l}= 13  \\
&\implies 7+y+x_{j}+x_{k}+x_{l}=13 \\
 & \implies y +x_{j}+x_{k}+x_{l}= 7
\end{align}
$$
so the number of ways to arrange 13 balls into 4 urns s.t. each urn as at least 6 balls is 
$$
4\cdot {7+4-1 \choose 4-1} = 4 \cdot {10 \choose 3} = 480
$$
 
Take the complement of this with the total $560 - 480 = 80$, therefore
$$
= \frac{80}{560}?
$$
I think this is right.