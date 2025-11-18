# Lecture 12: Bivariate Transformations

## 1 Basic Distribution Function Approach involving two r.v.

Example 1 LetX,Y denote a random sample of size 2 from anExp(1) distn.i.e.X,Y i.i.d.  
Find the p.d.f ofU=X+Y

Example 2 X,Y i.i.d. Uniform (0,1). Find p.d.f ofU=XY

Example 3

```
fX,Y(x,y) =
```

#### {

```
e−x, 0 ≤y≤x <∞
0 , else
```

1. IfU=X−Y, find the p.d.f ofU
2. IfU= 2X−Y, find the p.d.f ofU.

## 2 Bivariate Transformations

(U,V) is a function of (X,Y). (U,V) =g(X,Y) whereg:R^2 →R^2 .Given the distribution of (X,Y), find the  
distribution of (U,V).

### 2.1 First principles

```
x
```

```
y
```

```
u
```

```
v
B
```

Defineg−^1 (B) ={(x,y) :g(x,y)∈B}, for any setB⊂R^2.  
Then,

Formula for joint density  
Suppose:

1. (X,Y) has a joint pdffX,Y(x,y).
2. gis 1-to-1 and “smooth” fromA={(x,y) :fX,Y(x,y)> 0 }toB= image ofAunder the map  
    g={(u,v) : (u,v) =g(x,y) for some (x,y)∈A}

Thenghas an inverseh=g−^1 andhis also smooth.  
Notation:Letg= (g 1 ,g 2 ) withu=g 1 (x,y) andv=g 2 (x,y) andh= (h 1 ,h 2 ) withx=h 1 (u,v) andy=h 2 (u,v)  
Result:If 1 and 2 are true, then (U,V) has a joint pdf given by

whereJis the Jacobian of the inverse transformationh.|J|is the absolute value ofJ.

### 2.2 The Jacobian

wherex=h 1 (u,v),y=h 2 (u,v).  
Comments:

1. fU,V(u,v) =fX,Y

#### (

```
h 1 (u,v),h 2 (u,v)
```

#### )

```
|J|for (u,v)∈Bis the “vector” version offY(y) =fX
```

#### (

```
g−^1 (y)
```

#### )∣∣∣

#### ∣

```
d
dyg
```

− (^1) (y)

#### ∣∣

#### ∣∣

```
fory∈Y.
```

2. fX,Y

#### (

```
h 1 (u,v),h 2 (u,v)
```

#### )

```
is simplyfX,Y(x,y) re-expressed in terms ofuandv. Just replacex andyby
expressions in terms ofuandv.
```

### 2.3 Heuristic derivation of the density of(U, V) =g(X, Y)

Let (u,v) be a particular point in the (U,V) plane. Suppose the functiongmaps (x,y) to the point (u,v) (so that  
(x,y) =h(u,v) whereh=g−^1 ). LetAbe a small (infinitesimal) region containing (x,y). SupposegmapsAinto  
the small regionBcontaining (u,v).  
Then:

We also know:

and the approximations can be made as accurate as we please by making the areas sufficiently small.  
Equating the two expressions leads to

so that

This ratio of areas is (in the limit of areas going to zero) just the absolute value of the Jacobian|J(u,v)|of the  
inverse transformationh, which tells us the amount of contraction or expansion produced by the mappinghat  
the point (u,v).  
Thus we have:

as desired.

### 2.4 Example:

(X,Y) with joint pdffX,Y(x,y) = 6(1−x−y)ID(x,y), whereD={(x,y) :x > 0 ,y > 0 ,x+y < 1 }  
Define (U,V) =g(X,Y) byU=−log(1−X) =g 1 (X,Y),V = 1 −YX=g 2 (X,Y). Find joint pdffU,V(u,v).

(1) What are the supports of (X,Y) and (U,V)?  
AsXranges from 0 to 1,U=−log(1−X) ranging from 0 to∞.  
For fixedXbetween 0 and 1,V = 1 −YX ranges from 0 to 1 asY ranges from 0 to 1−X.  
Thus the supports are

(2) Find the inverse transformation.

(3) Find the Jacobian of the inverse transformationh= (h 1 ,h 2 ).

(4) The joint pdf is now given by

Comments:  
The marginals forUandV are:

Note that  
fU,V(u,v) =fU(u)fV(v) for allu,v(that is, for−∞< u <∞and −∞< v <∞):

```
6(1−v)e−^3 uI(0,∞)×(0,1)(u,v) =
```

#### (

```
3 e−^3 uI(0,∞)(u)
```

#### )(

```
2(1−v)I(0,1)(v)
```

#### )

#### .

