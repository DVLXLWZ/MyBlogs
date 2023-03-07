---
layout: post
title: Some Gaps and Examples in Intersection Theory by Fulton I
date: 2022-12-12
last_modified_at: 2023-02-26
tags: [Algebraic Geometry]
toc:  true
math: true
excerpt_separator: <!--more-->
---
This is one of a series of blogs aiming to complete some details of the examples in this book (*Intersection Theory, 2nd edition* by William Fulton[^2]) and give some comments. This blog we consider chapter 1 to chapter 6.

<!--more-->
## Part 0. Some notations
In this book we consider vector bundle as a geometric object (locally as $U\times\mathbb{A}^n$ with some cocycle condition) instead of a locally free $\mathscr{O}\_X$-module, although they are equivalent:
we may always let $E=\underline{\mathrm{Spec}}\_X\mathrm{Sym}(\mathscr{E})$ where $\mathscr{E}$ be the sheaf of sections of $E$.

Chow groups in book denoted by $A\_* (X)$ and here we denote it $\mathrm{CH}\_* (X)$ as a more modern notation. 

Here $P(E):=\underline{\mathrm{Proj}}\_X\mathrm{Sym}(\mathscr{E}^{\vee})=\mathbb{P}(\mathscr{E}^{\vee})$ where $\mathscr{E}$ be the sheaf of sections of $E$.
The Grassmannian $\mathrm{Grass}^e\_X(\mathscr{E})$ represented by 
\\[(f:T\to X)\mapsto\\{f^* \mathscr{E}\twoheadrightarrow \mathscr{Q},\mathrm{rank}(\mathscr{Q})=e\\}/\sim.\\]
Hence $P(E)=\mathrm{Grass}^{n-1}\_X(\mathscr{E}),\mathbb{P}(\mathscr{E})=\mathrm{Grass}^1\_X(\mathscr{E})$ if $\mathrm{rank}(\mathscr{E})=n$. In particuler,
$\mathbb{P}^n=\mathbb{P}((\mathscr{O}\_X^{n+1})^{\vee})=\mathrm{Grass}^n\_X(\mathscr{O}\_X^{n+1})$ and $\check{\mathbb{P}}^n:=\mathbb{P}(\mathscr{O}\_X^{n+1})=\mathrm{Grass}^1\_X(\mathscr{O}\_X^{n+1})$. We sometimes let $\mathrm{Grass}\_X(k,n):=\mathrm{Grass}\_X^k(\mathscr{O}\_X^n)$ and let $\mathrm{Grass}\_X(k,V)$ be the $k$-planes of $V$.

As in Fulton's B.5.7, Grassmannian in his book is also opposite to the Grothendieck's construction. So we will use the Fulton's notation as $G\_d(E):=\mathrm{Grass}^{r-d}\_X(E)\cong \mathrm{Grass}^{d}\_X(E^{\vee})$ where $E$ be a vector bundle of rank $r$ on $X$.

We may let $\mathscr{O}\_E(n):=\mathscr{O}\_{P(E)}(n)$.

## Chapter 1. Rational Equivalence
### Section 1.6. Alternate Definition of Rational Equivalence
**Example 1.6.3.**

### Section 1.9. Affine Bundles
**Example 1.9.1.**

## Chapter 2. Divisors
### Section 2.6. Gysin Map for Divisors
**Example 2.6.3.**(a) Let $L$ be a line bundle over $X$ with complement of zero section $L-\\{0\\}$. For $k\geq 0$, we of course get
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
$$
\begin{xy}
\xymatrix{
\mathrm{CH}_{k+1}(X) \ar[r]^{i_*} \ar[dr]_{c_1(L)\cap -} & \mathrm{CH}_{k+1}(L) \ar[d]^{\cong,i^*} \ar[r] & \mathrm{CH}_{k+1}(L-\{0\}) \ar[r] & 0\\
  & \mathrm{CH}_k(X) \ar[ur]_{\eta^*}  & & 
}
\end{xy}
$$
</p>
</body>
</html>
as after checking the cocycle condition, we get the normal bundle $N\_{X/L}\cong L$ and by Proposition 2.6(d) we get $i^* i\_* \alpha=c\_1(L)\cap\alpha$. $\blacksquare$

