
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


An easy trick to remember is "row times column" 