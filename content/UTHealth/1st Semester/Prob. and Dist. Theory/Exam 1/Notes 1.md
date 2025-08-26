# Lecture 1: Basic Set Theory and Its Operations

## 1 Why study probability?

In science, we aim to model real-world phenomena to describe or predict behavior.

Free fall:  $v = gt$ : velocity of object
	Where $g$ is  gravity and $t$ is time

- **Deterministic models:** Same Input $\implies$ Same Output
- **Limitations of deterministic models:** 
	- uncontrolled factors (ex: air resistance, temp, ...)
	- measurement error
	- lack of knowledge for a model to account for all causes of variations
    

Suppose I like to drink wine very much ...

There’s a bottle of wine I’ve been saving for years.

But then comes this rumor: tomorrow might be the end of the world.

### 1.1 Stochastic vs. Deterministic Models

Deterministic Model: Given initial conditions, output is predicted with (degree of) certainty 

Stochastic (Probabilistic) Model: Outcomes vary even under identical conditions due to randomness (ex: time to failure of a component)

- Our goal: develop a mathematical model of a framework to quantify and analyze uncertainty
- Example: Coin toss, lifetime of a light bulb, number of customers in a shop.
	$\implies$ need probabilistic model to deal with uncertainty
### 1.2 Role of probability in connecting population and sample

- Population: a group of people or object we are interested in studying (interchangeable with model)
- Sample: a subset of the populations (interchangeable with data)

Example 1: Population→Sample

Example 2: Sample→Population

### 1.3 Two Perspectives

- Model→Data:
- Data→Model:

### 1.4 Goal of a Biostatistician

- Develop and evaluate custom statistical methods for new scientific problems.
- Understand the data and the data-generating mechanism.
- Understand the connection between data and model.

## Diagnostic Calculus Test

## 2 Basic Set Theory

### 2.1 Basic terminology

Experiment:

Trial:

Outcome:

Sample space:

Sample space examples:

Example 1:

Example 2:

Example 3:

Example 4:

### 2.2 Sample spaces types

(countably) Finite:

Countably infinite:

If a sample space $S$ is either finite or countable infinite, then it is called a discrete sample  
space(or said to be countable).

Uncountable:

Example:

Example:

### 2.3 Event

An event is any collection of possible outcomes of an experiment, that is, any subset of the  
sample space $S$ (including $S$ itself).
 
Consider the example of tossing two coins: The subset:

contains the outcomes that correspond to the event of obtaining “at least one head.” If any  
one of the outcomes in $A$ occurs, then event $A$ occurred. Similarly, if one of the outcomes  
in

occurs, then the event “at least one tail” has occurred.

Consider the experiment of selecting a card at random from a standard deck and noting its  
suit: clubs (C), diamonds (D), hearts (H), or spades (S).

The sample space is

and some possible events are

### 2.4 Set operations
$A\subset B$ (Containment):

$A=B$ (Equality):

- Union:
- Intersection:
- Complement:

Example:

2.4.1 Commutative Laws:

2.4.2 Associative Laws:

2.4.3 Distributive Laws:

Proof of distributive law:  
To prove: For any sets $A$, $B$, and $C$,
$$A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$$

Goal: Prove set equality by showing mutual containment:

$$
\begin{gather}
A\cap(B\cup C)\subset(A\cap B)\cup(A\cap C) \\
\text{and} \\
(A\cap B)\cup(A\cap C)\subset A\cap(B\cup C)
\end{gather}
$$

Proof: first direction  
To show: $A\cap(B\cup C)\subset(A\cap B)\cup(A\cap C)$

Proof: second direction  
To show: $(A\cap B)\cup(A\cap C)\subset A\cap(B\cup C)$

#### 2.4.4 De Morgan’s Laws

Visual:

Visual:

#### 2.4.5 Infinite collections of sets

Let $A_{1},A_{2},\dots$ be a collection of sets, all defined on a sample space $S$. Then:

Example: infinite collections of sets  
Let $S= (0,1]$ and define $A_{i}= [(1/i),1]$. Then:  
$$
\bigcup_{i=1}^{\infty} A_{i} =
$$

$$
\bigcap_{i=1}^{\infty} A_{i} =
$$

#### 2.4.6 Disjoint sets

**Definition** Two events $A$ and $B$ are mutually exclusive(or disjoint) if:

The events $A_{1},A_{2},\dots$ are pairwise disjoint if:

Example:

#### 2.4.7 Partition of a set

**Definition** If $A_{1},A_{2},\dots$ are pairwise disjoint and:

then the collection{$A_{1},A_{2},\dots$}is called a partition of $S$.

Example:

Partitions are useful in probability theory, allowing us to divide the sample space into small,  
nonoverlapping pieces.