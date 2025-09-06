# Lecture 2: Basic Rules of Probability

Probability  
For each event A in the sample space S,

## 1 Sigma Algebra

A collection of subsets of S is called a sigma algebra(or Borel field), denoted by B, if it  
satisfies the following three properties:

```
a.
b.
c.
```

Properties of Sigma Algebra

- The empty set ∅ is a subset of any set. Thus, ∅⊆S.
- Since S=∅ c, properties (a) and (b) imply that S is always in B.

- From DeMorgan’s Laws, B is closed under countable intersections.

Associated with sample space S we can have many different sigma algebras. For example,  
the collection{∅, S}is a sigma algebra, usually called the trivial sigma algebra.

Example: Sigma Algebra (finite or countable S)

If the sample space S is finite or countable, we define:

```
B={all subsets of S, including S itself}
```

If S has n elements, then there are 2n sets in B.

Example:

Example: Sigma Algebra (uncountable S)

## 2 Axioms of Probability

Given a sample space S and an associated sigma algebra B, a probability function is a  
function P with domain B that satisfies:

```
1.
2.
3.
```

Comments on the Axioms

- The properties above are called the Axioms of Probability (or the Kolmogorov  
    Axioms, after A. Kolmogorov, one of the fathers of probability theory).
- ANY function P satisfying the axioms is called a probability function.
- The axiomatic definition makes no attempt to tell what particular function P to choose,  
    it merely requires P to satisfy the axioms.
- For any sample space many different probability functions can be defined. Which  
    one(s) reflects what is likely to be observed in a particular experiment is still to be  
    discussed.

Example: Defining Probabilities  
Experiment:

Example: defining probabilities  
Dart Game: The game of darts is played by throwing a dart at a board and receiving  
a score corresponding to the number assigned to the region in which the dart lands. Dart  
lands on region i with probability proportional to area.

```
P(scoringipoints) =Area of dart boardArea of regioni
```

## 3 Simple sample space

Simple sample space:

Example:

## 4 Some useful results

### 4.1 P(∅) = 0

To prove it:

### 4.2 Complement rule: P(A) = 1−P(A)

To prove it:

### 4.3 Monotonicity: If A⊆B, then P(A)≤P(B).

To prove it:

### 4.4 Boundedness of probability

For any event A⊆S:  
P(A)≤P(S) = 1⇒ P(A)≤ 1

### 4.5 Inclusion-exclusion

For two events A and B:

For three events A,B, and C:

### 4.6 Boole’s Inequality:

For a collection of events A 1 , A 2 ,... , An,

### 4.7 Bonferroni’s Inequality:

Visualization (two events)

Reading: Sections 1.1–1.2 of your textbook




