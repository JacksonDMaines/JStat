# Chapter 1

## Definition 1.1.1
The set, $S$, of all possible outcomes of a particular experiment is called the *sample space* for the experiment.

## Definition 1.1.2
An *event* is any collection of possible outcomes of an experiment that is, any subset of $S$ (including $S$ itself).

## Theorem 1.14
For any three events $A,B,C$ defined on samples space $S$
- a.) Commutativity: 
	- $A\cup B=B\cup A$
	- $A\cap B=B\cap A$ 
- b.) Associativity: 
	- $A\cup(B\cup C)=(A\cup B)\cup C$
	- $A\cap(B\cap C)=(A\cap B)\cap C$ 
- c.) Distributive Laws
	- $A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$
	- $A\cup(B\cap C)=(A\cup B)\cap(A\cup C)$
- d.) DeMorgan's Laws
	- $(A\cup B)^c=A^c\cap B^c$
	- $(A\cap B)^c=A^c\cup B^c$

## Definition 1.1.5
Two events $A$ and $B$ are disjoint (or mutually exclusive) if $A\cap B=\emptyset$.The events $A_{1},A_{2,\dots}$ are pairwise disjoint (or mutually exclusive) if $A_{i}\cap A_{j}=\emptyset$   $\forall i \neq j$

## Definition 1.1.6
If $A_{1},A_{2},\dots$ are pairwise disjoint and $\bigcup_{i=1}^{\infty}A_{i}=S$, then the collections $A_{1},A_{2},\dots$ forms a partition of $S$. 
	Note: $S$ is the Sample space.

## Definition 1.2.1 
A collection of subsets of $S$ is called a *sigma algebra* (or *Borel field*), denoted by $\mathbb{B}$, if it satisfies the following properties:
- a.) $\emptyset\in\mathbb{B}$
- b.) if $A\in\mathbb{B}$, then $A^c\in \mathbb{B}$
	- $\mathbb{B}$ is closed under complementation
- c.) If $A_{1},A_{2},\dots\in\mathbb{B}$, then $\bigcup_{i=1}^{\infty}A_{i}\in\mathbb{B}$
	- $\mathbb{B}$ is closed under countable unions

## Definition 1.2.4
Given a sample space $S and an associated sigma algebra $\mathbb{B}$, a probability function is a function $P$ with domain $\mathbb{B}$ that satisfies
1.  $P(A)\geq 0$ for all $A\in\mathbb{B}$
2.  $P(S)=1$
3.  If $A_{1},A_{2},\dots\in\mathbb{B}$ are pairwise disjoint, then$P\left( \bigcup_{i=1}^{\infty}A_{i} \right)=\sum_{i=1}^{\infty}P(A_{i})$.

## Theorem 1.2.6
Let $S=\{s_{1,\dots,S_{n}}\}$ be a finite set. Let $\mathbb{B}$ be any sigma algebra of subsets of $S$. Let $p_{1},..,p_{n}$ be nonnegative numbers that sum to 1. For any $A\in\mathbb{B}$ define $P(A)$ by
$$
P(A)=\sum_{\{i:s_{i}\in A\}}p_{i}
$$
(The sum over an empty set is defined to be 0) Then $P$ is a probability function on $\mathbb{B}$. This remains true if $S=\{s_{1}, s_{2},\dots \}$ is a countable set.

## Axiom of Finite Additivity
If $A\in \mathbb{B}$ and $B \in \mathbb{B}$ are disjoint, then $P(A\cup B)=P(A) + P(B)$


## Theorem 1.2.8
If P is a probability function and $A$ is any set of $\mathbb{B}$, then
- a.) $P(\emptyset)=0$
- b.) $P(A)\leq 1$
- c.) $P(A^c)=1-P(A)$

## Theorem 1.2.9
If $P$ is a probability function and $A$ and $B$ are any sets in $\mathbb{B}$, then 
- a.) $P(B\cap A^c)=P(B)-P(A\cap B)$
- b.) $P(A\cup B)=P(A)+P(B)-P(A\cap B)$
- c.) If $A\subset B$, then $P(A)\leq P(B)$

## Theorem 1.2.11 
If $P$ is a probability function, then
- a.) $P(A)=\sum_{i=1}^{\infty}P(A\cap C_{i})$ for any partition $C_{1},C_{2},\dots$
- b.) $P\left( \bigcup_{i=1}^{\infty}A_{i}\leq \sum_{i=1}^{\infty}P(A_{i}) \right)$ for any set$A_{1},A_{2},\dots$
	- Boole's Inequality

## Theorem 1.2.14
If a job consists of $K$ separate tasks, the ith of which can be done in $n_{i}$ ways, $i=1,\dots ,k$, then the entire jobs can be done in $n_{1} \times n_{2} \times \dots \times n_{k}$ ways 


## Table 1.2.1

|               | Without Replacement | With Replacement  |
| ------------- | ------------------- | ----------------- |
| **Ordered**   | $\frac{n!}{(n-r)!}$ | $n^r$             |
| **Unordered** | $n \choose r$       | $n+r-1 \choose r$ |


## Definition 1.3.2 
If $A$ and $B$ are events in $S$, and $P(B) > 0$, then the conditional probability of $A$ given $B$, written $P(A|B)$ is 
$$
P(A|B) = \frac{P(A\cap B)}{P(B)}
$$
Some alternative forms
$$
\begin{aligned}
P(A\cap B) = P(A|B)P(B) \\
P(A\cap B)=P(B|A)P(A) \\
P(A|B)=P(B|A)\frac{P(A)}{P(B)}
\end{aligned}
$$

## Theorem 1.3.5
**Bayes' Rule** Let $A_{1},A_{2,\dots}$ be a partition of the sample space, and let $\mathbb{B}$ be any set. Then, for each $i=1,2,\dots$
$$
P(A_{i}|B)=\frac{P(B|A_{i})P(A_{i})}{\sum_{j=1}^{\infty}P(B|A_{j})P(A_{j})}
$$

## Definition 1.3.7
Two events, $A$ and $B$, are statistically independent if 
$$
P(A\cap B)=P(A)P(B)
$$

## Definition 1.3.9
If $A$ and $B$ are independent events, then the following pairs are also independent:
- a.) $A$ and $B^c$
- b.) $A^c$ and $B$
- c.) $A^c$ and $B^c$


## Definition 1.3.12
A collection of events $A_{1},\dots,A_{n}$ are mutually independent if for any subcollection $A_{i_{1}}, \dots, A_{i_{k}}$, we have 
$$
P\left( \bigcap _{j=1}^{k} A_{i_{j}} \right)=\prod_{j=1}^{k}P(A_{i_{j}})
$$

## Definition 1.4.1 
A random variable is a function from a sample space $S$ into the real numbers

## Definition 1.5.1
The cumulative distribution function or cdf of a random variable $X$, denoted by $F_{X}(x)$, is defined by
$$
F_{X}(x)=P_{X}(X\leq x), \space \forall x

$$

## Def page 29
