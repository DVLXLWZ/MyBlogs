---
layout: post
title: Some Remarks of the Kollar and Mori's Birational Geometry of Algebraic Varieties I
date: 2023-01-10
last_modified_at: 2023-01-18
tags: [Algebraic Geometry]
toc:  true
math: true
excerpt_separator: <!--more-->
---
This blog aim to give some remarks and complete some details in this book (Kollar and Mori's Birational Geometry of Algebraic Varieties). I will read first five chapters of this book. This is the first blog from chapter 1 to chapter 2.
<!--more-->

## Chapter 1. Rational Curves and the Canonical Class
### Section 1.1. Finding Rational Curves when $K\_X$ is Negative
**Theorem 1.10.** For the deformation space of maps $f:C\to X$, if we consider the deformation space which fixed points $p\_1,...,p\_k$, then one can show that
\\[\dim(\mathrm{DefSpace})\geq\chi(C,f^* T\_X\otimes\mathscr{I}\_{p\_1+...+p\_k}).\\]
If $C$ smooth (at least at $p\_i$), then by [Tag 0AYV](https://stacks.math.columbia.edu/tag/0AYV), we get
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
&\dim(\mathrm{DefSpace})\geq\chi(C,f^* T_X\otimes\mathscr{O}(-p_1-...-p_k))\\
&=\chi(C,f^* T_X)-k\dim X\\
&=-(f_* (C)\cdot K_X)+(1-g(C)-k)\dim X
\end{align*}
</p>
</body>
</html>
and well done. $\blacksquare$

### Section 1.3. The Cone of Curves of Smooth Varieties
**Definition 1.15.** More properties of extremal faces and rays we refer chapter 18 (especially Theorem 18.5) in  book [Convex97][^8] which is important for us to read the Mori's theory. $\blacksquare$

**Theorem 1.24.** At the last step, in the process of proving $\overline{NE}(X)\_{K\_X\geq 0}+\sum\_i\mathbb{R}\_{\geq 0}[C\_i]$ is closed, one can get that these $\mathbb{R}\_{\geq 0}[C\_i]$ are extremal rays. $\blacksquare$

### Section 1.4. Minimal Models of Surfaces
**Theorem 1.28.** The second paragraph of the case $C^2=0$. Easy to see that we must have $k[C]=\sum a\_i[C\_i]=:F$ in $R\subset \overline{NE}(X)$ where $k\neq 0$ by checking intersection numbers. As $Z$ be a smooth curve, we get $\mathrm{cont}\_R:X\to Z$ is flat (as over Dedekind domain, flat iff torsion-free). Hence we have $k=1$ and hence $[C]=\sum a\_i[C\_i]$!

For more methods, let $\sum a\_i[C\_i]=:F$. As $R$ be a extremal ray, we get $[C\_i]\in R$ for all $i$. We find that $a\_iC\_i^2=C\_i\cdot (F-\sum\_{j\neq i}C\_j)$. As $C\_i\cdot F=0$, we get $a\_iC\_i^2=-\sum\_{j\neq i}C\_i\cdot C\_j\leq 0$. If $F$ is reducible, then $C\_i^2<0$ since the fibers are connected. As $c\_i^2=0$, we get $F$ is irreducible. Hence we also can get $F=aD$ for an integral curve $D$. $\blacksquare$

## Chapter 2. Introduction to the Minimal Model Program
### Section 2.3. Singularities in the Minimal Model Program
**Definition 2.25.** Here they just defined $a(E,X,\Delta)$ for some irreducible **exceptional** divisor over $X$ (**that is, $\mathrm{codim}\_X(\mathrm{center}\_XE)\geq 2$**). But actually this book told us that by definition we have $a(D\_i,X,\Delta)=-a\_i$ and $a(D,X,\Delta)=0$ for these **non-exceptional** divisor! Although these claim are very intuitive, we cannot do this AT ALL! Actually, following Definition 2.4 in the new book [SMMP][^2] (also by Kollar!), we need to **DEFINE** $a(D,X,\Delta):=-\mathrm{coeff}\_D \Delta$ for any non-exceptional divisor $D\subset X$! $\blacksquare$

**Lemma 2.27.** In fact, by definition one can see that
\\[a(E,X,\Delta)=a(E,X,\Delta+\Delta')+\mathrm{coeff}\_E f^* \Delta'\\]
and well done. $\blacksquare$

**Lemma 2.29.** Let $Y:=\mathrm{Bl}\_Z X$ with $p:Y\to X$. We first let $Z$ is a smooth subvariety of codimension $k$ in $X$, then by Exercise II.8.5(b) in [Har77][^1] we get 
\\[K\_Y=p^* K\_X+(k-1)E.\\]
Hence we get \\[p^* (K\_X+\Delta)=K\_Y+p^{-1}\_* \Delta+(1-k+\mathrm{mult}\_Z\Delta)E\\]
and we have $a(E,X,\Delta)=k-1-\mathrm{mult}\_Z\Delta$ and well done.

When $Z\subset X$ just a subvariety of codimension $k$, as for now $E$ be a component of the exception divisor which **dominates** $Z$, then we can replace $X$ with any open subscheme that **contains the generic point of $Z$**. Hence we can replace $X$ by $X\backslash\mathrm{Sing}(Z)$ and back to the smooth case! $\blacksquare$

**Corollary 2.31.** (1) Here fixed a birational $f:Y\to X$, we let \\[\Delta\_Y=f\_* ^{-1}\Delta-\sum\_{E\_i,f-\mathrm{exceptional}}a(E\_i,X,\Delta)E\_i\\]
Pick $Z\_0$ of codim $2$ subvariety in $E$ which not in any other $f$-exceptional divisors and not in $f^{-1}\_* \Delta$. Hence for $E\_k\subset Y\_k$, inductively we get
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
&a(E_k,Y,\Delta_Y)=1-\mathrm{mult}_{Z_{k-1}}\Delta_Y\\
&=1-\mathrm{mult}_{Z_0}\left(f_*^{-1}\Delta-\sum_{E_i,f-\mathrm{exceptional}}a(E_i,X,\Delta)E_i\right)\\
&=1-\mathrm{mult}_{Z_0}\left(-a(E_{k-1},X,\Delta)E_{k-1}-a(E,X,\Delta)E\right)\\
&=1+(1-k)c+(-1-c)=-kc
\end{align*}
</p>
</body>
</html>
and well done. $\blacksquare$

(3) Where the snc divisor we used? *First:* As $\sum\_i D\_i$ is snc, then for $J\subset I$ finite the scheme theoretic intersection $D\_J:=\bigcap\_{j\in J}D\_j$ is a regular scheme each of whose irreducible components has codimension $\sharp(J)$ in $X$. Hence for the situation now, $\mathrm{codim} f(D)=k$ and we can let $f(D)\subset D\_i$ iff $i\leq b$ for some $b\leq k$.

*Second:* Actually the **multiplicity** $\mathrm{mult}\_YD$ of a divisor $D$ along a subvariety $Y\subset X$ can be defined as the coefficient of exceptional divisor in the pullback of $D$ along $\mathrm{Bl}\_Y X\to X$. This definition can deduce from the definition ($\mathrm{coeff}\_{[Y]}s(Y,D)$) in section 4.3 of book [FulIT2nd][^3] (see also section 5.2.B in book [Positivity-I][^4]).
Hence for the situation now, if $\Delta=\sum\_i a\_iD\_i$ such that $\sum\_i D\_i$ is snc, then for some subvariety $Z$ we easy to see that 
\\[\mathrm{mult}\_Z\Delta=\sum\_{Z\subset D\_i}\mathrm{coeff}\_{D\_i}\Delta\\]
and this is the reason of snc divisors! $\blacksquare$

**Corollary 2.35.(3).** As we have \\[a(E,X,\Delta)=a(E,X,\Delta+\varepsilon\Delta')+\varepsilon\mathrm{coeff}\_E f^* \Delta'\\]
and we may need not assume that $\Delta,\Delta'$ have no common irreducible components (I think). $\blacksquare$

**Proposition 2.36.(2)** Finally, we get \\[\mathrm{totaldiscrep}(X,\Delta)=-\max\_i(1-\alpha\_i)\\]
by definition. Hence $1+\mathrm{totaldiscrep}(X,\Delta)=\min\_i(\alpha\_i)$ and well done. $\blacksquare$

**Proposition 2.43.(Important definitions and facts).** Here we need to introduce more things about Weil divisors and we follows [SMMP][^2] and [the stacks project](https://stacks.math.columbia.edu/) and a note [GD][^5].

(I) **Reflexive modules.** Let $X$ be an integral locally Noetherian scheme and $F$ be a coherent $\mathscr{O}\_X$-module. The *reflexive hull* of $F$ defined as $F^{\vee\vee}:=(F^{\vee})^{\vee}$. We called $F$ is **reflexive** if the natural map $j:F\to F^{\vee\vee}$ is an isomorphism (more results about these we refer [St 31.12](https://stacks.math.columbia.edu/tag/0AVT)). We may define $L^{[m]}:=(L^{\otimes m})^{\vee\vee}$. By [Tag 0EBL](https://stacks.math.columbia.edu/tag/0EBL) we find that if $X$ be an integral locally Noetherian normal scheme and $F,G$ are coherent reflexive $\mathscr{O}\_X$-modules. Then $(F^{\vee}\otimes G)^{\vee\vee}\cong\mathscr{H}om(F,G)$ which shows that the rule $(F,G)\mapsto F\hat{\otimes}G:=(F\otimes G)^{\vee\vee}$ defines an abelian group law on the set of isomorphism classes of rank $1$ coherent reflexive $\mathscr{O}\_X$-modules.

(II) **Weil divisors and reflexive modules.** Fixed an integral locally Noetherian normal scheme $X$ and consider the Weil divisor class group $\mathrm{Cl}(X)$ and the group of isomorphism classes of rank $1$ coherent reflexive $\mathscr{O}\_X$-modules $\mathrm{Cl}'(X)$. First we define the map $\mathrm{Cl}(X)\to \mathrm{Cl}'(X)$ as $D\mapsto\mathscr{O}\_X(D)$ as: since $X$ is normal, we can find some open set $U$ such that $U$ is regular and $\mathrm{codim}\_X X\backslash U\geq 2$. Hence $\mathrm{Cl}(X)\cong \mathrm{Cl}(U)$ canonically and induce $\mathscr{O}\_U(D\_U)$. By the uniquely extension of reflexive $\mathscr{O}\_X$-modules [Tag 0EBJ](https://stacks.math.columbia.edu/tag/0EBJ), we get this map! Actually a more natural definition is that for any open $V\subset X$ we define \\[\Gamma(V,\mathscr{O}\_X(D)):=\\{f\in K(X):\mathrm{div}(f)|\_V + D|\_V \geq 0\\}.\\]
Second, by [Tag 0EBM](https://stacks.math.columbia.edu/tag/0EBM), its not hard to show that this map is an isomorphism!

(III) **Global sections.** Fixed an integral locally Noetherian normal scheme $X$ and a Weil divisor $D$ on it. Pick a non-zero $s\in\Gamma(X,\mathscr{O}\_X(D))$. One can trivially construct a effective divisor $(s)\_0=\_{\mathrm{lin}} D$ and by Proposition 3.12 in [GD][^5], we have many results as the non-singular case! $\blacksquare$

**Theorem 2.44.** Since the original paper [Sza95][^6] has expired, we give a new reference about this. We refer book [Fujino17][^7] Proposition 2.3.20. $\blacksquare$

### Section 2.4. The Kodaira Vanishing Theorem
**Definition 2.49.** Now $X\_{m,L}:=\underline{\mathrm{Spec}}\_X\bigoplus\_{i=0}^{m-1}L^{-i}$ with canonical map $p:X\_{m,L}\to X$. Now we will find the kernel of $p^* :\mathrm{Pic}(X)\to\mathrm{Pic}(X\_{m,L})$! Easy to see that $p\_* \mathscr{O}\_{X\_{m,L}}=\bigoplus\_{i=0}^{m-1}L^{-i}$. Let $M\in\ker p^* $, then we get \\[p\_* \mathscr{O}\_{X\_{m,L}}=p\_* p^* M=M\otimes p\_* \mathscr{O}\_{X\_{m,L}}=\bigoplus\_{i=0}^{m-1}M\otimes L^{-i}.\\]
By the *Krull-Schmidt theorem*, the decomposition of a vector bundle in a direct sum of indecomposable ones is unique up to permutation of the summands, so we get $M\cong L^i$ for any $i$. Hence $\ker p^* =\\{L^i\\}\cong\mathbb{Z}/m\mathbb{Z}$. $\blacksquare$

**All of the section 2.4.** I will omit the whole proof of the Kodaira vanishing theorem here (since it is so old I think...). Next time I will read the section in the Fujino's [Fujino17][^7] using the mixed Hodge structure. (ps: now you used the GAGA, why we not using the kahler identity and kill these things?) $\blacksquare$

### Section 2.5. Generalizations of the Kodaira Vanishing Theorem
**Definition 2.59.** Let $X$ be a *normal* projective variety with Cartier divisor $D$ and let $N(D)=\\{m\geq 0:h^0(X,mD)\neq 0\\}$. We may define 
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
$$\kappa(X,D):=\left\{
\begin{align*}
\max_{m\in N(D)}\dim\phi_{|mD|}(X),&N(L)\neq\emptyset\\
-\infty,&N(L)=\emptyset
\end{align*}\right.
$$
</p>
</body>
</html>
be the *Iitaka dimension* of $D$. When $X$ is not normal, we may take its normalization $\nu:X'\to X$ and define $\kappa(X,D):=\kappa(X',\nu^* D)$.

So we can let $D$ is big if $\kappa(X,D)=\dim X$ which is equivalent to the definition here (see Lemma 2.2.3 in [Positivity-I][^4]). (Of course we can define the Iitaka dimension using $\mathrm{trdeg}\_{\mathbb{C}}(R(X,D))-1$ where $R(X,D):=\bigoplus\_{m\geq 0}H^0(X,mD)$.) We also define the *volume* of the big divisor $D$ to be \\[\mathrm{vol}(X,D):=\limsup\_{m\to +\infty}\frac{h^0(X,mD)}{m^{\dim X}/(\dim X)!}\\]
and by [Positivity-I][^4] we get $\mathrm{vol}(X,D)=\lim\limits\_{m\to +\infty}\frac{h^0(X,mD)}{m^{\dim X}/(\dim X)!}$ (for the case not big, it is not known that if this limit exists). $\blacksquare$

**Theorem 2.64.** For the final step, we have showed that $H^i(X,L\otimes f\_* \omega\_Y)=0$ for $i>0$. We may ask in this situation if we have $f\_* \omega\_Y=\omega\_X$? Actually we have more general results (taken from Lemma 3.3.2 in [Fujino17][^7]):

*Lemma.* Let $X$ be a smooth variety and let $D$ be an $\mathbb{Q}$-divisor on $X$ such that $\mathrm{supp}(\\{D\\})$ is a snc divisor. If $Y$ be a log resolution of pair $(X,\\{D\\})$, then we have \\[f\_* \mathscr{O}\_Y(K\_Y+\lceil f^* D \rceil)\cong \mathscr{O}\_X(K\_X+\lceil D \rceil).\\]

*Sketch of the proof.* Let $\Delta:=\lceil D \rceil-\lfloor D \rfloor$, then $\Delta$ is reduced snc divisor. Hence we get
\\[K\_Y+f^{-1}\_* \Delta+f^* \lfloor D \rfloor=f^* (K\_X+\lceil D \rceil)+\sum\_{E\_i:f-\mathrm{exceptional}}a(E\_i,X,\Delta)E\_i.\\]
We can easily check that \\[\mathrm{mult}\_{E\_i}(\lceil f^* D \rceil-(f^{-1}\_* \Delta+f^* \lfloor D \rfloor))\geq 1\\]
for any $f$-exceptional with $a(E\_i,X,\Delta)=-1$. Hence we have \\[K\_Y+\lceil f^* D \rceil=f^* (K\_X+\lceil D \rceil)+F\\]
for some effective $f$-exceptional Cartier divisor $F$ on $Y$. Hence well done. $\blacksquare$

There is a generalization (known as Kawamata–Viehweg vanishing theorem) of this theorem, we refer section 3.2 in [Fujino17][^7]. $\blacksquare$


[^1]: [Har77] Robin Hartshorne. Algebraic geometry, volume 52. Springer Science & Business Media, 1977.

[^2]: [SMMP] Singularities of the Minimal Model Program. Janos Kollar. Cambridge. 2013.

[^3]: [FulIT2nd] William Fulton. Intersection Theory, 2nd. Springer New York, NY. 1998. 

[^4]: [Positivity-I] R. Lazarsfeld. Positivity in AG I. Springer. 2000.

[^5]: [GD] KARL SCHWEDE. [GeneralizedDivisors](https://www.math.utah.edu/~schwede/Notes/GeneralizedDivisors.pdf).

[^6]: [Sza95] Endre SzabÃ. Divisorial log terminal singularities. J. Math. Sci. Univ. Tokyo. Vol. 1 (1995), No. 3,631-639.

[^7]: [Fujino17] Osamu Fujino. Foundations of the Minimal Model Program. World Scientific. 2017.

[^8]: [Convex97] Ralph Tyrell Rockafellar. Convex Analysis. Princeton University Press. 1997.
