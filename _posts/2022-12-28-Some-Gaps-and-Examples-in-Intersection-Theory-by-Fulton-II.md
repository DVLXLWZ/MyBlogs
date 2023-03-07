---
layout: post
title: Some Gaps and Examples in Intersection Theory by Fulton II
date: 2022-12-28
last_modified_at: 2023-01-19
tags: [Algebraic Geometry]
toc:  true
math: true
excerpt_separator: <!--more-->
---
This is one of a series of blogs aiming to complete some details of the examples in this book (*Intersection Theory, 2nd edition* by William Fulton[^1]) and give some comments. This blog we consider chapter 7 to chapter 9.

<!--more-->

> Previously on these:
>
> [Some Gaps and Examples in Intersection Theory by Fulton I](https://dvlxlwz.github.io/2022/12/12/Some-Gaps-and-Examples-in-Intersection-Theory-by-Fulton-I/).

## Chapter 7. Intersection Multiplicities
### Section 7.1. Proper Intersections
**Example 7.1.1.** In the case of proper component, we claim that $i(Z,X\cdot V;Y)=(e\_WV)\_Z$. Actually $(e\_WV)\_Z$ be the coefficient of $Z$ in $\\{s(W,V)\\}\_{k-d}$ and $i(Z,X\cdot V;Y)$ be the coefficient of $Z$ in $\\{c(N)\cap s(W,V)\\}\_{k-d}$.

**Example 7.1.2.** Let $X,Y,V,W,Z$ as before and let $A=\mathscr{O}\_{Z,V}$. We claim that 
\\[i(Z,X\cdot V;Y)=\sum\_{i=0}^d\mathrm{length}\_A(H\_i(K\_* (a\_1,...,a\_d)))=e\_A(a\_1,...,a\_d).\\]

**Example 7.1.12.** For $X=V=E$ and $Y=\mathrm{Bl}\_qS$ where $S$ be a surface with exceptional divisor $E$. Then $Z=E$ be the only distinguished variety, hence
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
&X\cdot V=c_1(g^*N_{X/Y})\cap [X]\\
&=c_1(\mathscr{O}(-1))\cap [X]\\
&=-c_1(\mathscr{O}(1))\cap [X]=-[p]
\end{align*}
</p>
</body>
</html>
where $p\in E$. $\blacksquare$

## Chapter 8. Intersections on Non-singular Varieties
### Section 8.1. Refined Intersections
**Corollary 8.1.1.**

**Corollary 8.1.2.** Using Corollary 8.1.1 to $\gamma\_f:\Gamma\_f\to X\times Y$, we cannot get $x\cdot\_fy=(x\times y)\cdot[\Gamma\_f]$ (actually their support is not correct!). Actually, if we let $\delta:X\to\Gamma\_f$ be the inclusion, then
\\[x\cdot\_fy=\delta^!((x\times y)\cdot[\Gamma\_f])\\] and well done. $\blacksquare$

**Example 8.1.5.** I think this is **meaningless** and we do not use the Theorem 6.4?? $\blacksquare$

**Example 8.1.6.** Here we **should let $E$ over $Y'$ and let $f':X'\to Y'$**, then we **should have:**
\\[x\cdot\_f(c\_i(E)\cap y)=(c\_i((f')^* E)\cap x)\cdot\_fy.\\]
(Or the domain of these classes are **NOT CORRECT**.) And we need **NOT** use the Proposition 6.3. We need to use **Example 3.2.8**. Let $p,q:X'\times Y'\to X',Y'$ be the projections, then we get
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
&x\cdot_f(c_i(E)\cap y)=\gamma_f^!(x\times(c_i(E)\cap y))\\
&=\gamma_f^!(c_i(q^*E)\cap(x\times y))
\end{align*}
</p>
</body>
</html>

and 

<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
&(c_i((f')^* E)\cap x)\cdot_fy=\gamma_f^!((c_i((f')^* E)\cap x)\times y)\\
&=\gamma_f^!(c_i(p^*(f')^* E)\cap (x\times y))=\gamma_f^!(c_i(q^* E)\cap (x\times y))
\end{align*}
</p>
</body>
</html>
and well done. $\blacksquare$

**Example 8.1.12.** **AGAIN!** The domains of $\Delta\cdot\Delta$ and $c\_n(T\_X)\cap[X]$ are never the same! One may let $\Delta=X$ with diagonal map $\delta:\Delta\to X\times X$, then $\delta^!\Delta=c\_n(T\_X)\cap[X]$ is trivial, then by Corollary 8.1.2, well done. $\blacksquare$

**Example 8.1.13.**

### Section 8.2. Intersection Multiplicities
**Example 8.2.2.**

### Section 8.3. Intersection Ring
**Example 8.3.4.** Let $E$ be a vector bundle of rank $r$ over a non-singular variety $Y$. Let $\zeta=c\_1(\mathscr{O}\_E(1))$ over $P(E)$. Let $p:P(E)\to Y$ be the projection. Then we claim that
\\[\mathrm{CH}^* (P(E))\cong \frac{\mathrm{CH}^* (Y)[\zeta]}{\zeta^r+c\_1(E)\zeta^{r-1}+\cdots+c\_r(E)}.\\]
By Theorem 3.3, we get $\mathrm{CH}^* (P(E))\cong\bigoplus\_{i=0}^{r-1}\zeta^i\mathrm{CH}^* (Y)$. Hence there exists a monic polynomial $f$ of degree $r$ such that \\[\mathrm{CH}^* (P(E))\cong\mathrm{CH}^* (Y)[\zeta]/(f).\\]
Here we need to identify the polynomial $f$. Consider the universal exact sequence
\\[0\to\mathscr{O}\_E(-1)\to p^* E\to\xi\to0,\\]
then $c(\mathscr{O}\_E(-1))c(\xi)=c(p^* E)$. First we have $c(\mathscr{O}\_E(-1))=1-\zeta$. Identifying $\mathrm{CH}^* (Y)$ with $p^* \mathrm{CH}^* (Y)$, we get
\\[c(\xi)=c(E)c(\mathscr{O}\_E(-1))^{-1}=c(E)(1+\zeta+\zeta^2+\cdots).\\]
As $\mathrm{rank}(\xi)=r-1$, we get
\\[0=c\_r(\xi)=\zeta^r+c\_1(E)\zeta^{r-1}+\cdots+c\_r(E)!\\]
Hence $f$ have been determined and we get 
\\[\mathrm{CH}^* (P(E))\cong \frac{\mathrm{CH}^* (Y)[\zeta]}{\zeta^r+c\_1(E)\zeta^{r-1}+\cdots+c\_r(E)}.\\]
Well done. $\blacksquare$

**Example 8.3.9.**

**Example 8.3.14.** First we have
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
n(w)&:=\int_Xh^w\cap[W]=\int_{P(V)}f_*(h^w\cap[W])\\
  &=\int_{P(V)}c_1(\mathscr{O}_V(1))^w\cap f_*[W]\\
  &=\deg(W/f(W))\int_{P(V)}c_1(\mathscr{O}_V(1))^w\cap[f(W)]\\
  &=\deg(W/f(W))\deg(f(W)).
\end{align*}
</p>
</body>
</html>

Next, since 

<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
&\int_Xh\cdot c_1(p^*L)^j\cap p^*[y]\cdot[W]\\
&=\int_Xh\cdot p^*(c_1(L)^j\cap [y])\cdot[W]=0
\end{align*}
</p>
</body>
</html>
for $j>0$, we have

<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
k(W)&:=\int_X\zeta^{w-1}[X_y]\cdot[W]\\
  &=\int_X(h-c_1(p^*L))^{w-1}[X_y]\cdot[W]\\
  &=\int_Xh^{w-1}p^*[y]\cdot[W].
\end{align*}
</p>
</body>
</html>
We claim that \\[[W]=k(W)h^{d-w}+p^* (\alpha)h^{d-w-1},\\]
where $\alpha\in\mathrm{CH}\_0(Y)$ with $\deg\alpha=n(W)-k(W)n(X)$.

### Section 8.4. Bezout's Theorem (Classical Version)
**Example 8.4.2.(c).** For the first method, let $[\Delta]=\sum\_{i=0}^na\_is^it^{n-i}$. Easy to get that $a\_i=\deg([\Delta]\cdot s^{n-i}t^i)$. If $L$ and $M$ are general linear subspaces of codimension $n-i$ and $i$, respectively as the text. Hence $[L\times M]=s^{n-i}t^i$. Hence 
\\[a\_i=\deg([\Delta]\cdot s^{n-i}t^i)=\sharp(\Delta\cap(L\times M))=\sharp(L\cap M)=1.\\]
Hence well done. For the second method, this is just calculation. $\blacksquare$

**Example 8.4.4.** Let $V\subset\mathbb{P}^n\times\mathbb{P}^m$ of dimension $k$ with \\[[V]=\sum\_{i+j=k}a\_{ij}s^{n-i}t^{m-j}.\\]
Define $V'\subset\mathbb{P}^{n+m+1}$ as the text, hence $\dim V'=k+1$ and we claim that $\deg V'=\sum\_{i+j=k}a\_{ij}$.

**Some Remarks of Example 8.4.5.** This example can generalized as: for $V\_1,...,V\_r\subset\mathbb{P}^n$ as subvarieties and let $J(V\_1,...,V\_r)\subset\mathbb{P}^{r(n+1)-1}$ be the joint variety of them. Let $L$ be the standard linear space as in the example, then 
\\[V\_1\cdot...\cdot V\_r=L\cdot J(V\_1,...,V\_r).\\]
So this example **turns intersection products of several subvarieties in projective space into the intersection of a subvariety and a linear space**. As $L=\bigcap\_{i=1}^t H\_i$ where $H\_i$ are hyperplanes, then by induction, we **sometimes can just consider the case of intersection of a subvariety and a hyperplane**! $\blacksquare$

**Some Remarks of Example 8.4.8.** By Example 8.4.5 and Example 8.2.6, we get **the intersection multiplicity over a non-singular variety can be determined by intersection multiplicity of varieties of complementary dimension in $\mathbb{P}^n$ with one factor a linear space**. $\blacksquare$

**Example 8.4.13. (Resultants).** For $d\_i$, then moduli space of hypersurfaces of degree $d\_i$ in $\mathbb{P}^n$ is 
\\[\mathrm{Hilb}^{P\_i}\_{\mathbb{P}^n}\cong\mathbb{P}(\Gamma(\mathbb{P}^n,\mathscr{O}(d)))=\mathbb{P}^{m\_i},\\]
 as in section 4.3.2 of [Ser06][^2] where $P\_i(z)=\binom{n+z}{n}-\binom{n+z-d\_i}{n}$ and $m\_i=\binom{n+d\_i}{n}-1$. $\blacksquare$

## Chapter 9.Excess and Residual Intersections
### Section 9.1. Equivalence of Connected Component
**Example 9.1.1.** Easy to see that \\[(X\_1\cdot...\cdot X\_r)^Z=\sum\_{i=1}^rX\_i\cdot s(Z,Y)\_1+s(Z,Y)\_0.\\] If the curve $Z$ be the complete intersection of Cartier divisors $D\_1,...,D\_{r-1}$, then $N\_ZY=\bigoplus\_{i=1}^{r-1}\mathscr{O}(D\_i)$, hence
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
s(Z,Y)&=c(N_ZY)^{-1}\cap[Z]=c\left(\bigoplus_{i=1}^{r-1}\mathscr{O}(D_i)\right)^{-1}\cap[Z]\\
  &=\prod_{i=1}^{r-1}c\left(\mathscr{O}(D_i)\right)^{-1}\cap[Z]=\prod_{i=1}^{r-1}(1+c_1(\mathscr{O}(D_i)))^{-1}\cap[Z]\\
  &=\prod_{i=1}^{r-1}(1-c_1(\mathscr{O}(D_i)))\cap[Z]=\left(1-\sum_{i=1}^{r-1}c_1(\mathscr{O}(D_i))\right)\cap[Z]\\
  &=[Z]-\sum_{i=1}^{r-1}D_i\cdot [Z].
\end{align*}
</p>
</body>
</html>
Others are trivial, well done. $\blacksquare$

**Example 9.1.5.** We have 
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
&(X_1\cdot...\cdot X_r)^Z=\left\{\prod_{i=1}^rc(N_{X_i}\mathbb{P}^r)\cap s(Z,\mathbb{P}^r)\right\}_0\\
&=s(Z,\mathbb{P}^r)_0+\sum_{i=1}^rc_1(N_{X_i}\mathbb{P}^r)\cap s(Z,\mathbb{P}^r)_1\\
&+\sum_{i,j}c_1(N_{X_i}\mathbb{P}^r)\cdot c_1(N_{X_j}\mathbb{P}^r)\cap s(Z,\mathbb{P}^r)_2\\
&=s(Z,\mathbb{P}^r)_0+\sum_{i=1}^rc_1(\mathscr{O}(n_i))\cap s(Z,\mathbb{P}^r)_1\\
&+\sum_{i,j}c_1(\mathscr{O}(n_i))\cdot c_1(\mathscr{O}(n_j))\cap s(Z,\mathbb{P}^r)_2\\
&=s(Z,\mathbb{P}^r)_0+nc_1(\mathscr{O}(1))\cap s(Z,\mathbb{P}^r)_1+n^2c_1(\mathscr{O}(1))^2\cap s(Z,\mathbb{P}^r)_2
\end{align*}
</p>
</body>
</html>
where $c\_i:=c\_i(T\_Z)$ and $n=\sum\_{i=1}^rn\_i$. Now we need to determine $s(Z,\mathbb{P}^r)$. Actually we have

<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
s(Z,\mathbb{P}^r)&=c(T_{\mathbb{P}^r}|_Z)^{-1}c(T_Z)\cap[Z]\\
&=[Z]+(c_1(T_Z)-c_1(T_{\mathbb{P}^r}|_Z))\cap[Z]\\
&+(c_2(T_Z)-c_1(T_{\mathbb{P}^r}|_Z)c_1(T_Z)+c_1(T_{\mathbb{P}^r}|_Z)^2-c_2(T_{\mathbb{P}^r}|_Z))\cap[Z].
\end{align*}
</p>
</body>
</html>
Hence we get

<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
&(X_1\cdot...\cdot X_r)^Z=n^2c_1(\mathscr{O}(1))^2\cap [Z]+nc_1(\mathscr{O}(1))(c_1-c_1(T_{\mathbb{P}^r}))\cap[Z]\\
&+(c_2-c_1c_1(T_{\mathbb{P}^r})+c_1(T_{\mathbb{P}^r})^2-c_2(T_{\mathbb{P}^r}))\cap[Z].
\end{align*}
</p>
</body>
</html>
Now we claim that $c\_k(T_{\mathbb{P}^r})\cap-=\binom{r+1}{k}c\_1(\mathscr{O}(1))^k\cap-$. By Euler sequence and Whitney formula, we get

<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
c(T_{\mathbb{P}^r})&=c(\mathscr{O}(1))^{r+1}=(1+c_1(\mathscr{O}(1)))^{r+1}\\
&=\sum_{i=0}^{r+1}\binom{r+1}{i}c_1(\mathscr{O}(1))^i.
\end{align*}
</p>
</body>
</html>
Hence as we get the claim. Finally, by Bezout Theorem and some easy computation, we well done. $\blacksquare$

**Example 9.1.8.** We all know that the fine moduli space of plane conics is $\mathrm{Hilb}\_{\mathbb{P}^2}^{2t+1}\cong\mathbb{P}^5$. Pick $x\_0,x\_1,x\_2$ be the coordinates of $\mathbb{P}^2$ and then the conics are defined by \\[f(x\_0,x\_1,x\_2)=ax\_0^2+bx\_0x\_1+cx\_1^2+dx\_0x\_2+ex\_1x\_2+fx\_2^2.\\]
That is, we can identify this curve with $[a:b:c:d:e:f]\in\mathbb{P}^5$. After some computation, we can show that the condition of tangent to some fixed line will formed a quadric hypersurface! (More simply, one can see that the conics contain a fixed point will formed a hyperplane and if five fixed points in general position, then these five hyperplanes is a single point! This shows that these five points determined a unique conic!) This computation also tell us that if $l\_1,...,l\_5$ are lines of general position in $\mathbb{P}^2$, then the Veronese surface $Z$ is a components of $\bigcap H\_{l\_i}$.

Now we find that $\deg(H\_{l\_1}\cdot...\cdot H\_{l\_5})=32$ and we have
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
&\deg(H_{l_1}\cdot...\cdot H_{l_5})^Z\\
&=\deg\left\{\prod_{i=1}^5c(N_{H_{l_i}}\mathbb{P}^5)\cap s(Z,\mathbb{P}^5)\right\}_0\\
&=\deg\left\{(1+c_1(\mathscr{O}_{\mathbb{P}^5}(2)))^5\cap s(Z,\mathbb{P}^5)\right\}_0\\
&=\int_{Z}(1+c_1(\mathscr{O}_{\mathbb{P}^5}(2)|_Z))^5\cap s(Z,\mathbb{P}^5)\\
&=\int_{Z}(1+c_1(\mathscr{O}_{\mathbb{P}^2}(4)))^5(1-9h+51h^2)\\
&=\int_{Z}(1+4h)^5(1-9h+51h^2)=31
\end{align*}
</p>
</body>
</html>
where $h=c\_1(\mathscr{O}\_{\mathbb{P}^2}(1))$. We should note that, here $Z$, the Veronese surface means <mark>the locus of double lines (by some very easy computation)!</mark> What will happend in $Z$? <mark>Actually, the elements in $Z$ has equations are simply the square of the equation of a line. If one of
these double lines meets a conic at a point, then because it is cut out by the square of the line, the intersection multiplicity is automatically at least two, so they are counted as tangent, no matter if the underlying reduced line is tangent to the conic.</mark> Hence we need to kill them, and there exists $32-31=1$ residue point outside of $Z$. Hence **there is a unique conic tangent to these five lines**. $\blacksquare$

**Example 9.1.9. (3264 for Char$\neq 2$).** The same reason in the discussion in **Example 9.1.8**, we need to **kill the things belong to $Z$**! First, using the method of **Example 9.1.6** (that is, using the blowing up to express the segre classes), we can find that
\\[\deg(H\_{D\_1}\cdot...\cdot H\_{D\_5})^Z=\int\_Z(1+12h)^5(8-144h+1632h^2)=4512.\\]
With more conditions, we now assume that the points in $\bigcap H\_{D\_i}$ outside $Z$ are **isolated**! Hence \\[\sum\_{C}i(C)=6^5-4512=3264.\\]
When $D\_i$ are in the general position, then $i(C)=1$, hence there are $3264$ conics tangent to $D\_i$.

Keeping the isolated condition, we actually have $i(C)=\prod\_{i=1}^5(4-\sharp(C\cap D\_i))$. 
One can have more situations and more results as follows:

![](/my_pics/2022-12-28-2.png)
taken from the paper [EAGC][^3].

For $3264$, there are many methods. After blowing up, we consider the strict transform $H'\_{D\_i}$ and just need to compute $\prod[H'\_{D\_i}]$, such as [EAGC][^3] and famous book [3264EH][^4]. $\blacksquare$

**Example 9.1.14.** The *proper immersion* $f:X\to Y$ of non-singular varieties here **is not the schematically cloed immersion**, it means **$f$ is proper and induce the injection of tangent spaces of all points of $X$**. So this is the *traditional immersion* we learned in differential geometry.

Now we need to show \\[ [X\_k]=f^* [Y\_{k-1}]-c\_d(v\_f)\cap [X\_{k-1}].\\]
Actually,

### Section 9.2. Residual Intersection Theorem
**Example 9.2.7.** Instead  of blowing up $\bigcap\_{i<j}(Z\_i\cap Z\_j)$, we should blowing up $\bigcup\_{i<j}(Z\_i\cap Z\_j)$ and use Proposition 9.2 and Proposition 4.2. $\blacksquare$

### Section 9.3. Double Point Formula
**Example 9.3.3.(c)(d).** I do not know what are the meaning of these things???

**Example 9.3.5.**

**Example 9.3.11.** Actually we need to find a non-singular complete surface $X$ with the same properties in Example 9.3.7 over $\overline{X}$ (we may use the resolution of singularities of surfaces in any characteristic). Then we can find that 
\\[(V\_{p\_1}\cdot V\_{p\_1}\cdot\overline{X})^S=s(S,\overline{X})\_0+2(d-1)c\_1(\mathscr{O}(1))\cap s(S,\overline{X})\_1\\]
and then we get the degree is $(3d-4)e-3t+2\nu$. $\blacksquare$

**Example 9.3.13.** For $X^n\subset\mathbb{P}^N$ and linear projections $f\_m:X^n\to\mathbb{P}^m$. Hence by pure calculation we have
\\[H\cdot\mathbb{D}(f\_m)-\mathbb{D}(f\_{m+1})=\mathbb{R}(f\_m)\\]
where $H=c\_1(\mathscr{O}\_X(1))$. If $N\leq 2n$ and $f\_m$ is unramified, then $\mathbb{R}(f\_m)=\mathbb{R}(f\_{m+1})\cdots =\mathbb{R}(f\_{2n-1})=0$ by projections. Hence $H^{2n-m}\cdot \mathbb{D}(f\_m)=\mathbb{D}(f\_{2n})$. As $N\leq 2n$ we get $\mathbb{D}(f\_{2n})=0$. Hence $\mathbb{D}(f\_m)=0$ by the Chow ring structure of projective space! Well done. These are the main results in [Johnson78][^5]. $\blacksquare$


[^1]: [FulIT2nd] William Fulton. Intersection Theory, 2nd. Springer New York, NY. 1998.

[^2]: [Ser06] E. Sernesi. Deformations of algebraic schemes. Springer Berlin, Heidelberg. 2006.

[^3]: [EAGC] Andrew Bashelor, Amy Ksir, and Will Traves. Enumerative Algebraic Geometry of Conics.

[^4]: [3264EH] David Eisenbud, Joe Harris. 3264 and All That, A Second Course in Algebraic Geometry. 2016.

[^5]: [Johnson78] Kent W. Johnson. Immersion and embedding of projective varieties. Acta Mathematica. 1978.

