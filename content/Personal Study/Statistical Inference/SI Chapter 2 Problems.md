[[SI Notes#Chapter 2|Chapter 2 Notes]]
### 2.1
a.) $Y=X^3$ and $f_{X}(x)=42x^5(1-x)$ for 0<x<1
Find PDF of Y? 

Let $y=x^3=g(x)$
	 Then $g'(x)=3x^2 > 0$ $\forall x\in \mathbb{R}$ , thus monotone?

We know that (from theorem link it later!!!!!)

$$
f_{Y}(y) = \begin{cases} f_{x}(g^{-1}(y))|\frac{d}{dy}g^{-1}(y)|& y \in Y \\
0&other

\end{cases} 

$$
so 

$$
g^{-1}(y) = y^{1/3} \implies f_{x}(g^{-1}(y)) = 42(y^{1/3})^{5}(1-y^{1/3})
$$
and 
$$
\frac{d}{dy}g^{-1}(y)=\frac{1}{3}y^{-2/3}
$$
therefore
$$
f_{Y}(y)=\begin{cases}
42(y^{1/3})^5(1-y^{1/3})|\frac{1}{3}y^{-2/3}|&0<y<1 \\
0 & other
\end{cases}
$$
lets reduce this

$$
\begin{aligned}
&42(y^{1/3})^5(1-y^{1/3})\left|\frac{1}{3}y^{-2/3}\right| \\
&= 14y^{5/3}(1-y^{1/3})y^{-2/3} \\
&= 14y(1-y^{1/3}) \\
&= 14y - 14y^{4/3}
\end{aligned}
$$

thus 

$$
=\begin{cases}
14y - 14y^{4/3}&0<y<1 \\
0 & other
\end{cases}
$$
Lets prove the pdf integrates to 1
$$
\begin{aligned} \\
&\int f_{Y(y)dy} = \int_{0}^{1}14y-14y^{4/3}dy = 14\int_{0}^{1}ydy - 14\int_{0}^{1}y^{4/3}dy \\
&= 14\left[ \frac{1}{2}y^{2} \big|_{0}^{1}\right] - 14\left[ \frac{3}{7}y^{7/3} \big|_{0}^{1} \right] \\
&= 14\left( \frac{1}{2}(1)^{2} - 0 \right) - 14\left( \frac{3}{7}(1)^{7/3}-0 \right) \\
&= 7-6 = 1
\end{aligned} \\

$$

b.) $Y=4X+3$ and $f_{X}(x) = 7e^{-7x}$ for $0<x<\infty$
Find pdf of Y? 

So let $y=4x+3=g(x)$
	and $g'(x) = x >0\space\space\forall x\in(0,\infty)\implies monotone$ I think?
then
$g^{-1}(y)=\frac{y-3}{4}\implies f_{X}(g^{-1}(y))=ye^{-7\frac{y-3}{4}}$ 
and
$\frac{d}{dy}g^{-1}(y)=\frac{1}{4}$
therefore 
$$
f_{Y}(y)=\begin{cases} 7e^{-7\frac{y-3}{4}}|\frac{1}{4}|&3<y<\infty & \\
0 & other
\end{cases} \\
$$
lets reduce
$$
\begin{aligned}
&\frac{7}{4}e^{-7\frac{y-3}{4}} \\
&= \frac{7}{4}e^{\frac{-7y}{4} + \frac{21}{4}} \\
&=\frac{7}{4}e^{\frac{21}{4}}\cdot e^{\frac{-7y}{4}}
\end{aligned}
$$
$$
=\begin{cases}
\frac{7}{4}e^{\frac{21}{4}}\cdot e^{\frac{-7y}{4}} &3<y<\infty \\
0 & other
\end{cases}
$$

proving pdf integrates to 1
$$
\begin{aligned}

&\int f_{Y}(y)dy = \int_{3}^{\infty}\frac{7}{4}e^{\frac{21}{4}}\cdot e^{\frac{-7y}{4}}dy \\
& =\frac{7}{4}e^{\frac{21}{4}}\cdot \int_{3}^{\infty}e^{\frac{-7y}{4}}dy \\
&=\frac{7}{4}e^{\frac{21}{4}}[\frac{-4}{y}e^{\frac{-7y}{4}}\big|_{3}^{\infty}] \\
\\
& Note:\lim_{ x \to \infty }e^-x = 0 \\ \\
&= \frac{7}{4}e^{\frac{21}{4}}[0 - (-\frac{4}{7}e^{\frac{-7(3)}{4}})] \\
&= \frac{7}{4}e^{\frac{21}{7}}[0 + \frac{4}{7}e^{\frac{-21}{7}}] \\
&= (\frac{7}{4})(\frac{4}{7})e^{\frac{21}{7}}\cdot e^{\frac{-21}{7}} \\
&= (1)e^{\frac{21}{7}+ \frac{-21}{7}} \\
&= (1)e^0 = 1

