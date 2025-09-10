
# Probability
- Assign level of uncertainty to an outcome of a phenomena 

## Sample Space
- Denoted $\Omega$ or $S$

## Event


## Probability of Finding Event
- Denoted: $P(A)$
### Theoretical Prob.
$$
\frac{\text{Number of outcomes in A}}{\text{Number of outcomes in S}}
$$
- What we guess. 

### Empirical Prob.
$$
\frac{\text{Number of times A occured}}{\text{Number of trials or observations}}
$$
- Observed Data. 


## Probability  Distribution
List of all possible events and their probabilities

## Complement 
- Denoted: $D^c$
- All outcomes not in $D$

Note: $P(D^c)=1-P(D)$

## Set Operations

### Union
- Combined elements of $A$ and $B$
- Denoted: $\cup$ 
- "or"

### Intersection
- common elements of $A$ and $B$
- Denoted: $\cap$
- "and"

**Ex:** Let $A=\{1,2,3,4,5\}$ and $B=\{1,3,9,12\}$ then, 
$$
A\cup B=\{1,2,3,4,5,9,12\}
$$
and
$$
A\cap B = \{1,3\}
$$
### General Addition Rule
$$
P(A\cup B) = P(A) + P(B) - P(A\cap B)
$$
## Disjoint
 - Cannot happend at the same time.
 - $A\cap B=\emptyset$, then $A$ and $B$ are mutually exclusive or disjoint
**Ex:** Rolling dice, rolling 1 or 2 

### Special Addition Rule
 - If $A$ and $B$ are disjoint
 - $A\cap B=\emptyset$
$$
P(A\cup B) = P(A) + P(B)
$$
## Frequency Table
- Marginal Total:  column or row total
- Joint Total: is in the cell


## Conditional Probability
- Restrict to group, known group of interest.
Let $A$ and $B$ be events
$$
P(A|B) = \frac{P(A\cap B)}{P(B)}=\frac{\text{Joint Prob.}}{\text{Marginal Prob.}}
$$
## Independence 
- Knowing previous event doesnt effect future events
$$
P(A\cap B) =P(A)P(B)
$$
- When $A$ and $B$ are independent. 

## General Multiplication Rule
$$
P(A\cap B)=P(A|B)P(B)
$$
- Thus $A$ and $B$ are independent if $P(A|B)=P(A)$

To check independence
1. $P(A\cap B)=P(A|B)P(B)$
2. $P(A|B)=P(A)$


**Question:** Let $A$ and $B$ be events that are both disjoint and independent. Is it true that both $P(A)$ and $P(B)$ are both 0, or is just one being 0 satisfactory? 

**Answer:**