(b) Here $X\subset\mathbb{P}^n$ with affine cone $V\subset\mathbb{A}^{n+1}$. I think here $V$ be the **pointed affine cone**: since we have 
$X\cong\underline{\mathrm{Proj}}\_X\mathrm{Sym}(\mathscr{O}(1))$, the affine cone is $\underline{\mathrm{Spec}}\_X\mathrm{Sym}(\mathscr{O}(1))$
and the pointed affine cone is $\underline{\mathrm{Spec}}\_X\mathrm{Sym}(\mathscr{O}(1))-\\{0\\}$. $\blacksquare$

## Chapter 3. Vector Bundles and Chern Classes
### Section 3.2. Chern Classes
**Example 3.2.7.** For vector bundles $E,F$ over $X$ of rank $r,s$, we defined $c(F-E):=c(F)/c(E)=c(F)s(E)=\cdots$.
We claim that \\[c\_{s-r+1}(F-E)\cap\alpha=p\_* (c\_s(p^* F\otimes\mathscr{O}\_E(1))\cap p^* \alpha)\\]
where $\alpha\in\mathrm{CH}\_* (X)$ and $p:P(E)\to X$.
Actually we have
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
&c_{s-r+1}(F-E)\cap\alpha\\
  &=\sum_{i+j=s-r+1}c_i(F)s_j(E)\cap\alpha\\
  &=\sum_{i+j=s-r+1}c_i(F)p_*(c_1(\mathscr{O}_E(1))^{r-1+j}\cap p^*\alpha)\\
  &=\sum_{s-i=r-1+j}c_i(F)p_*(c_1(\mathscr{O}_E(1))^{r-1+j}\cap p^*\alpha)\\
  &=p_*\left(\sum_{s-i=r-1+j}c_i(p^*F)c_1(\mathscr{O}_E(1))^{r-1+j}\cap p^*\alpha\right)\\
  &=p_*\left(\sum_{i=0}^sc_{s-i}(p^*F)c_1(\mathscr{O}_E(1))^i\cap p^*\alpha\right)\\
  &=p_*\left(c_s(p^*F\otimes\mathscr{O}_E(1))\cap p^*\alpha\right).
\end{align*}
</p>
</body>
</html>
Hence well done. $\blacksquare$

**Example 3.2.13.** Here Fulton define the *Euler characteristic* as $\int\_X c\_n(T\_X)$, we need to verify that this is coincident with the original one when $X$ is projective smooth variety over $\mathbb{C}$!

By Example 3.2.5 (Borel-Serre identity), we get \\[c\_n(T\_X)=\mathrm{td}(T\_X)\sum\_{p=0}^n(-1)^p\mathrm{ch}(\bigwedge^p\Omega\_X).\\]
Use Hirzebruch-Riemann-Roch theorem (Corollary 15.2.1) to $\sum\_{p=0}^n(-1)^p\bigwedge^p\Omega\_X$ we get
\\[\int\_Xc\_n(T\_X)=\sum\_{p,q}(-1)^{p+q}h^p(X,\bigwedge^q\Omega\_X).\\]
By Hodge decomposition theorem we get
\\[\chi(X)=\sum\_{r}{(-1)}^rh^r(X(\mathbb{C}),\mathbb{C})=\sum\_{p,q}(-1)^{p+q}h^p(X,\bigwedge^q\Omega\_X)\\]
and well done. $\blacksquare$

**Example 3.2.19.**


**Example 3.2.22.** We have $\mathrm{Hilb}\_{\mathbb{P}^3}^P=\check{\mathbb{P}}^3$ where $P$ be the Hilbert polynomial of 2-planes in $\mathbb{P}^3$. Hence we get \\[0\to S\to\mathscr{O}\_{\check{\mathbb{P}}^3}^{\oplus 4}\to Q\cong\mathscr{O}\_{\check{\mathbb{P}}^3}(1)\to0.\\]
Hence let $E:=\mathrm{Sym}^2(S^{\vee}\otimes Q^{\vee})$ and consider $P(E)$. Hence the variety of conics meeting a given line is given by the vanishing of a section of $\mathscr{O}\_E(1)$.

