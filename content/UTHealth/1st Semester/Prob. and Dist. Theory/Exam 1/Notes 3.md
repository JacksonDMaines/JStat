# Lecture 3: Combinatory Analysis

## 1 Counting

### 1.1 Why Counting Matters in Probability  
In discrete probability, we define
$$
P(A)=\frac{\text{\# of favorable outcomes}}{\text{total}}
$$
- Therefore, enumeration is fundamental to probabilistic reasoning.
- Useful in card games, lotteries, coding theory, genetics, and more.

### 1.2 Fundamental Theorem of Counting  
If a task consists of $k$ independent steps, with $n_{1}$ choices for step 1, $n_{2}$ for step 2,... , $n_{k}$  
for step k, then the total number of outcomes is
$$
= n_{1}\cdot n_{2}\cdot \dots \cdot n_{k}
$$

Example: A password with 2 digits (0–9) followed by 1 letter (A–Z) has:
$$
10\cdot 10 \cdot 26 = 2600
$$
### 1.3 Factorial  
**Definition:** For a positive integer $n$, the number of ways to order $n$ distinct items is
$$
n! = n \cdot (n-1) \cdot (n-2) \cdot \dots \cdot 2 \cdot 1
$$
Furthermore, we define.  $0! =1$ 

Example: How many ways to arrange 4 different books on a shelf?
$$
4! = 4 \cdot 3 \cdot 2 \cdot 1 = 24
$$
### 1.4 “n choose r”  
The number of ways to choose $r$ objects from $n$, unordered:
$$
{n \choose r} =\frac{n!}{r!(n-r)!}
$$
"n choose r"


**Example:**  
Number of ways to choose 3 people from a group of 10:
$$
{10 \choose 3} = \frac{10!}{3!(10-3)!}=120
$$


**Example:** In many national lotteries(e.g., US Powerball, Lotto 6/49), you must choose 6 distinct  
numbers from a fixed pool (e.g., 1–44), without replacement and without regard to order.  
Question:How many different lottery tickets can you generate by choosing 6 numbers out of 44  
(unordered, no replacement)?
$$
{44 \choose 6} = 7,059,052
$$
If with order:
$$
\frac{44!}{38!}=44 \cdot 43 \cdot \dots \cdot 39
$$

If unordered but with replacement:
$$
{44+6-1 \choose 6} = {44 \choose 6}
$$

**Stars and Bars example:**  
**Question:** How many ways to give 8 identical candies to 3 children?
$$
x_{1}+x_{2}+x_{3}=8\space where \space x_{i}\geq 0 \space for \space i=1,2,3
$$
**Example Distribution:**  
Candies=∗, Bars=|(Separate Children):

—  
**Special case 1:** Each child gets at least 1
$$
{8+3-1 \choose 3-1} = {10 \choose 2} = 45
$$
Note: this is also ${10 \choose_{8}}$, top is number of bars and candies, bottom is number of bars
—  
**Special case 2:** Each child gets at most 6

Let $y_{i}=x_{i}-1,(\geq 0)$ so $y_{1}+y_{2}+y_{3}=5$
$$
{5 + 3 -1 \choose 3-1} = {7 \choose 2} = 21
$$

—  
**Special case 3:** Each child gets at least 1 and at most 6

without restrictions: ${10 \choose 6} = 45$, $45-9=36$

Note: $9$ comes from manually finding all the other combinations


**Poker Game Examples**  
**Example:** In 5-card poker, each player is dealt 5 cards from a standard 52-card deck. Hands are  
evaluated by categories such as pairs, three-of-a-kind, flush, etc.  
Question: Find the probability of being dealt a 4-of-a-kind (e.g., four Queens and one other  
card).  
**Key Points:**
- A 4-of-a-kind $\implies$ 4 cards of the same rank
- $5^{th}$ card must be different
- Order does NOT matter

Step-by-step enumeration:

1. Choose a rank for the quadruple: 13 (2-10, J, Q, K, A)
2. Choose 4 cards of that rank: ${4 \choose 4} =1$
3. Choose the 5th card:  48 (remaining 4 cards)

Total 4-of-a-kind hands: (total 5)
$$
13 \cdot 1 \cdot 48 = 624
$$

Total 5-card hands:
$$
{52 \choose 5} = 2,598,960
$$

**Probability:**


$$
P(4\space of\space a\space kind) = \frac{624}{2598960}
$$

**Question:** How about four aces?  
$P(4\space aces) = \frac{48}{2598960}$

**Example:** How about a full house? A full house is exactly three of one rank and two of another.

- Three cards of one rank (e.g., three Queens)
- Two cards of a dfferent rank (e.g., two 4s)  
    Step-by-step enumeration:

1. Choose rank for 3-of-a-kind: ${13 \choose 1}=13$
2. Choose 3 cards of that rank: ${4 \choose 3}=4$
3. Choose a different rank for the pair: ${12 \choose 1}=12$
4. Choose 2 cards of that rank:  ${4 \choose 2} = 6$

Total full house hands:
$$
13 \cdot 4 \cdot 12 \cdot 6 = 3744
$$
Total 5-card hands:
$$
\text{still the same } {52 \choose 5} 
$$

**Probability:**
$$
P(\text{full house}) = \frac{3744}{{52 \choose 2}} 
$$

## 2 Conditional Probability

**Definition:** 
$$
P(A|B) = \frac{P(A\cap B)}{P(B)} \text{ if P(B)}>0
$$
"p of $A$ given $B$"

**Interpretation:**  The probability of A occurring, given that B has occurred.  


Restrict sample space to $B$, then measure how much of $B$ overlaps with $A$.  

Example: Let $A$ be “card is a King,” and $B$ be “card is a face card (J, Q, K).” Then draw one  
card from a standard deck.
$$
P(A|B) = \frac{P(king\cap face)}{P(face)}=\frac{\frac{4}{52}}{\frac{12}{52}}=\frac{1}{3}
$$

Multiplication Rule  
We have: $P(A\cap B)=P(B)\cdot P(A|B)$

Note the symmetry of $A\cap B$, we also have: $P(A\cap B)=P(A)\cdot P(B|A)$

Expanding to three events:$P(A\cap B\cap C)=P(A)\cdot P(B|A) \cdot P(C|A\cap B)$

## 3 Law of Total Probability

If $B_{1}, B_{2},\dots, B_{n}$ forms a partition of the sample space, then
$$
P(A)= \sum_{i=1}^{n}P(B_{i})\cdot P(A|B_{i})
$$

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