\end{aligned}
$$



c.) $Y=X^2$ and $f_{X}(x)=30(x^2)(1-x)^2$ for $0<x<1$
Find pdf of Y

So let $y=x^2=g(x)$, then
	 $g'(x)=2x>0 \space \forall x\in (0,1) \implies monotone$
		 I think? There is probably another thing you gotta prove?
then
$g^{-1}(y)=y^{1/2}\implies f_{x}(g^{-1}(y))=30(y^{1/2})^2(1-y^{1/2})^2$
and
$\frac{d}{dx}g^{-1}(y)=\frac{1}{2}y^{-1/2}$
So

$$
f_{Y}(y)=\begin{cases}
30(y^{1/2})^2(1-y^{1/2})^2 &0<y<1 \\
0 & other
\end{cases}
$$
lets reduce
$$
\begin{aligned}
&=30(y^{1/2})^2(1-y^{1/2})^2 \\
&=15y(1-y^{1/2})^2y^{-1/2} \\
&=15y^{1/2}(1-y^{1/2})^2 \\
&=15y^{1/2}(1-2y^{1/2}+y) \\
&=15(y^{1/2}-2y+y^{3/2})

\end{aligned}

$$
reduce to this point for easier integration. So it should be this now.
$$
f_{Y}(y)=\begin{cases} 
15(y^{1/2}-2y+y^{3/2}) & 0<y<1 \\
0 & other \\

\end{cases}
$$
Lets prove this pdf integrates to 1.
$$
\begin{aligned}
&\int f_{Y}(y)dy = \int_{0}^{1}15(y^{1/2}-2y+y^{3/2})dy \\
& = 15\int_{0}^{1}y^{1/2}-2y+y^{3/2}dy \\
& = 15\left[ \frac{2}{3}y^{3/2} - y^2+\frac{2}{5}y^{5/2} \vert_{0}^{1}\right] \\
&=15\left[ \frac{2}{3}(1)^{3/2} -(1)^2+\frac{2}{5}(1)^{5/2}-0 \right] \\
&=15\left[ \frac{2}{3}-1+\frac{2}{5} \right] = 15\left( \frac{1}{15} \right) = 1

\end{aligned}

$$

### 2.2
a.) $Y=X^2$ and $f_{x}(x)=1 \space for \space 0<x<1$
Find pdf of Y
Let
	$y=x^2=g(x)$ then,
		$g'(x)=2x>0 \space \forall x \in(0,1) \implies montone$
			I really need to figure out if this is true....
So
	$g^{-1}(y)=y^{1/2}$ then, 
		$\frac{d}{dx}g^{-1}(x)=\frac{1}{2}y^{-1/2}$
Thus
$$
f_{Y}(y)=\begin{cases}
 (1)\left( \frac{1}{2}y^{-1/2} \right)&0<y<1 \\
0& other
\end{cases}
$$
b.)  $Y=-\log(x)$ and $f_{X}(x)=\frac{(n+m+1)!}{n!m!}x^n(1-x)^m\space \space 0<x<1$ and $m,n\in \mathbb{N}\cup {0}$
Find pdf of Y
Let
	$y=-\log(x)=g(x)$ then,
		$g'(x)=-\frac{1}{x}<0\space\forall x\in(0,1)\implies montone$
	and
		$g^{-1}(x)=-e^y$, so
		$\frac{d}{dx}g^{-1}(x)=-e^y$
	Thus
$$
f_{Y}(y)=\begin{cases}
\frac{(n+m+1)!}{n!m!}(-e^y)^n(1+e^y)^m &0<y<\infty \\
0 &other

\end{cases}
$$
c.)$Y=e^X$ and $f_{X}(x)=\frac{1}{\sigma^2}xe^{\frac{-(x/\sigma)^2}{2}}$for $0<x<\infty$
Find pdf of Y
Let
	$y=e^x=g(x)$ then,
		$g'(x)=e^x\space\forall x\in(0,\infty)\implies monotone$
therefore
	$g^{-1}(y)=\ln(y)$
		and
		$\frac{d}{dy}g^{-1}(y)=\frac{1}{y}$
thus
$$
f_{Y}(y)=\begin{cases}
\frac{1}{\sigma^2}\ln(y)e^{-\frac{(\ln(y)/\sigma)^2}{2}}|\frac{1}{y}|&0<y<\infty \\
0&other
\end{cases}
$$








