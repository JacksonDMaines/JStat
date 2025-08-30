
## System of Equations
$$
\begin{gather}
a_{11}x_{1}+a_{12}x_{2}+\dots+a_{1m}x_{m}=b_{1} \\
a_{21}x_{1}+a_{22}x_{2}+\dots+a_{2m}x_{m}=b_{2} \\ 
\vdots \\
a_{n1}x_{1}+a_{n2}x_{2}+\dots+a_{nm}x_{m}=b_{n}
\end{gather}

$$
$$
\begin{matrix}
da
\end{matrix}
$$


$$
\left[\begin{array}{cc|c} 1 & 2 & 3 \\ 4 & 5 & 6 \end{array}\right]
$$

### Augmented Matrix
$$

\left[\begin{array}{cccc|c} 
a_{11} & a_{12} & \dots & a_{1m} & b_{1} \\
a_{21} & a_{22} & \dots & a_{2m} & b_{2} \\
\vdots & \vdots & \ddots & \vdots & \vdots \\
a_{n1} & a_{n2} & \dots & a_{nm} & b_{n} \\
\end{array}\right]
$$



## Matrix Operations
- Multiply row i by $c\iff cR_{i}$
- Switch rows i and j $\iff R_{i}\leftrightarrow R_{j}$
- Add row i to c times row j $\iff R_{i}\leftrightarrow cR_{j}$


## Row-Echelon
Needs to satisfy
- a row of all zeros is at the bottom of the matrix
- if row isn't all zeros then its left most entry is a 1
- 2 successive rows of not all zeros the 1's should be one column off
to satisfy reduced row-echelon you need all of above and 
- if first entry of column is 1 all other entries are zeros

Note: Reducing augmented matrix to row-echelon is called Gaussian elimination
	Reducing augmented matrix to reduced row-echelon is called Gaus-Jordan elimination

## Solving System of Equations
Augmented Matrix  $\to$ Row Echelon $\to$ Back Sub 


## Matrix


$$
\begin{gather} \space \space \space m \\ \space \space \space\longrightarrow \\n\Big\uparrow
\left[\begin{array} 
 - - & -  \\
- & -
\end{array}\right] \\ 
\end{gather}
$$

this is a $\text{n x m}$ matrix


### Identity Matrix

$$
I = \left[ \begin{array}{ccccc}  
1 & 0 & 0 & \dots & 0 \\
0 & 1 & 0 & \dots & 0 \\
0 & 0 & 1 & \dots & 0 \\ 
\vdots & \vdots & \vdots&\ddots & \vdots\\
0 & 0 & 0 & \dots & 1 \\
\end{array}\right]
$$
 The 1's lay on the main diag of the matrix


### Matrix Algebra
#### +/-
just +/- cell to cell
you can only +/- matrix of same sizes

#### $\cdot$ by Constant
$$
E \cdot \left[\begin{array} 
 - a & b  \\
c & d
\end{array}\right] = \left[\begin{array} 
 - E\cdot a & E\cdot b  \\
E\cdot c & E\cdot d
\end{array}\right]
$$

or any $\text{n x m}$ matrix

#### $\cdot$ by Matrix
Let $A$ be a $\text{n x p}$ matrix, and $B$ be a $\text{p x m}$ matrix, then

$AB$ will be a $\text{n x m}$ matrix

where the $ij^{th}$ entry is found by multiplying row $i$ of $A$ and column $j$ of $B$

Note: its not just that... its more like the entry 

$$
AB_{ij} = \sum _{k=1}^{p}A_{ki}B_{ik}
$$
but how do I explain that easier?

# YO INSERT COOL PICTURE HERE 
	Later :)


An easy trick to remember is "row times column" 


##### Multiplication Example
$$
\left[ \begin{array}{cc}  
1 & 2 \\
3 & 4 \\
5 & 6
\end{array}\right] \cdot
\left[ \begin{array}{ccc} 1 & 2 & 1  \\
2 & 1 & 1
\end{array}\right]
$$
Note: we can tell the $1st$ matrix is $3 \times2$ and the $2nd$ matrix is $2 \times 3$ therefore

$$
\underbracket{3\,\times \overbracket{2 \space \cdot \space 2}^{\text{matching}} \times\, 3}_{\text{answer}} = 3 \times 3
$$

we know our final matrix will be size $3 \times 3$. If we follow our matrix multiplication mantra "row times column"

$$
\left[ \begin{array}{cc}  
1 & 2 \\
3 & 4 \\
5 & 6
\end{array}\right] \cdot
\left[ \begin{array}{ccc} 1 & 2 & 1  \\
2 & 1 & 1
\end{array}\right] = \left[\begin{array}
1(1) + 2(2) & 1(2) + 2(1) & 1(1) + 2(1)  \\
3(1) + 4(2) & 3(2) + 4(1) & 3(1) + 4(1) \\
5(1) + 6(2) & 5(2) + 6(1) & 5(1) + 6(1)
\end{array}\right]
$$

simplify

