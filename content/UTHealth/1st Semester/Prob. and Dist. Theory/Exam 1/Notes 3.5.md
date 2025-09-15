# Further comments and applications on rules of probability

## 1 Unions, inclusion–exclusion
$$
\begin{align} 
&(1)\space P(A\cup B)=P(A)+P(B)-P(A\cap B) \\ \\
&(2)\space P\left( \bigcup_{i=1}^{k}A_{i} \right)\leq \sum_{i=1}^{k}P(A_{i})
\end{align} 
$$

**Proof of (2):**
- For $k=2$, $(2)$ becomes $P(A\cup B)\leq P(A)+P(B)$ follow immediately from $(1)$, because $P(A\cap B)\geq 0$ 
- For $k=2$, $P(A\cup B\cup C)=P((A\cup B)\cup C)\leq P(A\cup B)+P(C)\leq P(A)+P(B)+P(C)$ 
- For $k=4$, $P(A\cup B\cup C\cup D)=P((A\cup B\cup C)\cup D)\leq P(A\cup B\cup C) + P(D)\leq P(A)+P(B)+P(C)+P(D)$
- $\vdots$
- by induction you get $(2)$



### 1.1 Application of : $P\left( \bigcup_{i=1}^{k}A_{i} \right)\leq \sum_{i=1}^{k}P(A_{i})$

**A Multiple Comparison Procedure**

Suppose a researcher (Ed) wishes to design an experiment to compare $k$ treatments with a control  
(placebo). Take $k= 5$ for simplicity. After conducting the experiment, Ed will draw conclusions  
about the effectiveness of the treatments.

Suppose that none of the treatments are effectiveness; they are all equivalent to the control. (Of  
course, Ed doesn’t know this.)

Let $A_{i}={\text{Ed falsely claim treatment i is better than control}}$. Define $B=⋃_{i=1}^{5}A_{}i$(i.e., Ed has  
at least one false claim).

Apparently, $B$ is the event that Ed makes an error. Suppose Ed wishes the probability of an error  
to be at most 0.05. How can he accomplish this?
	- Answer 1: If experiment is designed so that $P(A_{i})=.001$, then $P(B)=P\left( \bigcup_{i=1}^{5}A_{i} \right)\leq \sum_{i=1}^{5}P(A_{i})=.05$
### 1.2 Principle of Inclusion–Exclusion

$P(A∪B) = P(A)+P(B)−P(A∩B)$ is the simplest case of the Principle of Inclusion–Exclusion

The next case $k= 3$:
$$
P(A\cup B\cup C)=P(A)+P(B)+P(C) - P(A\cap B)-P(B\cap C)+P(A\cap B\cap C)
$$

The general case:
$$
 \begin{align} P\left( \bigcup_{i=1}^{k}A_{i} \right) = \sum_{i=1}^{k}P(A_{i})
& - \sum_{i<j}P(A_{i}\cap A_{j})  \\
&+ \sum_{i<j<l}P(A_{i}\cap A_{j}\cap A_{l})  \\
&+ \dots - \dots +  \\
&\vdots \\
&+ (-1)^{k-1}P(A_{1}\cap A_{2}\cap \dots \cap A_{k})
\end{align} 
$$


There is a “picture proof” of the case withk= 3 where you keep track of how many times each  
region in the Venn diagram gets counted. (Do it!)

Proof fork= 3.

$$
\begin{align}
P(A\cup B\cup C) &= P((A\cup B)\cup C) \\
&=P(A\cup B)+P(C)-P((A\cup B)\cap C) \\
&=P(A) + P(B) - P(A\cap B) + P(C) - P((A\cap C)\cup(B\cap C)) \\
&=P(A)+P(B)+P(C) - P(A\cap B)-P(A\cap C)-P(B\cap C) + P((A\cap C)\cap (A\cap B)) \\
&=P(A)+P(B)+P(C) - P(A\cap B)-P(A\cap C)-P(B\cap C) +P(A\cap B\cap C)
\end{align}
$$


### 1.3 Applications of Inclusion–Exclusion

A monkey types 5 letters at random (independent keystrokes; each letter equally likely with prob.
$1/26$, so all $26^5$ sequences are equally likely).


- (#1) $P(\text{types HELLO})$

- (#2) $P(\text{types BURP})$

- (#3) $P(\text{types ZIT})$

- (#4) $P(\text{types AAAA})$

- (#5) $P(\text{types AAA})$

- (#6) $P(\text{types AA})$

- (#7) $P(\text{at least one A})$


## 2 Conditional probability

#### $P(A∩B∩C) =P(A)\cdot P(B|A)\cdot P(C|A∩B)$ 

since the RHS can be written as

and we can cancel terms.

And similarly


$P(A∩B∩C∩D) =P(A)\cdot P(B|A)\cdot P(C|A∩B)\cdot P(D|A∩B∩C)$


### 2.1 Urn models

An urn contains colored balls; each draw is equally likely among balls in the urn.

- **Sampling with replacement:** return the ball after each draw.
- **Sampling without replacement:** do not return the ball.
- **Polya urn:** after drawing a ball, replace it and add another ball of the same color.

Example. An urn has 7 red and 3 white balls. Draw 3 balls in sequence without replacement.  
Let $A_{i}=\{\text{ith ball is red}\}$. Then

The same problem with a Polya Urn:

## 3 Examples for Law of Total Probability and Bayes’ Theorem

Situation. Four coins in a hat, numbered 1, 2, 3, 4. Upon choosing a coin at random (equally  
likely), we toss the same coin six times. Let $π_{i}$  be the probability of heads for coin $i$. The given  
values are  
$π_{1} = 0. 2 , π_{2} = 0. 4 , π_{3} = 0. 6 , π_{4} = 0. 8.$

### Preliminaries

### Problem 1: Probability of exactly four heads

Let $A=\{\text{observe 4 heads in 6 tosses}\}$. Define $B_{i}=\{\text{choose coin i}\}$. $B_{1} ,B_{2} ,B_{3} ,B_{4}$ form a partition.

### Problem 2: Probability of the coin given 4 heads

Suppose we observe 4 heads (in 6 tosses). What is the probability we have chosen coin $i$?