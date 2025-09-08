# Lecture 2: Basic Rules of Probability

Probability  
For each event A in the [[Notes 1#2.2 Sample spaces types|sample space]] $S$,

We want to associate with $A$ a # between 0 and 1 that we will call it the probability of $A$, denoted by $P(A)$
## 1 Sigma Algebra

A collection of subsets of $S$ is called a sigma algebra (or Borel field), denoted by $\mathcal{B}$, if it  
satisfies the following three properties:
1. $\emptyset \in \mathcal{B}$ 
2. $A\in \mathcal{B}\implies A^c\in\mathcal{B}$ (closed under complementation) 
3. $A_{1}, A_{2}, \dots \in \mathcal{B} \implies \bigcup_{i=1}^{\infty}\in \mathcal{B}$ (closed under countable unions)

### Properties of Sigma Algebra

- The empty set $\emptyset$ is a subset of any set. Thus $\emptyset \subset S$
- Since $S=\emptyset^c$, properties (1) and (2) imply that $S$ is always in $\mathcal{B}$.
- From DeMorgan’s Laws, $\mathcal{B}$ is closed under countable intersections.

$A_{1}, A_{2}, \dots \in \mathcal{B}$, then by property 2 of Borel fields, $A_{1}^c, A_{2}^c, \dots \in \mathcal{B}$. By [[Notes 1#2.4.4 De Morgan’s Laws|DeMorgans Law]], then $(\bigcup_{i=1}^{\infty}A_{i}^c)^c=\bigcap_{i=1}^{\infty}A_{i}$

Associated with sample space $S$ we can have many different sigma algebras. For example,  
the collection $\{\emptyset,S\}$ is a sigma algebra, usually called the **trivial sigma algebra**.

**Example: Sigma Algebra (finite or countable S)**

If the sample space S is finite or countable, we define:
$$
\mathcal{B}=\{\text{all subsets of S, including S itself}\}
$$

If S has $n$ elements, then there are $2^n$ sets in $\mathcal{B}$.

**Example:** Let $S=\{1,2,3\}$, the $\mathcal{B}=2^3=8$ sets
$$
\mathcal{B} = \big\{\{\emptyset\}, \{1\}, \{2\}, \{3\}, \{1,2\}, \{2,3\}, \{1,3\}, \{1,2,3\}\big\}
$$


**Example: Sigma Algebra (uncountable S)**
Let $S=(-\infty, \infty)$ then $\mathcal{B}$ is chosen to contain all sets of the following form. 
- $[a,b]$
- $(a,b]$
- $[a,b)$
- $(a,b)$
$\forall a,b\in \mathbb{R}$

Note: By properties of $\mathcal{B}$ contains all sets that can be formed by taking union/intersections of the sets

$\sigma$-algebra is a rule book for which events are legal to talk about in prob.
## 2 Axioms of Probability

Given a sample space $S$ and an associated sigma algebra $\mathcal{B}$, a **probability function** is a  
function $P$ with domain $\mathcal{B}$ that satisfies:
1. $P(A)\geq 0\space \forall A\in\mathcal{B}$ (Non-negativity)
2. $P(S) = 1$ (Normalization)
3. If $A_{1}, A_{2}, \dots \in \mathcal{B}$ are mutually exclusive, then $P\left( \bigcup_{i=1}^{\infty}A_{i} \right)=\sum _{i=1}^{\infty}P(A_{i})$ (Countable additivity)


Comments on the Axioms

- The properties above are called the **Axioms of Probability** (or the Kolmogorov  
    Axioms, after A. Kolmogorov, one of the fathers of probability theory).
- ANY function $P$ satisfying the axioms is called a probability function.
- The axiomatic definition makes no attempt to tell what particular function $P$ to choose,  
    it merely requires $P$ to satisfy the axioms.
- For any sample space many different probability functions can be defined. Which  
    one(s) reflects what is likely to be observed in a particular experiment is still to be  
    discussed.

**Example: Defining Probabilities**  
**Experiment:** Tossing fair coin. 
- "Fair" equally likely for heads or tails

$S=\{H,T\}$ 
$\sigma$-algebra = $\big\{\{\emptyset\}, \{H\}, \{T\}, \{HT\}\big\}$

"fair" $\implies$ $P(\{H\})=P(\{T\})$ 1. 
	by properties 2.) and 3.)

$P(\{H\}\cup\{T\})=P(\{H\})+ P(\{T\})=1$ 2. 

1.+2. $\implies$ $P(\{H\})=P(\{T\})=\frac{1}{2}$ 


## 3 Simple sample space

**Simple sample space:** A finite samples space where all the outcomes are equally likely.
- finite, equally likely
- Samples space = $\{e_{1}, e_{2}, \dots, e_{N}\}$
- Each $P(e_{i})=\frac{1}{N}$
- For each $A\subset S$: $P(A) = \frac{\text{\# of outcomes in A}}{N}$

**Example:** Rolling a dice. 

## 4 Some useful results

### 4.1 $P(\emptyset)=0$

To prove it: Proof by contradiction.
Assume $P(\emptyset) = a>0$ and let $A_{i}$ for $i = 1, 2, 3... , then

$\bigcup_{i=1}^{\infty} = \emptyset$, where $A_{i}\cap A_{j}= \emptyset$ for $i\not=j$ (meaning [[Notes 1#2.4.6 Disjoint sets|mutually exclusive]]) therefore

$$
P(\emptyset) = P\left( \bigcup_{i=1}^{\infty}A_{i} \right)=\sum_{i=1}^{\infty}P(A_{i}) = \sum_{i=1}^{\infty}a=\infty 
$$
This contradicts with finiteness of probability therefore $P(\emptyset)=0$ 

### 4.2 Complement rule: $P(A^c)=1-P(A)$
To prove it: Let $S=A\cup A^c$, also $A\cap A^c=\emptyset$ (mutually exclusive)
$$
P(S)=P(A\cup A^c)=P(A)+P(A^c)=1 
$$
by the [[Notes 2#2 Axioms of Probability|2nd axiom of probability]] then

$P(A^c)=1-P(A)$

### 4.3 Monotonicity: If $A\subset B$, then $P(A)\leq P(B)$.

To prove it: Let $B=A\cup(B\cap A^c)$ 
$$
P(B)=P(A\cup(B\cap A^c))=P(A)+P(B\cap A^c) 
$$
we know that $P(B\cap A^c)\geq 0$ by [[Notes 2#2 Axioms of Probability|1st axiom of probability]] So (removing it from equality above breaks equality) $P(A)\leq P(B)$

### 4.4 Boundedness of probability

For any event $A\subset S$:
$$
P(A)\leq P(S) = 1 \implies P(A)\leq 1
$$

### 4.5 Inclusion-exclusion

For two events $A$ and $B$: 
$$
P(A\cup B)=P(A)+P(B)-P(A\cap B)
$$

For three events $A$,$B$, and $C$:
$$
P(A\cup B\cup C)= P(A) + P(B) + P(C) -P(A\cap B) -P(B\cap C)-P(A\cap C)+P(A\cap B\cap C)
$$

### 4.6 Boole’s Inequality:

For a collection of events $A_{1}, A_{2}, \dots A_{n}$,
$$
P\left( \bigcup_{i=1}^{n}A_{i} \right)\leq \sum_{i=1}^{n}P(A_{i})
$$
### 4.7 Bonferroni’s Inequality:

$$
P(A\cap B)\geq P(A)+P(B)-1
$$


Reading: Sections 1.1–1.2 of your textbook