$$
= \left[\begin{array}{cc}
1 + 4 & 2 +2 &  1+2 \\
3 + 8 &  6 + 4 & 3 + 4  \\
5 + 12 & 10 + 6 & 5 + 6
\end{array}\right] = \left[\begin{array}{ccc}
5 & 4 & 3 \\
11 & 10 & 7 \\
17 & 16 & 11
\end{array}\right]
$$



### Transpose 
We denote transpose of a matrix as $A^T$

All transpose does is makes every row become a column (or column a row). Its not as confusing as it sounds. 

Note: A $n \times m$ matrix should become a $m \times n$ matrix after transposing.

##### Transpose Example
Let A be the matrix
$$
\left[ \begin{array}{ccccc}  
a_{11} & a_{12} & a_{13} & \dots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \dots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \dots & a_{3n} \\ 
\vdots & \vdots & \vdots&\ddots & \vdots\\
a_{m1} & a_{m2} & a_{m3} & \dots & a_{mn} \\
\end{array}\right]
$$
then $A^T$ will be
$$
\left[ \begin{array}{ccccc}  
a_{11} & a_{21} & a_{31} & \dots & a_{n1} \\
a_{12} & a_{22} & a_{32} & \dots & a_{n2} \\
a_{13} & a_{32} & a_{33} & \dots & a_{n3} \\ 
\vdots & \vdots & \vdots&\ddots & \vdots\\
a_{1n} & a_{2n} & a_{3n} & \dots & a_{nm} \\
\end{array}\right]
$$
Notice how the n's and m's kinda flip?



#### 2nd Transpose Example 
$$
\left[\begin{array}{c}
1 & 2 \\
3 & 4 \\
5 & 6
\end{array}\right]^T = \left[\begin{array}{c}
1 & 3 & 5 \\
2 & 4 & 6
\end{array}\right]
$$
or
$$
\left[\begin{array}{c} 
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}\right]^T = \left[\begin{array}
{c}1 & 4 & 7 \\
2 & 5 & 8 \\
3 & 6 & 9
\end{array}\right]

$$


### Invertible
If A is a square matrix and there exists B a square matrix such that
$$
AB = BA = I
$$
where $I$ is the identity matrix, then A is invertible and B is the inverse of A. If B doesn't exist then A is a singular matrix

#### Properties of Invertible Matrices
Let A,B be invertible matrices of $n \times m$, then
1. $AB$ is invertible and $(AB)^{-1} = B^{-1}A^{-1}$
2. $A^{-1}$ is invertible and $(A^{-1})^{-1} = A$
3. For $n = 0,1,2\dots$ , $A^n$ is invertible and $(A^n)^{-1} = A^{-n} = (A^{-1})^n$
4. Let $c\in \mathbb{R}/\text{\{0\}}$ then $cA$ is invertible and $(cA)^{-1} = \frac{1}{c}A^{-1}$
5. $A^T$ is invertible and $(A^{T})^{-1} = (A^{-1})^T$


### Inverse 
##### For a $2 \times 2$ Matrix
$$
A = \left[\begin{array}{c} a & b \\
c & d
\end{array}\right]
$$
A is invertible if $ad-bc \neq 0$ and singular if $ad-bc = 0$ 

If A is invertible then, 
$$
A^{-1} = \frac{1}{ad-bc}\left[\begin{array}
{c}d & -b \\
-c & a
\end{array}\right]

$$
I always remember "switch a and d, negative b and c"

##### Tricks
If upper triangle matrix has zeros in diag its singular. 
If it has no zeros its invertible

### Symmetric
$A = A^T$, then $A$ is symmetric
##### Properties
1. $\forall A$, $AA^T$ and $A^TA$ is symmetric
2. Let $A$ be invertible and symmetric then $A^{-1}$ is symmetric
3. Let $A be invertible then $AA^T$ and $A^TA$ are invertible


### LU-Decomposition
Look in Numerical Notes






### Determinates
$A$ is a $n \times n$ then the determinate of $A$ is denoted:

$$
\det(a) = |A| = \left[\begin{array}
{aaa}a_{11} & a_{12} & \dots \\
\vdots & \ddots
\end{array}\right]
$$

#### $2 \times 2$ Matrix

$$
\det(A) = \left|\begin{array}
{aa}a & b \\
c & d
\end{array}\right| = ad-bc
$$

#### $3 \times 3$ Matrix

$$
\det(A) = \left|\begin{array}
{aaa}a & b  & c \\
d & e & f \\
g & h & i
\end{array}\right| = aei+bfg + cdh - (ceg + afh + bdi)
$$

this comes from the product of the diagonals of this matrix

$$
\left|\begin{array}
{aaa}a & b  & c \\
d & e & f \\
g & h & i
\end{array}\right|\begin{array}
{aa}a & b \\
d & e \\
g & h
\end{array}
$$

for example.

$$
\left|\begin{array}
{aaa}\colorbox{yellow}{a} & \colorbox{green}{b}  & \colorbox{pink}{c} \\
d & \colorbox{yellow}{e} &\colorbox{green}{f} \\
g & h & \colorbox{yellow}{i}
\end{array}\right|\begin{array}
{aa}a & b \\
\colorbox{pink}{d} & e \\
\colorbox{green}{g} & \colorbox{pink}{h}
\end{array}
$$

