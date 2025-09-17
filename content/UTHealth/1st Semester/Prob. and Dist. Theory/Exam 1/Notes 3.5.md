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
Let 
$$
\begin{align}
A_{1} = \{\text{1st letter "H"}\} \\
A_{2} = \{\text{1st letter "E"}\} \\
A_{3} = \{\text{1st letter "L"}\} \\
A_{4} = \{\text{1st letter "L"}\} \\
A_{5} = \{\text{1st letter "O"}\} \\
\end{align}
$$
then $P(A_{1}\cup A_{2}\cup A_{3}\cup A_{4}\cup A_{5})=P(A_{1})\cdot P(A_{2})\cdot P(A_{3})\cdot P(A_{4})\cdot P(A_{5})= (\frac{1}{26})^5$

- (#2) $P(\text{types BURP})$
You could get either
$$
\begin{align}
\_BURP \\
BURP\_
\end{align}
$$
then $\{\text{monkey typing BURP}\} = \{BURP\_{}\}\cup\{\_BURP\}=B_{1}\cup B_{2}$ where 
$$
\begin{align}
P(B_{1})=\left( \frac{1}{26} \right)\left( \frac{1}{26} \right)\left( \frac{1}{26} \right)\left( \frac{1}{26} \right)(1) = \left( \frac{1}{26} \right)^4 \\
P(B_{2})=\left( \frac{1}{26} \right)\left( \frac{1}{26} \right)\left( \frac{1}{26} \right)\left( \frac{1}{26} \right)(1) = \left( \frac{1}{26} \right)^4
\end{align}
$$
**Note:** $B_{1}$ and $B_{2}$ are disjoint so
$$
P(B_{1}\cup B_{2}) = P(B_{1})+P(B_{2}) = 2 \cdot \left( \frac{1}{26} \right)^4
$$
- (#3) $P(\text{types ZIT})$
You could either get
$$
\begin{align}
\_\space\_ZIT \\
\_ZIT\_ \\
ZIT\_\space\_
\end{align}
$$
**Note:** Same idea as #2, blanks can be anything so they are $\frac{26}{26}=1$. Also these events are still disjoint. Therefore
$$
P(C_{1}\cup C_{2}\cup C_{3}) = P(C_{1})+P(C_{2})+P(C_{3}) =3 \cdot\left( \frac{1}{26} \right)^3
$$
- (#4) $P(\text{types AAAA})$
You can either get
$$
\begin{align}
\_AAAA  \\
AAAA\_
\end{align}
$$
**Note:** these arent disjoint, see $\_AAAA \cap AAAA\_ = AAAAA$, therefore
$$
P(D_{1}\cup D_{2}) = P(D_{1})+P(D_{2})-P(D_{1}\cap D_{2}) = \left( \frac{1}{26} \right)^4 + \left( \frac{1}{26} \right)^4 - \left( \frac{1}{26} \right)^5
$$
- (#5) $P(\text{types AAA})$
You can either get
$$
\begin{align}
\_\space\_AAA  \\
\_AAA\_  \\
AAA\_\space\_ 
\end{align}
$$
Again see that these are disjoint, so you need to find all the pairwise intersections and triple intersections.
$$
\begin{align}
P(E_{1}\cup E_{2}\cup E_{3}) &= P(E_{1})+P(E_{2})+P(E_{3})  \\
&-P(E_{1}\cap E_{2})-P(E_{2}\cap E_{3})-P(E_{1}\cap E_{3}) \\
&+P(E_{1}\cap E_{2}\cap E_{3}) \\ \\

&=3 \cdot\left( \frac{1}{26} \right)^3 -2\cdot \left( \frac{1}{26} \right)^4
\end{align}
$$
- (#6) $P(\text{types AA})$
Same idea as above, its just long. 
$$
P(F_{1}\cup F_{2}\cup F_{3}\cup F_{4}) = 4 \cdot\left( \frac{1}{26} \right)^2  - 3 \cdot\left( \frac{1}{16} \right)^3 - \left( \frac{1}{26} \right)^4 + \left( \frac{1}{26} \right)^5
$$
- (#7) $P(\text{at least one A})$
$$
\begin{align}
&= 1-P(\text{No A's}) \\
&=1-\left( \frac{25}{26} \right)^5
\end{align}
$$

## 2 Conditional probability

#### $P(A∩B∩C) =P(A)\cdot P(B|A)\cdot P(C|A∩B)$ 

since the RHS can be written as
$$
=P(A) \cdot \frac{P(A\cap B)}{P(A)}\cdot \frac{P(A\cap B\cap C)}{P(A\cap B)}=P(A\cap B\cap C)
$$

And similarly


$P(A∩B∩C∩D) =P(A)\cdot P(B|A)\cdot P(C|A∩B)\cdot P(D|A∩B∩C)$


### 2.1 Urn models

An urn contains colored balls; each draw is equally likely among balls in the urn.

- **Sampling with replacement:** return the ball after each draw.
- **Sampling without replacement:** do not return the ball.
- **Polya urn:** after drawing a ball, replace it and add another ball of the same color.

Example. An urn has 7 red and 3 white balls. Draw 3 balls in sequence without replacement.  
Let $A_{i}=\{\text{ith ball is red}\}$. Then $P(\text{ 3 red balls})=P(A_{1}\cap A_{2}\cap A_{3})=P(A_{1})\cdot P(A_{2}|A_{1})\cdot P(A_{3}|A_{1}\cap A_{2})$
$$
= \left( \frac{7}{10} \right)\left( \frac{6}{9} \right)\left( \frac{5}{8} \right)
$$

The same problem with a Polya Urn:
$$
= \left( \frac{7}{10} \right)\left( \frac{8}{11} \right)\left( \frac{9}{12} \right)
$$
## 3 Examples for Law of Total Probability and Bayes’ Theorem

Situation. Four coins in a hat, numbered 1, 2, 3, 4. Upon choosing a coin at random (equally  
likely), we toss the same coin six times. Let $π_{i}$  be the probability of heads for coin $i$. The given  
values are  
$π_{1} = 0. 2 , π_{2} = 0. 4 , π_{3} = 0. 6 , π_{4} = 0. 8.$

### Preliminaries
$$
S = \{(i,r_{1},r_{2},r_{3},r_{4},r_{5},r_{6})\}: 1\leq i \leq 4, r_{t}\in\{H,T\}
$$
**Note:** Cardinality of $S$: $|S|=4 \cdot 2^6$, also they are not all equally likely. 

### Problem 1: Probability of exactly four heads

Let $A=\{\text{observe 4 heads in 6 tosses}\}$. Define $B_{i}=\{\text{choose coin i}\}$. $B_{1} ,B_{2} ,B_{3} ,B_{4}$ form a partition. By [[Notes 3#3 Law of Total Probability|law of total probability]] 
$$
\begin{align}
P(A)&=\sum_{i=1}^{4}P(B_{i})\cdot P(A|B_{i}) \\
&=\sum_{i=1}^{4}\left( \frac{1}{4} \right) \cdot {6 \choose 4}\cdot(\pi_{i})^4(1-\pi_{i})^2 \approx.1776
\end{align}
$$

### Problem 2: Probability of the coin given 4 heads

Suppose we observe 4 heads (in 6 tosses). What is the probability we have chosen coin $i$?

Given $A$, for $i=1,2,3,4$, use bayes theorem $P(B_{i}|A)$
$$
P(B_{i}|A)=\frac{P(B)\cdot P(A|B_{i})}{P(A)}
$$
**Note:** All $P(B_{i}|A)$ should sum to 1. 


