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

- **Population**: a group of people or object we are interested in studying (interchangeable with model)
- **Sample**: a subset of the populations (interchangeable with data)

**Example 1:** Population→Sample
40% have particular biomarker.
	Question: A random sample of 10 subjects was chosen. What number of them have the biomarker?

Model to Data

**Example 2**: Sample→Population
Observe among 10 randomly selected subjects 4 have a biomarker. 
	Question 1: What is the estimated proportion in population with the biomarker. 
	Question 2: If Someone claims that 30% have the biomarker, can we accept or reject that claim?

Data to Model
### 1.3 Two Perspectives

- **Model→Data**: Known model (population) allows us to calculate the probability of observed data (sample)

- **Data→Model**: Known data (sample) allows us to estimate the parameters of model (population)

### 1.4 Goal of a Biostatistician

- Develop and evaluate custom statistical methods for new scientific problems.
- Understand the data and the data-generating mechanism.
- Understand the connection between data and model.

## Diagnostic Calculus Test

## 2 Basic Set Theory

### 2.1 Basic terminology

**Experiment**: A process that can generate observable outcomes

**Trial**: Single execution of single experiment

**Outcome**: a possible result of trial

**Sample** **space**: set of all possible outcomes of an experiment, 
- Denoted: $S$

**Sample space examples**:

Example 1: Toss 2 Coins
- $S =\{HH, HT, TH, TT\}$

Example 2: Toss coin twice, observe # of heads
- $S=\{0,1,2\}$

Example 3: Toss coin, until heads occurs, we observe # of tosses.
- $S=\{1,2,3,\dots\}$

Example 4: A lightbulb in service, time of operation until it dies
 - $S=\{0\leq t\leq \infty\}$

### 2.2 Sample spaces types

**(countably) Finite:** $S=\{e_{1}, e_{2}, \dots, e_{N}\}$ 
- Example 1 and 2
**Countably infinite**: $S=\{e_{1}, e_{2}, \dots\}$
- Example 3

If a sample space $S$ is either finite or countable infinite, then it is called a discrete sample  
space(or said to be countable).

**Uncountable**: It does NOT have 1-to-1 map to Natural numbers. 
- There is no way to enumerate all elements of $S$

Example: Set of Real #'s in interval $[0,1]$ 

Example: The exact life time of light bulbs
 - $S=\{t\in\mathbb{R}|t\geq0\}$

### 2.3 Event

An event is any collection of possible outcomes of an experiment, that is, any subset of the  
sample space $S$ (including $S$ itself).
 
Consider the example of tossing two coins: The subset:
$$
A = \{HH, HT, TH\}
$$
contains the outcomes that correspond to the event of obtaining “at least one head.” If any  
one of the outcomes in $A$ occurs, then event $A$ occurred. Similarly, if one of the outcomes  
in
$$
B=\{TT, HT, TH\}
$$
occurs, then the event “at least one tail” has occurred.

Consider the experiment of selecting a card at random from a standard deck and noting its  
suit: clubs (C), diamonds (D), hearts (H), or spades (S).

The sample space is
$$
S=\{C,D,H,S\}
$$
and some possible events are
$$
A = \{C, D\}
$$
$$
B = \{D, H, S\}
$$

### 2.4 Set operations
$A\subset B$ (Containment): $x\in A \implies x\in B$

$A=B$ (Equality): $A\subset B$ and $B \subset A$

- **Union:** $A\cup B=\{x: x\in A \text{ or }x\in B\}$
- **Intersection:** $A\cap B=\{x: x\in A \text{ and }x\in B\}$
- **Complement:** $A^c=\{x: \not\in A\}$ 
	- $A/B = \{x: x\in A \text{ and }x\not\in B\}$


**2.4.1 Commutative Laws:** $A\cup B = B\cup A$ and $A\cap B = B\cap A$

**2.4.2 Associative Laws:** $A\cup(B\cup C) = (A\cup B)\cup C$ and $A\cap(B\cap C)=(A\cap B)\cap C$

**2.4.3 Distributive Laws:** $A\cup(B\cap C)=(A\cup B)\cap(A\cup C)$ and $A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$


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

$$
(A\cup B)^c = A^c\cap B^c
$$
$$
(A\cap B)^c = A^c\cup B^c
$$

#### 2.4.5 Infinite collections of sets

Let $A_{1},A_{2},\dots$ be a collection of sets, all defined on a sample space $S$. Then:
$$
\bigcup_{i=1}^{\infty} A_{i} = \{x\in S|x \in A_{i} \text{ for some i}\}
$$

$$
\bigcap_{i=1}^{\infty} A_{i} = \{x \in S|x \in A_{i} \text{ for all i}\}
$$



#### 2.4.6 Disjoint sets

**Definition** Two events $A$ and $B$ are mutually exclusive(or disjoint) if:
$$
A\cap B = \emptyset 
$$
The events $A_{1},A_{2},\dots$ are pairwise disjoint if:
$$
A_{i}\cap A_{j} = \emptyset \space \forall_{i \not=j}
$$


#### 2.4.7 Partition of a set

**Definition** If $A_{1},A_{2},\dots$ are pairwise disjoint and:
$$
\bigcup_{i=1}^{\infty}A_{i}=S
$$

then the collection{$A_{1},A_{2},\dots$}is called a partition of $S$.

Partitions are useful in probability theory, allowing us to divide the sample space into small,  
nonoverlapping pieces.