get the first half of the equation. 

$$
\colorbox{yellow}{aei} + \colorbox{green}{bfg} + \colorbox{pink}{cdh}
$$

then the second half the equation comes from the opposite angle diagonals. 

$$
\left|\begin{array}
{aaa}a & b  & \colorbox{orange}{c} \\
d & \colorbox{orange}{e} & \colorbox{lightblue}{f} \\
\colorbox{orange}{g} & \colorbox{lightblue}{h} & \colorbox{red}{i}
\end{array}\right|\begin{array}
{aa}\colorbox{lightblue}{a} & \colorbox{red}{b} \\
\colorbox{red}{d} & e \\
g & h
\end{array}
$$

getting you: 

$$
\colorbox{orange}{ceg} + \colorbox{lightblue}{afh} + \colorbox{red}{bdi}
$$

that comes together to give you the equation for a determinate of a $3 \times 3$ matrix

$$
 \det(a) = \colorbox{yellow}{aei} + \colorbox{green}{bfg} + \colorbox{pink}{cdh} - (\colorbox{orange}{ceg} + \colorbox{lightblue}{afh} + \colorbox{red}{bdi})
$$


#### Properties
Let $A$ be $n \times n$ and $c\in\mathbb{R}$
	$\det(c\cdot A)=c^n\det(A)$
Let $A,B$ be $n \times n$
	$\det(A\cdot B) = \det(A) \cdot \det (B)$
Let $A$ be $n \times n$
	$\det(A^{-1}) = \frac{1}{\det(A)}$
$n \times n$ matrix $A$ is invertible iff $\det(A) \neq 0$
Let $A$ be $n \times n$
	$\det(A) = \det(A^T)$
Let $A$ be $n \times n$ and a triangle matrix
	then $\det(A) = a_{11}\cdot a_{22}\cdot\dots \cdot a_{nn}$

For larger matrices
	you can do some weird submatrix bullshit to find determinates. 
	Its not super hard to do by hand its just annoying.
	If its that bigger then $3\times 3$ just use a computer?


### Euclidean
#### Norm
Magnitude of vector, denoted: 
$$
||v||
$$
where
$$
||v|| = \sqrt{v_{1}^2 + v_{2}^2 + \dots + v_{n}^2}
$$
##### Properties
$||c \cdot v|| = |c| \cdot ||v||$
Unit vector: $||v||=1$
For $\mathbb{R}^2\text{ or }\mathbb{R}^3$
	$||v||\geq 0$
	$||v|| = 0$ iff $v=0$


#### Dot Product
or scalar product or Euclidean inner product, it has a lot of names.

Let $u$ and $v$ be vectors in  with $\mathbb{R}^2\text{ or }\mathbb{R}^3$ with angle $\theta$ in between them. Then
$$
u \cdot v = ||u|| \cdot ||v|| \cdot \cos(\theta)
$$
This is useful to find angles between vectors, like in physics and stuff like that.

or
$$
\mathbb{R}^2: u\cdot v = u_{1}v_{1} + u_{2}v_{2}
$$
$$
\mathbb{R}^3: u\cdot v = u_{1}v_{1} + u_{2}v_{2}+ u_{3}v_{3} 
$$
$$
\mathbb{R}^n: \text{it scales}
$$

Note: $|u \cdot v| \leq ||u|| \cdot||v||$ in $\mathbb{R}^n$

#### Projection 
These fucking suck. You really need some visual for this.

Orthogonal projection of $u$ on $a$ denoted: 
$$
proj_{a}u =  \frac{u\cdot a}{||a||^2}a
$$
where that $u \cdot a$ on top is a dot product.

Add visual of projection.


#### Cross Products
Let $u$ and $v$ be vectors in $\mathbb{R}^3$ then the cross product of $u\text{ and } v$ is denoted:
$$
u \times v
$$
$$
u \times v = (u_{2}v_{3}- u_{3}v_{2}, u_{3}v_{1}- u_{1}v_{3}, u_{2}v_{2}-u_{2}v_{1})
$$
this is a vector I think? so maybe I should be using <>? 

$$
u \times v = \left(\left|\begin{array}
{aa} u_{2} & u_{3} \\
v_{2} & v_{3}
\end{array}\right|, -\left|\begin{array}
{aa} u_{1} & u_{3} \\
v_{1} & v_{3}
\end{array}\right|, \left|\begin{array}
{aa} u_{1} & u_{2} \\
v_{1} & v_{v}
\end{array}\right|\right)
$$

$$
u \times v = \left| \begin{array}
{aaa} i & j & k \\
u_{1} & u_{2} & u_{3} \\
v_{1} & v_{2} & v_{3}
\end{array}\right|
$$

	Note: you also need to solve for i,j,k here after getting the determinate

$$
||u \times v|| = ||u|| \cdot ||v|| \sin(\theta)
$$


#### Orthogonal
if $u \cdot v = 0$ , $\mathbb{R}^n$

if orthogonal, then
$$
||u+v||^2 = ||u||^2+||v||^2
$$

### Vector Spaces
#### Linear independence
#### Least Squares
#### OR-Decomposition