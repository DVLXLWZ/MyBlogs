---
layout: post
title: Some Gaps and Examples in Intersection Theory by Fulton III
date: 2023-01-19
last_modified_at: 2023-02-26
tags: [Algebraic Geometry]
toc:  true
math: true
excerpt_separator: <!--more-->
---
This is one of a series of blogs aiming to complete some details of the examples in this book (*Intersection Theory, 2nd edition* by William Fulton[^1]) and give some comments. This blog we consider chapter 10 to chapter 13.

<!--more-->

> Previously on these:
>
> [Some Gaps and Examples in Intersection Theory by Fulton I](https://dvlxlwz.github.io/MyBlogs/2022/12/12/Some-Gaps-and-Examples-in-Intersection-Theory-by-Fulton-I/);
> 
> [Some Gaps and Examples in Intersection Theory by Fulton II](https://dvlxlwz.github.io/MyBlogs/2022/12/12/Some-Gaps-and-Examples-in-Intersection-Theory-by-Fulton-II/).

## Chapter 10. Families of Algebraic Cycles
### Section 10.1. Families of Cycles Classes
**Example 10.1.6(a).** We called $T$ be a *unirational* variety if there exists a dominant rational map $\mathbb{P}^n\_k\dashrightarrow T$. Easy to see that $T$ is unirational iff there is a dominant generically finite morphism $X\to T$, where $X$ is rational iff there is a finite extension of $K(T)$ which is a
purely transcendental field extension of $k$, the base field.

Now we get a dominant rational map $f:\mathbb{P}^n\dashrightarrow T$. Pick $X\to \mathbb{P}^n$ be a birational projective map (taking the Zariski closure of $\Gamma\_f$, which is actually a blowing map as in Harshorne II.7) such that extend $f$ as a projective surjective map $X\to T$. Hence if we can show that the blowing up $X\to\mathbb{P}^n$ has the chains of rational curves connecting any two points, then so as mapping to $T$! Hence now checking affine locally, we reduce the problem to the case in the text!

Finally we give another beautiful proof of this case (due to Sándor Kovács ([mathoverflow/q/115759](https://mathoverflow.net/q/115759))): Assume that $\pi(t)=0\in \mathbb{A}^m$. Then the point $t\in E$ corresponds to a normal direction of $Z$ at $0$. Let $L\subset \mathbb{A}^m$ be a line pointing in that direction and let $\widetilde{L}=\pi^{-1}\_* L\subset T$ be the strict transform of $L$ on $T$. Observe that by choice $L\not\subset Z$ and hence $\widetilde{L}\not\subset E$. Also note that $\pi\|\_{\widetilde{L}}: \widetilde{L}\to L$ is the blow up of $L$ along $L\cap Z$, and hence it is an isomorphism. Therefore there exists a morphism $h: \mathbb{A}^1\to\widetilde{L} \subset T$ with $h(0)=t$ but $h(\mathbb{A}^1)=\widetilde{L}$ not contained in $E$. $\blacksquare$

### Section 10.3. Algebraic Equivalence
**Example 10.3.2.** Here we prove the last claim in the proof (maybe hint) following the D. Mumford's *Abelian Varieties* Page 53:

*Lemma.* Let $X$ by any variety and $x,y\in X$, then there is an irreducible curve $C$ on $X$ containing $x$ and $y$.

*Proof.* We assume that $\dim X> 1$. By the lemma of Chow, we may assume $X$ projective. By induction of dimension, it is sufficient to find a subvariety $Y$ of codimension $1$ in $X$ containing $x,y$.

Now blowing up $x,y$ we get a birational morphism $f:X':=\mathrm{Bl}\_{x,y}X\to X$ and $X'$ is projective with $\dim f^{-1}(x)>1$ and $\dim f^{-1}(y)>1$. Let $X'\subset\mathbb{P}^N$ and there is a hyperplane $H\subset\mathbb{P}^N$ such that $H\cap X'=Y'$ is irreducible by some kind of Bertini's irreducibility theorem (see [Tag 0G4C](https://stacks.math.columbia.edu/tag/0G4C)), and $H\cap f^{-1}(x)\neq\emptyset$ and $H\cap f^{-1}(y)\neq\emptyset$ since the reason of dimension. After taking $Y:=f(Y')$ and well done! $\blacksquare$

*Remark.* (i) As the base field is algebraically closed, the product of curves is a variety;

(ii) For more results of Bertini type, we refer [Tag 0FD4](https://stacks.math.columbia.edu/tag/0FD4) and [Arxiv 1912.09076](https://arxiv.org/pdf/1912.09076.pdf). $\blacksquare$

### Section 10.4. An Enumerative Problem
**Step 1.** I think $\zeta:=p^* c\_1(\mathscr{O}\_{\mathbb{P}^2}^{\vee}(1))$ should be $c\_1(\mathscr{O}\_E(1))$ where $p:P(E)=I\to\mathbb{P}^2$! $\blacksquare$

## Chapter 11. Dynamic Intersections
### Section 11.2. Infinitesimal Intersection Classes
**Begining of this section.** Now $\Lambda=N\_0 T$ and seem as a fiber of $\Lambda\_X=N\_X\mathscr{X}$. Now $\Lambda\_X$ and $i^* N\_Y(Y\times T)$ are all trivial line bundle over $X$, hence $N\_X(Y\times T)\cong N\_XY\oplus i^* N\_Y(Y\times T)\cong N\_XY\oplus \Lambda\_X$.

Now the inclusion $(\varrho,id):\Lambda\_X\to N\_XY\oplus\Lambda\_X$ as the composition:
\\[\Lambda\_X\to N\_X(Y\times T)=N\_XY\oplus i^* N\_Y(Y\times T)\cong N\_XY\oplus \Lambda\_X\\]
where the first equality be the canonical decomposition of elements in $\Lambda\_X$ and the second isomorphism is mapping the part in the trivial bundle to the $\Lambda\_X$ making $\Lambda\_X\to\Lambda\_X$ is $id$! Hence $\varrho(\frac{\partial}{\partial t})$ is the first part! See the diagram as an example:

![placeholder](/MyBlogs/my_pics/2023-01-19-1.png){: .align-center}

See also **Example 11.3.1** as a nice example. $\blacksquare$

### Section 11.3. Limits and Distinguished Varieties
**Example 11.3.2.** (Original paper: [Excess intersection of divisors](http://www.numdam.org/item/CM_1981__43_3_281_0.pdf)) Actually we get exact sequence of Artinians
\\[0\to\mathscr{O}/(a\_1,a\_2)\to\mathscr{O}/(a\_1g\_2-a\_2g\_1,fa\_1,fa\_2)\to\mathscr{O}/(f,a\_1g\_2-a\_2g\_1)\to0.\\]
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
&\mathrm{length}_{\mathscr{O}}(\mathscr{O}/(a_1g_2-a_2g_1,fa_1,fa_2))\\
&=\mathrm{length}_{\mathscr{O}}(\mathscr{O}/(a_1,a_2))+\mathrm{length}_{\mathscr{O}}(\mathscr{O}/(f,a_1g_2-a_2g_1)).
\end{align*}
</p>
</body>
</html>
By **Proposition 7.1** and the assumption of without common factors, we get the result. $\blacksquare$

**Example 11.3.1-11.3.3.** Actually Example 11.3.1-11.3.2 explain the Segre's formula $(* )$ for the construction of $H\_1\cdot H\_2$ by
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
\begin{equation}
\require{AMScd}
\begin{CD}
H_1\cap H_2 @> >> \mathbb{P}^2\\
@VVV @VV V\\
H_1\times H_2 @> >> \mathbb{P}^2\times\mathbb{P}^2
\end{CD}
\end{equation}
</p>
</body>
</html>
+ For Example 11.4.3. (a) and (b) show that Severi’s claim is not true, so the contributions of distinguished varieties may not be described as the *minimum* over all deforma-tions of hypersurfaces.
+ For Example 11.4.3. (d)-(e) show that the different constructions of $H\_1\cdot H\_2$ may have different distinguished varieties and different contributions. $\blacksquare$

### Section 11.4. Moving Lemmas
**Example 11.4.1.** For details, we refer [Tag 0B0D](https://stacks.math.columbia.edu/tag/0B0D) instead of the original paper by Robert since the proofs in stacks project are more clear. $\blacksquare$

**Example 11.4.2.** For the proof of this fact, we need to read the paper [Hoyt71][^2]. But I haven't this paper for now (for [Hoyt71Paper](https://informaticsjournals.com/index.php/jims/article/view/16721), we need to pay it)...

**Example 11.4.7.** After reading chapter 19 (about cycle maps) I will finish this example.

**Example 11.4.8.(b).** Need to add.

**Example 11.4.9.** For the proof of this fact, we need to read the part of the book [Samuel55][^3]. But it is a French book and I even cannot download it!

## Chapter 12. Positivity
### Section 12.1 Positive Vector Bundles
**At the begining.** The definition of *ample* here is strange as if a scheme $X$ admit an ample line bundle $L$, then $X$ is hence proper over $k$. Hence a quasi-affine scheme $X$ with an ample line bundle will implies $\dim X=0$. $\blacksquare$

**For the ampleness of vertor bundles.** This definition created by R. Hartshorne. These basic properties can be seen in the original paper [AmpleHar66][^4] or the book [LarII][^5]. $\blacksquare$

**Theorem 12.1.** (b) They claim that $P(L\oplus 1)\backslash s\_E(X)\cong L^{\vee}$.

They claim that $L^{\vee}$ pullback to $L^{\vee}$ is trivial.

**Example 12.1.4.** What the hell was the last two statements? First one we need to show that if $E$ is ample, then $ms\_E^* [V]\in \mathrm{CH}^+\_{k-r} (X)$ for some $m>0$, how can we use the proof of Theorem 12.1.(b)? Second they do not know if this is true for (d), but there are no condition about *generated by its sections*!!! **I think there must be some mistake here!**

**Example 12.1.5.** If $E$ is $n$-ample and generated by its sections with subvariety $V\subset E$ such that $\dim V\geq \mathrm{rank} E+n$, then they claim that $s\_E^* [V]\in\mathrm{CH}^+\_* (X)$. Following the proof of the Theorem 12.1.(c), the only modification is the last step (we use $\dim V\geq \mathrm{rank} E+n$ here). By the original paper of $n$-ampleness [Sommese78][^6] Proposition (1.7.3), we get that if there is a finite map $f:Z\to X$ of a proper variety $Z$ and $f^* E$ has a trivial quotient bundle, then $\dim Z < n$! Now as $\dim V\geq \mathrm{rank} E+n$, we get $s\_E^* V\in \mathrm{CH}\_k (X)$ where $k\geq n$. Hence $\dim X\geq n$ and this is impossible! (Note: why Fulton do not just let $\dim X\geq n$?)

For the final statement, if the first statement in the final paragraph in Example 12.1.4 is correct, then $E$ is $n$-ample and we can argue as Example 12.1.4. But why Fulton do not just assume that $E$ is $n$-ample???

These two examples are so **weird**, we need to think these more some day!

**Example 12.1.8.** How can we use $0\notin\mathrm{CH}\_{n-p}^+ (X)$? We need to think more...

**Example 12.1.9.** Why $f(Z)\subset\mathbb{A}^1$ is finite? Here $V$ need not be proper and if $V\subset s\_E(X)$ (if $\dim X >\dim V$), then $f(Z)\subset\mathbb{A}^1$ cannot be a finite set. We need to think more...

**Example 12.1.10.** I think the only condition we used in the proof of Theorem 12.1.(c) is the final step! So we just need to let $E$ generically ample, that is, $\mathrm{Damp}(E)\neq X$, then $s\_E^* [C]\in \mathrm{CH}\_* ^+ (X)$ here! Of course the condition $\mathrm{Supp}(C)$ not contained in $\mathrm{Damp}(E)$ can implies this condition, but I don't know what's the meaning of this. Even the final sentence of the second paragraph tell us that Schur polynomials in Chern classes of generically ample vector bundles are positive since by Example 12.1.7.(b) we get $\Delta\_{\lambda}(E)\cap [X]=s\_H^* [\Omega]\in\mathrm{CH}\_* ^+ (X)$ where $H$ have the same positivity with $E$. $\blacksquare$

### Section 12.2. Positive Intersections
**Example 12.2.1.** (a). For the Grassmannian, we refer Example 12.2.2. For flag varieties, we refer [AP83][^7] Corollary 2.2.

(b). The exact sequence $0\to\mathscr{O}\_X\to E\to T\_X\to0$ can be seen as follows
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
\xymatrix {
 &0\ar[d]&0\ar[d]& & \\
 &O_X\ar[d]&O_X\ar[d]& & \\
0\ar[r]&E\ar[r]\ar[d]&O_X(1)^{\oplus(n+2)}\ar[dr]\ar[d]& & \\
0\ar[r]&T_X\ar[r]\ar[d]&T_{\mathbb{P}^n}\ar[r]\ar[d]&O_X(d)\ar[r]& 0\\
 &0&0& & 
}
\end{xy}
$$
</p>
</body>
</html>
by some easy diagram chase. $\blacksquare$

**Example 12.2.2.**

**Example 12.2.3.**

**Example 12.2.8.** Why we can get $\deg\_L(V\_1\cdots V\_r)=\prod\_{j=1}^r\deg\_L(V\_j)$? I think this is not correct if $X$ is not $\mathbb{P}^n$.

**Example 12.2.9.** We need to show that the Chern classes $c\_i(E)\cap [X]$ represented by non-negative cycles if bundle $E$ is generated by global sections.

**Example 12.2.11.** For some details, we refer section 2 in [FulLar83][^8]. $\blacksquare$

### Section 12.3. Refined Bézout Theorem
**Example 12.3.5.** We need to add the reference of this Lazarsfeld's inequality!

## Chapter 13. Rationality
I will omit this section since this is far from the aspect of geometry!!!


[^1]: [FulIT2nd] William Fulton. Intersection Theory, 2nd. Springer New York, NY. 1998.

[^2]: [Hoyt71] W. L. Hoyt. On the Moving Lemma for Rational Equivalence. The Journal of the Indian Mathematical Society, 35(1-4), 47–66. 1971.

[^3]: [Samuel55] P. Samuel. Méthodes d'algèbre abstraite en géométrie algébrique. Ergebnisse der Mathematik, neue Folge, 4, 5. (Springer, Berlin). 1955.

[^4]: [AmpleHar66] Robin Hartshorne. Ample vector bundles. Pub. Mathématiques de lHES, 29, 64–94. 1966.

[^5]: [LarII] R. Lazarsfeld. Positivity in Algebraic Geometry II. Springer. 2004.

[^6]: [Sommese78] Andrew John Sommese. Submanifolds of Abelian varieties to Rebecca, 233, 229–256. 1978.

[^7]: [AP83] Aigli Papantonopoulou. On the tangent bundle of a flag variety. Annali dell’Università di Ferrara, 29, 1–7. 1983.

[^8]: [FulLar83] William Fulton, Robert Lazarsfeld. Positive Polynomials for Ample Vector Bundles. Ann. of Math (2), Vol. 118, No. 1, pp. 35-60. 1983.
