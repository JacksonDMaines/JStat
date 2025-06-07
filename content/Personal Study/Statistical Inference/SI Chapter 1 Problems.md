[[SI Notes#Chapter 1|Chapter 1 Notes]]
### 1.1 

	a. Should be 2^4 possible combination

		S = {HHHH, HHHT, HHTT, HTTT, 
			TTTT, THHH, TTHHH, TTTH, 
			HTTH, HTHH, HHTH, THHT, 
			THTT, TTHT, THTH, HTHT}
	b.

$$
{ 0, 1, 3, 4, \dots. }
$$
			Cause its some countable number of bites, its not $$[0, \infty) $$ cause you cant have like .1 bites for 1.5 bites.
	c. $$ [0, \infty) $$
	 d. $$ (0, \infty) $$
	 e. $$ [0,1] $$

### 1.2
	a. 
	
$A/B = A/(A \cap B) = A \cap B^c$
if $x \in A/B$ then $x \in A$ and $x\notin B$. Since x doesn't exist in B then in any intersection of B x still wont exists So $x \in A$ and $x\notin(A \cap B)$ or $x\in A/(A\cap B)$. Thus $x\in A$ and $x \notin B$ then $x \in A$ and $x\in B^c$
therefore $x\in(A\cap B^c)$

	b. 
	
- $B = (B \cap A)\cup(B \cap A^c)$
- We need to prove both directions
- $x \in B \implies x\in (B\cap A) \cup(B \cap A^c)$
	- Let $x \in B$. Then $x\in A$ or $x\in A^c$
		- If $x\in A$, 
		- then $x\in B\cap A$ and $x\notin B\cap A^c$ therefore $x\in (B\cap A) \cup (B \cap A^c)$
		- If $x \in A^c$, 
		- then $x \notin B \cap A$ and $x \in B \cap A^c$ therefore $x\in (B\cap A) \cup (B \cap A^c)$
	- thus $x \in B \implies x\in (B\cap A) \cup(B \cap A^c)$ or $(B\cap A) \cup (B \cap A^c) \subset B$ (This proves right direction)
- $x\in (B\cap A) \cup(B \cap A^c) \implies x\in B$
	- Let $x\in (B\cap A) \cup(B \cap A^c)$, thus $x \in (B \cap A)$ or $x \in (B \cap A^c)$
		- If $x \in (B \cap A)$
		- then $x\in B$ and $x \in A$ 
		- If $x\in (B \cap A^c)$
		- then $x \in B$ and $x \in A^c$
	- in both cases $x \in B$
	- thus $x\in (B\cap A) \cup(B \cap A^c) \implies x\in B$ or $B \subset (B\cap A) \cup(B \cap A^c)$ (This proves left direction)
Therefore $B \iff (B\cap A) \cup(B \cap A^c)$ or $B = (B \cap A)\cup(B \cap A^c)$

	c.

$B/A = B \cap A^c$
If $x \in B/A$ then $x \in B$ and $x \notin A$ thus $x \in B$ and $x \in A^c$ or $x\in B \cap A^c$
Thus $B/A = B \cap A^c$

	d. 

$A \cup B = A \cup (B \cap A^c)$
$A \cup B = A \cup (B \cap A)\cup(B \cap A^c)$ from part b.)
$A \cup (B \cap A)\cup(B \cap A^c) = (A \cup (B \cap A)) \cup (A \cup (B \cap A^c))$
$(A \cup (B \cap A)) \cup (A \cup (B \cap A^c)) = ((A \cup B) \cap (A \cup A)) \cup (A \cup (B \cap A^c))$
$((A \cup B) \cap (A \cup A)) \cup (A \cup (B \cap A^c)) = ((A \cup B) \cap A) \cup (A \cup (B \cap A^c))$
$((A \cup B) \cap A) \cup (A \cup (B \cap A^c)) = A \cup (A \cup (B \cap A^c))$  Identity:$((A \cup B) \cap A)=A$
$A \cup (A \cup (B \cap A^c) =A \cup (B \cap A^c)$


### 1.3


	a.

$A \cup B=B\cup A$ and $A \cap B=B\cap A$
Let $x\in A\cup B$ 
	Then $x \in A$ or $x \in B$, therefore $x \in B \cup A$. Thus $A \cup B=B\cup A$
Let $x\in A\cap B$
	Then $x \in A$ and $x \in B$, therefore $x\in B\cap A$. Thus $A \cap B=B\cap A$

	b. 

$A\cup (B\cup C) = (A\cup B)\cup C$ and $A\cap(B\cap C) = (A\cap B)\cap C$
Let $x\in A\cup(B\cup C)$
	Then $x\in A$ or $x\in B\cup C$, or $x\in A$ or $x\in B$ or $x\in C$. Thus $x\in A\cup B$ or $x \in C$. Therefore $x\in(A\cup B) \cup C$.  $A\cup (B\cup C) = (A\cup B)\cup C$
Similar Idea for $\cap$

	c. 

$(A\cup B)^c = A^c \cap B^c$ and $(A \cap B)^c = A^c \cup B^c$
Let $x \in (A\cup B)^c$
	Then $x \notin A\cup B$, thus $x\notin A$ or $x\notin B$. So $x\in A^c$ and $x\in B^c$, therefore $x\in A^c\cap B^c$ thus $(A\cup B)^c = A^c \cap B^c$



### 1.4
a. $P(A\cup B) = P(A) + P(B) -P(A\cap B)$
b. $P((A\cap B^c)\cup(B\cap A^c)) = P(A\cap B^c) + P(B\cap A^c) = [P(A) - P(A\cap B)] + [P(B) - P(B\cap A)] = P(A) + P(B) -2P(A\cap B)$
c. same as a.
d. $1 - P(A\cap B)$




### 1.5

$A = {twin \space females}$
$B = identical \space twins$
$C = twins$

a. identical twin females (think a bunch of concentric circles)
b. $P(A\cap B \cap C) = \frac{1}{90} \frac{1}{3} \frac{1}{2} =\frac{1}{540}$

### 1.6
$P(0 \space heads) = (1-u)(1-w)$
$P(1 \space head) = u(1-w) + (1-u)w$
$P(2 \space heads)=uw$

### 1.7


did these on paper, honestly I like it better than typing them.....

### 1.9
