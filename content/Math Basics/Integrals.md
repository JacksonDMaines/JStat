
## Typical Integrals

### Indefinite
Let $f(x) = x^a$  where $a\in\mathbb{Z}/{\{0\}}$

$$
\int f(x)dx = \int x^adx = \frac{x^{a+1}}{a+1}+C
$$

$$
dx \to\text{what you are integrating with respect to}

$$
$$
C \to \text{when doing definite integrals don't forget this "Plus C"}
$$

## Definite
Let $f(x)$ exist then
$$
\int_{a}^{b}f(x)dx =g(x)\Big|_{a}^{b} = g(b) - g(a)
$$
No need for a "Plus C" here

# Tricks
## U-Sub
Sometimes what you are integrating with respect to makes it more complicated, so switching to a more usable variable of integration can help

Personally I think showing a U-Sub makes more sense than trying to explain it.

**Example:**
$$
Let \space f(x)=2xe^{x^2} \space solve \space \int f(x)dx = \int 2xe^{x^2}dx
$$
>[!faq]- Answer
>$$ \begin{align}
&Let \space u=x^2, \text{we now need to find the derivative of u called du} \\ \\
& du = \frac{d}{dx}x^2=2xdx \\ \\ \\
& \text{Now we have: }  \\
&u=x^2  \\
&du = 2xdx \\
 \\
&\text{Lets just plug in our u and du into the integeral. Lets first regorganize the integral } \\ \\
& \int 2xe^{x^2}dx= \int e^{x^2}\cdot 2xdx \\ \\
& \text{Can you see what the u and du replace?} \\ \\
&=\int e^udu  \\ \\
&\text{ Now we can just integrate as we would normally } \\ \\
&=e^u+C \\ \\
& \text{Now replace u} \\ \\
&=e^{x^2} + C \\ \\ \\
&\text{This is a simple U-Sub example.} \\
& \text{But U-Sub can be very useful tool for integrals that are not immediately obvious.}
\end{align} 
$$




## Integration by Parts
Integration by parts utilizes a u-sub like idea, but instead of just choosing a u you also choose a dv. Its most useful for integrals that contain a function that has a looping derivative (think $e^x$ or $sin(x)$)

How does it work? Most of the time you will see people describing integration by part as 
$$
\int udv = u\cdot v - \int vdu
$$
I don't think this is good for an initial definition. Its useful later once you understand the concepts, but its confusing at the beginning.

Rather lets think about it like this.  Let $f(x)$ and $g(x)$ exist then

$$
\int f(x)g(x)dx 
$$
Let $u=f(x)$ and $dv=g(x)dx$. Now we need to differentiate u and integrate dv. 
$$
\begin{align}
&u = f(x)  \\
&du = f'(x)dx \\
 \\
 \\
&dv = g(x)dx \\
&v = \int g(x)dx = L'(x)
\end{align}
$$
then
$$
\begin{align}
&\int f(x)g(x)dx \\
& = f(x)L(x)-\int L(x)f'(x)dx
\end{align}
$$
For indefinite integrals it works like this.
$$
\int_{a}^{b}udv = (u\cdot v)\Big|_{a}^{b}-\int_{a}^{b}vdu
$$

>[!tip]
>Its best to choose something that has a terminating derivative for u (Ex: x^2)
> and something that has a looping derivative for dv (Ex: sinx)



Lets do an example:
$$
\text{Solve the following:} \int xe^{6x}dx
$$


>[!faq]- Answer
>$$
\begin{align}
&\int xe^{6x}dx \\
&\text{Let }u=x \text{ and }dv=e^{6x}dx \\ 
& \text{then }du=1dx \text{ and }v =\int e^{6x}dx=\frac{1}{6}e^{6x} \\ \\ \\
&\int xe^{6x}dx = x\left( \frac{1}{6}e^{6x} \right)-\int \frac{1}{6}e^{6x}\cdot 1dx  \\
&=x\left( \frac{1}{6}e^{6x} \right) - \frac{1}{6}\int e^{6x}dx \\
&=x\left( \frac{1}{6}e^{6x} \right) - \frac{1}{6}\left( \frac{1}{6}e^{6x} + C \right) \\
& = \frac{x}{6}e^{6x}-\frac{1}{36}e^{6x}+C
\end{align}
$$


# Higher Order Integrals
$$
\int\int f(x,y) \, dxdy 
$$
This works just like parentheses. Do inner integral first then outer integral.
$$
\left( \int\left( \int f(x,y)dx \right)dy \right)
$$
This is 2 integrals, but its the same idea for a triple integral.

Note: You can switch the order of integration (dxdy $\to$ dydx), this sometimes make integration alot easier

## Polar Transformations
Think unit circle. Notes:
$$
\begin{align}
&\text{Cartesian} \to \text{Polar} \\
&x = r\cos(\theta) \\
&y = r\sin(\theta) \\
&r^2=x^2+y^2 \implies r =\sqrt{ x^2 +y^2}\\
 \\
&\text{Note: r is radius and }0<r<\infty \\
&\theta\text{ is a polar angle }0\leq \theta \leq 2\pi \\
 \\
 \\
& dA = r dr d\theta
\end{align}
$$

Lets do an example: 
$$
\begin{align}
&\text{Solve the following: }\int \int 2xydA \\ \\
&\text{Where D is the region between circles }\\
&\text{with radius 2 and radius 5 in the first quadrant.}
\end{align}
$$




# Trig Rules

## Easy Trick
$$
\text{Go up for integral, once at top go back to bottom}
$$
$$
\begin{aligned}
&\space \space \space \space \space Sin \\
&\space \space \space \space \space Cos \\
&-Sin \\
& -Cos


\end{aligned}
\quad \Bigg\uparrow
$$