ThusUandV are independent r.v.’s.  
We can see this by inspection (using the following lemma) directly from (∗).

Lemma:IffX,Y(x,y) =cp(x)q(y) for−∞< x <∞and−∞< y <∞, thenXandY are independent r.v.’s  
with marginal densities found by “normalizing”p(x) andq(y).  
Going back to (∗):

fU,V(u,v) = 6(1−v)e−^3 u, 0 < u <∞, 0 < v < 1  
=cp(u)q(v) for allu,v,  
wherec= 6,p(u) =e−^3 uI(0,∞)(u), andq(v) = (1−v)I(0,1)(v).  
ThusUandV are independent.  
If you don’t like indicator functions, modify the lemma as follows.  
Lemma:If the support offX,Y(x,y) is a Cartesian product set, and on this support

fX,Y(x,y) =cp(x)q(y),  
thenXandY are independent.  
A more precise and detailed wording:  
Lemma:If

```
fX,Y(x,y) =
```

#### {

cp(x)q(y), (x,y)∈A×B,  
0 , otherwise,  
thenXandY are independent, and

```
fX(x) =ap(x) forx∈A
fY(y) =bq(y) fory∈B
```

wherea,bare normalizing constants.

### 2.5 Example:

SupposeX,Y are i.i.d.N(0,1). Define (R,Θ) as the polar coordinates of (X,Y):

```
x
```

```
y
```

```
r
```

```
(x,y)
```

```
θ
```

Then

```
R=
```

#### √

```
X^2 +Y^2 , Θ = sin−^1
```

#### ( Y

#### √

#### X^2 +Y^2

#### )

```
or = tan−^1
```

#### (Y

#### X

#### )

#### .

DefineS=R^2. Find the joint pdf of (S,Θ).

The technique we used is generally useful: to find the distribution ofU = function(X,Y), introduce another  
convenient random variableV = function(X,Y), then find the joint pdf of (U,V) and integrate overV.

## 3 Distributions of Sums and Ratios

IfXandY have joint pdffX,Y(x,y), then  
(1)Z=X+Y has pdf

```
fZ(z) =
```

#### ∫∞

```
−∞
```

```
fX,Y(x,z−x)dx,
```

(2)Z=Y/Xhas pdf

```
fZ(z) =
```

#### ∫∞

```
−∞
```

```
|x|fX,Y(x,zx)dx.
```

WhenX,Y are independent,

```
fX,Y(x,z−x) =fX(x)fY(z−x), fX,Y(x,zx) =fX(x)fY(zx).
```

In this case (1) is known as a ‘convolution integral’ or as the ‘convolution of two densities’.

“Formula” approach forY/X  
Define the transformation  
U=X  
V =XY

#### (

```
=g 1 (X,Y)
=g 2 (X,Y)
```

#### )

with inverse transformation  
X=U  
Y =U V

#### (

```
=h 1 (U,V)
=h 2 (U,V)
```

#### )

The mapping (X,Y)7→(U,V) is 1-to-1 from

```
A={(x,y) :x 6 = 0} onto B={(u,v) :u 6 = 0}.
```

The Jacobian of the inverse transformation is∣  
∣∣  
∣∣  
∣∣

```
∂x
∂u
```

```
∂y
∂u
∂x
∂v
```

```
∂y
∂v
```

#### ∣∣

#### ∣∣

#### ∣∣

#### ∣

#### =

#### ∣∣

#### ∣∣

#### ∣

```
1 v
0 u
```

#### ∣∣

#### ∣∣

```
∣=u.
```

so that  
fU,V(u,v) =fX,Y(u,uv)|u| foru 6 = 0,  
and

```
fV(v) =
```

#### ∫∞

```
−∞
```

```
fU,V(u,v)du=
```

#### ∫∞

```
−∞
```

```
|u|fX,Y(u,uv)du.
```

“Formula” approach:X+Y:

```
(X,Y) (U,V)
U=X
V =X+Y
```

#### }

```
many other choices
```

Get joint densityfU,V(u,v).  
Integrate oututo getfV(v).

“First principles”:  
(1) FindFZ(z) whereZ=X+Y,

(2) FindFZ(z) whereZ=Y/X(AssumefX(x) = 0 forx <0)

Caution:When applying

```
fZ(z) =
```

#### ∫∞

```
−∞
```

```
fX,Y(x,z−x)dx,
```

you must think carefully about where the integrand is positive and where it is zero.

Example:SupposeX,Y independent with

fX(x) =αe−αx forx > 0 , fY(y) =βe−βy fory > 0.  
ThenZ=X+Y has density

Example:IfX,Y are i.i.d. with common densityf(x) = 6x(1−x), 0 < x < 1 ,find the density ofZ=X+Y.