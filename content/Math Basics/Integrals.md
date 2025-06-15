
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
>$$
\begin{align}
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
