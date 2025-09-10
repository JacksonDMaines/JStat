# Lecture 3: Combinatory Analysis

## 1 Counting

### 1.1 Why Counting Matters in Probability  
In discrete probability, we define

- Therefore, enumeration is fundamental to probabilistic reasoning.
- Useful in card games, lotteries, coding theory, genetics, and more.

### 1.2 Fundamental Theorem of Counting  
If a task consists of $k$ independent steps, with choices for step 1, for step 2,... ,  
for stepk, then the total number of outcomes is

Example: A password with 2 digits (0–9) followed by 1 letter (A–Z) has:

### 1.3 Factorial  
**Definition:** For a positive integer $n$, the number of ways to order $n$ distinct items is

Furthermore, we define.  
Example: How many ways to arrange 4 different books on a shelf?

### 1.4 “n choose r”  
The number of ways to choose $r$ objects from $n$, unordered:

**Example:**  
Number of ways to choose 3 people from a group of 10:

**Example:**  
Sampling 2 objects from $\{A, B, C\}$ with replacement.

The tree above has leaves.

**Example:** In many national lotteries(e.g., US Powerball, Lotto 6/49), you must choose 6 distinct  
numbers from a fixed pool (e.g., 1–44), without replacement and without regard to order.  
Question:How many different lottery tickets can you generate by choosing 6 numbers out of 44  
(unordered, no replacement)?

If with order:

If unordered but with replacement:

**Stars and Bars example:**  
**Question:** How many ways to give 8 identical candies to 3 children?

**Example Distribution:**  
Candies=∗, Bars=|(Separate Children):

—  
**Special case 1:** Each child gets at least 1

—  
**Special case 2:** Each child gets at most 6

—  
**Special case 3:** Each child gets at least 1 and at most 6

**Poker Game Examples**  
**Example:** In 5-card poker, each player is dealt 5 cards from a standard 52-card deck. Hands are  
evaluated by categories such as pairs, three-of-a-kind, flush, etc.  
Question: Find the probability of being dealt a 4-of-a-kind (e.g., four Queens and one other  
card).  
**Key Points:**

Step-by-step enumeration:

1. Choose a rank for the quadruple:
2. Choose 4 cards of that rank:
3. Choose the 5th card:  
    Total 4-of-a-kind hands:

Total 5-card hands:

**Probability:**

```
P(4-of-a-kind) =
```

**Question:** How about four aces?  
$P(4-aces) =$

**Example:** How about a full house? A full house is exactly three of one rank and two of another.

- Three cards of one rank (e.g., three Queens)
- Two cards of a dfferent rank (e.g., two 4s)  
    Step-by-step enumeration:

1. Choose rank for 3-of-a-kind:
2. Choose 3 cards of that rank:
3. Choose a different rank for the pair:
4. Choose 2 cards of that rank:  
    Total full house hands:

Total 5-card hands:

**Probability:**

## 2 Conditional Probability

**Definition:**

**Interpretation:**  The probability of A occurring, given that B has occurred.  
Visualize:

Restrict sample space to $B$, then measure how much of $B$ overlaps with $A$.  
Example: Let $A$ be “card is a King,” and $B$ be “card is a face card (J, Q, K).” Then draw one  
card from a standard deck.

Multiplication Rule  
We have:

Note the symmetry of $A\cap B$, we also have:

Expanding to three events:

## 3 Law of Total Probability

If $B_{1}, B_{2},\dots, B_{n}$ forms a partition of the sample space, then

Useful when:

- The event $A$ depends on several mutually exclusive scenarios
- Helps break complex events into manageable parts

## 4 Bayes’ Theorem:

An simplified version:

### —

**Example (Two Boxes with Colored Balls):**  
There are two boxes: $A$ and $B$. You pick a box at random with

```
P(A) = 0. 4 , P(B) = 0. 6.
```

From box $A$, the probability of drawing a red ball is 0.7. From box $B$, the

probability of drawing a red ball is 0.2. You draw one ball and it is red. What is  
the probability that the red ball was from box $A$?  
Solution: First compute the marginal probability of red via total probability:

Apply Bayes’ Theorem:

**Example:** A disease affects 1 in 1,000 people. The diagnostic test is 99% sensitive  
(true positive rate) and 95% specific (true negative rate). A person takes the test  
and gets a positive result  
Question: What is probability the person actually has the disease?  
We want to find: $P(Disease |Positive \space Test)$

- $D$: Person has the disease
- $Dc$: Person does not have the disease
- $T$: Test result is positive

Given:

```
P(D) = P(Dc) =
P(T |D) = P(T |Dc) =
```

Applying Bayes’ Theorem,

Key Takeaways:

- Even with a positive test and high accuracy, the chance of actually having  
    the disease is low.
- This is due to the very low prevalence(rare disease).

## 5 Independence

**Definition:** Two events $A$ and $B$ are statistically independent if:

**Interpretation:** The occurrence of one does not affect the other.

**Examples:**

- Tossing a coin twice: the outcome of one toss doesn’t affect the other.
- Drawing with replacement.
- Breakfast choice and machine failure due to internal defect..

**Example:** Three radar sets operating independently are set to detect any aircraft  
flying through a certain area. Each set has a probability of 0.02 of failing to detect  
a plane in its area.

Multiple Event Independence  
Three events A, B, C are mutually independent if:

Important: pairwise independence does not imply mutual independence.

Example: Consider throwing two fair six-sided dice. The sample space is $S=\{(i,j)|i,j\in\{1,\dots 6\}\}$ with 36 equiprobable outcomes.  
Define the following events:

```
A={doubles appear}={(1,1),(2,2),(3,3),(4,4),(5,5),(6,6)},
B={sum is between 7 and 10},
C={sum is 2, 7 , or 8}.
```

Given:

- $P(A) =$
- $P(B) =$
- $P(C) =$

Triple intersection:

So $B$ and $C$ are

Therefore:

Conclusion

- Triple product identity is to guarantee full independence.
- For three events to be fully independent:
    1. All three pairwise combinations must be independent.
    2. The triple intersection must match the product:  
        $P(A∩B∩C) =P(A)·P(B)·P(C)$ 
- In our last example: only the last condition is satisfied, not the others.