Let $h=c\_1(Q)$, we get $1=c(\mathscr{O}\_{\check{\mathbb{P}}^3}^{\oplus 4})=c(S)(1+h)$ and hence $c(S)=1-h+h^2-h^3$. Hence we get
\\[c(S^{\vee}\otimes Q^{\vee})=\sum\_{i=0}^3(1-h)^{3-i}c\_i(S^{\vee})=1-2h+2h^2.\\]
Finally, if $\mathrm{rank}(F)=3$, we have \\[c(\mathrm{Sym}^2(F))=1+4c_1+5c_1^2+5c_2+2c_1^3+11c_1c_2+7c_3.\\]
Hence we get \\[c(E)=1-8h+30h^3-60h^3.\\]
Hence \\[s(E)=\frac{1}{1-8h+30h^3-60h^3}=1+8h+34h^2+92h^3.\\] Let $p:P(E)\to\check{\mathbb{P}}^3$.
Hence 
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
&\int_{P(E)}c_1(\mathscr{O}_E(1))^8\cap [P(E)]\\
&=\int_{\check{\mathbb{P}}^3}p_* (c_1(\mathscr{O}_E(1))^8\cap p^* [\check{\mathbb{P}}^3])\\
&=\int_{\check{\mathbb{P}}^3} s_3(E)=92.
\end{align*}
</p>
</body>
</html>
Others are the same.

### Section 3.3. Rational Equivalence on Bundles
**Example 3.3.2.** Now we get $q:P(E\oplus 1)\to X$ and $j:E\to P(E\oplus 1)$ and the universal exact sequence
\\[0\to\mathscr{O}\_{E\oplus 1}(-1)\to q^* (E\oplus 1)\to \xi\to 0.\\]
Hence we get $s^* s\_* (\alpha)=q\_* (c\_r(\xi)\cap\bar{s}\_* (\alpha))$ where $\bar{s}=j\circ s$. Hence we have
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
&q_* (c_r(\xi)\cap\bar{s}_* (\alpha))\\
&=\sum_{i=0}^r q_* (c_1(\mathscr{O}_{E\oplus 1}(1))^ic_{r-i}(q^*E)\cap\bar{s}_* (\alpha))\\
&=\sum_{i=0}^r c_{r-i}(E)q_* (c_1(\mathscr{O}_{E\oplus 1}(1))^i\cap\bar{s}_* (\alpha))\\
&=c_r(E)\cap\alpha+\sum_{i=1}^r c_{r-i}(E)q_* (c_1(\mathscr{O}_{E\oplus 1}(1))^i\cap\bar{s}_* (\alpha))\\
&=c_r(E)\cap\alpha
\end{align*}
</p>
</body>
</html>
since $c_1(\mathscr{O}\_{E\oplus 1}(1))^i\cap\bar{s}\_* (\alpha)=0$ by definition of $\bar{s}$. $\blacksquare$

## Chapter 4. Cones and Segre Classes
### Section 4.1. Segre Class of a Cone
**Example 4.1.4. (Grassmann–Plücker relations).** Here $X=\mathbb{A}^{mn}$ where $m\geq n$ with coordinates $(x\_{ij})$ and $X$ be the locus of rank $<n$ with ideal sheaf $I$ (generated by all $n$-minors of $(x\_{ij})$). Let $C=C\_XY$. For any $(i)=(i\_1,...,i\_n)$ where $1\leq i\_1<\cdots<i\_n\leq m$, let $t\_{(i)}$ be a variable and $\delta\_{(i)}$ be the corresponding minor of $(x\_{ij})$. Now consider the embedding 
\\[P(C)=\underline{\mathrm{Proj}}\_X\bigoplus\_{n\geq 0}I^n/I^{n+1}\to X\times\mathbb{P}^N\\]
given by surjection $\mathrm{Sym}\mathscr{O}\_X^{N+1}\to \bigoplus\_{n\geq 0}I^n/I^{n+1}$ as $t\_{(i)}\mapsto\delta\_{(i)}$ where $N=\binom{m}{n}-1$.

What is Plücker relations? As we all know we have the closed embedding $\mathrm{Grass}(k,n)\to\mathbb{P}^{\binom{n}{k}-1}$ given by $\mathrm{span}(w\_1,...,w\_k)\mapsto[w\_1\wedge\cdots\wedge w\_k]$ (more generally, we have $\mathrm{Grass}^e(\mathscr{E})\to\mathbb{P}\left(\bigwedge^e\mathscr{E}\right)$). Actually the Plücker relations are just the things generated the ideal sheaf of $\mathrm{Grass}(k,n)$ in $\mathbb{P}^{\binom{n}{k}-1}$. In the special case, let $W'$ be the $k$-dimensional subspace spanned by the basis of column vectors $W\_1,...,W\_k$. Let $W$ be the $n\times k$ matrix of homogeneous coordinates, whose columns are $W\_1,...,W\_k$. For any ordered sequence $1\leq i\_1<\cdots< i\_k\leq n$ of $k$ integers, let $W\_{i\_1...i\_k}$ be the determinant of the $k\times k$ matrix whose rows are the $i\_1,...,i\_k$ rows of $W$. Then, up to projectivization, $\\{W\_{i\_1...i\_k}\\}$ are the Plücker coordinates of the element $W'$ of the Grassmannian. One can show that the embedding determined by: for any $i\_1<\cdots< i\_{k-1}$ and $j\_1<\cdots< j\_{k+1}$ in $[1,n]$, we have
\\[\sum\_{l=1}^{k+1}(-1)^lW\_{i\_1...i\_{k-1}j\_l}W\_{i\_1...\hat{j}\_l...i\_{k+1}}=0.\\]

Back to our example. Hence by definition we have embeddings \\[P(C)\to X\times\mathrm{Grass}\_{k}(n,m)\to\mathbb{P}^{\binom{m}{n}-1}\\]
and $P(C)=\\{(\phi,L):\mathrm{Im}(\phi)\subset L\\}$. $\blacksquare$

### Section 4.2. Segre Class of a Subscheme
**Example 4.2.9. (Local Euler obstruction and Nash blow-up).** What is Nash blow-up? For a variety $X$ of dimension $r$ with an embedding $X\to Y$ for a non-singuler variety of dimension $n$. Consider the canonical map \\[\tau:X^{\mathrm{reg}}\to X\times\mathrm{G}\_r(TY),x\mapsto(x,T\_{X,x})\\]
and let $X':=\overline{\mathrm{Im}\tau}$. Then $\nu:X'\to X$ is called the Nash blow-up of $X$. The idea of this is that we can replace each singular point by all limiting positions of the tangent spaces at the non-singular points. (1. Nash blowing-up is locally a monoidal transformation; 2. Although the above construction uses an embedding, the Nash blow-up itself is unique up to unique isomorphism.) The more result of this and local Euler obstruction, one can read [Note on MacPherson's local Euler obstruction](https://arxiv.org/pdf/1412.3720.pdf). $\blacksquare$

### Section 4.3. Multiplicity Along a Subvariety
**Example 4.3.2. (Symmetric product of non-singular curves).** Fix a non-singular projective curve $C$ over some algebraically closed field $k$. We consider $C^d=C\times\cdots\times C$ with a canonical $C^{(d)}:=\mathfrak{S}\_d$-action. By D. Mumford's theory, the scheme (coarse moduli space) $C^d/\mathfrak{S}\_d$ exists. One can show that $C^{(d)}$ is nonsingular for all $d$ (see [Milne-Jacobian](https://www.jmilne.org/math/xnotes/JVs.pdf) Proposition 3.2. In SGA-I, purity theorem says that $V/G$ can be nonsingular only if the ramification locus is empty or has pure codimension $1$ in $V$ . This implies that $V/G$ can be nonsingular only if $V$ is a curve!) Milne also shows that $C^{(d)}$ is the fine moduli space of degree $d$-(relative) effective divisors, hence $C^{(d)}\cong\mathrm{Hilb}^d\_{C/k}$. More properties of $C^{(d)}\to \mathrm{Jac}(C)$ we refer [A-V](http://www-personal.umich.edu/~stevmatt/abelian_varieties.pdf) Theorem 25.1.

Now let $\deg D=d,\dim\|D\|=r$, we claim that $s(\|D\|,C^{(d)})=(1+h)^{g-d+r}\cap[\|D\|]$. For $d$ large, the map $u\_d:C^{(d)}\to \mathrm{Jac}(C)$ is a projective bundle $P(E)$ where $E$ is a vector bundle of rank $d+1-g$ over $\mathrm{Jac}(C)$. Hence $r=d-g$. In this case $N\_{C^{(d)}}(\|D\|)$ is tirvial, hence $s(\|D\|,C^{(d)})=[\|D\|]$ which proves the claim. For small $d$ consider $C^{(d)}\subset C^{(d+s)},E\mapsto E+sP\_0$. By some simple analysis (see Theorem 2 in section 3 in paper [Schwarzenberger][^1], he showed that $i\_d:C^{(d)}\subset C^{(d+1)}$ as a divisor correspond to $\mathscr{O}\_{C^{(d+1)}}(1)$ such that $i\_d^* \mathscr{O}\_{C^{(d+1)}}(1)=\mathscr{O}\_{C^{(d)}}(1)$) we find that the normal bundle on $\|D\|$ has Chern class $(1+h)^s$. Well done. $\blacksquare$

### Section 4.4. Linear Systems
**Example 4.4.3.** Let $X$ be an irreducible hypersurface $V\_+(F(X\_0,...,X\_{n+1}))\subset\mathbb{P}^{n+1}$. The singular locus $J\subset X$ defined by $(\frac{\partial F}{\partial X\_0},...,\frac{\partial F}{\partial X\_{n+1}})$. Taking blowing up $\pi:X':=\mathrm{Bl}\_J X\to X$ with $f:X'\to\mathbb{P}^{n+1}=P(V^{\vee})$ where 
\\[V=\mathrm{Span}\left\\{\frac{\partial F}{\partial X\_0},...,\frac{\partial F}{\partial X\_{n+1}}\right\\}\subset H^0(X,\mathscr{O}\_X(d-1))\\]
be a linear system of $X$ with base locus $J$. Define $X^{\vee}:=f(X')\subset P(V^{\vee})$ be the dual variety of $X$. Hence we have
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
\deg f_* [X']&=\int_Xc_1(\mathscr{O}(d-1))^n-\int_Jc(\mathscr{O}(d-1))^n\cap S(J,X)\\
  &=(d-1)^n\int_Xc_1(\mathscr{O}(1))^n-\int_J(1+c_1(\mathscr{O}(d-1)))^n\cap S(J,X)\\
  &=(d-1)^n\deg X-\sum_{i=0}^n\binom{n}{i}\int_Jc_1(\mathscr{O}(d-1))^i\cap S(J,X)\\
  &=d(d-1)^n-\sum_{i=0}^n\binom{n}{i}(d-1)^i\int_Jc_1(\mathscr{O}(1))^i\cap S(J,X)\\
  &=d(d-1)^n-\sum_{i=0}^n\binom{n}{i}(d-1)^i\deg(s_i),
\end{align*}
</p>
</body>
</html>
where $s_i$ be the $i$-component of $S(J,X)$. $\blacksquare$

## Chapter 5. Deformation to the Normal Cone
**No gaps.**

## Chapter 6. Intersection Products
### Section 6.1. The Basic Construction
**Example 6.1.2.** See the answer in [Calculating the distinguished varieties of intersection product](https://mathoverflow.net/questions/210068/calculating-the-distinguished-varieties-of-intersection-product). $\blacksquare$

**Example 6.1.4.**

### Section 6.3. Excess Intersection Formula
**Example 6.3.4.** After some reduction, we let $\alpha=[V],V=Y'$ and $i^!\alpha=s\_E^!\alpha=s\_{f^* E}^!\alpha$. We need to show that 
\\[j\_* s\_{f^* E}^![Y']=c\_d(f^* E)\cap [Y'].\\]

**Example 6.3.5.**

[^1]: [Schwarzenberger] Schwarzenberger. Jacobians and symmetric products[J]. Illinois Journal of Mathematics, 1963, 7(2): 257-268.

[^2]: [FulIT2nd] William Fulton. Intersection Theory, 2nd. Springer New York, NY. 1998.
