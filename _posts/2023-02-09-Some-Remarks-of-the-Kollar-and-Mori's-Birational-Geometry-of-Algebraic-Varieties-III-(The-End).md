---
layout: post
title: Some Remarks of the Kollar and Mori's Birational Geometry of Algebraic Varieties III (The End)
date: 2023-02-09
last_modified_at: 2023-02-28
tags: [Algebraic Geometry]
toc:  true
math: true
excerpt_separator: <!--more-->
---
This blog aim to give some remarks and complete some details in this book (Kollar and Mori's Birational Geometry of Algebraic Varieties). I will read first five chapters of this book. This is the third blog which about chapter 4 and chapter 5.
<!--more-->

> Previously on these:
>
> [Some Remarks of the Kollar and Mori's Birational Geometry of Algebraic Varieties I](https://dvlxlwz.github.io/MyBlogs/2023/01/10/Some-Remarks-of-the-Kollar-and-Mori's-Birational-Geometry-of-Algebraic-Varieties-I/);
> 
> [Some Remarks of the Kollar and Mori's Birational Geometry of Algebraic Varieties II](https://dvlxlwz.github.io/MyBlogs/2023/01/18/Some-Remarks-of-the-Kollar-and-Mori's-Birational-Geometry-of-Algebraic-Varieties-II/).

## Chapter 4. Surface Singularities of the Minimal Model Program
### Section 4.1. Log Canonical Surface Singulariries
**Theorem 4.5.** Here I need to point out that when the case $(X,\Delta)$ canonical and not smooth, then $E\neq\emptyset$ and $E=\bigcup\_i E\_i$ with negative definite $(E\_i\cdot E\_j)$. Then by proof of the minimal model of surface **Theorem 1.28** (kill the $(-1)$-curves), we find that $K\_Y$ is nef! $\blacksquare$

### Section 4.2/4.3. Du Val Singularities and Its Simultaneous Resolutions
**Theorem 4.20.** What is a surface double point? I will omit this. Second, in the proof of Du Val singularity implies canonical, we use a fact taken from [Tag 0AV9](https://stacks.math.columbia.edu/tag/0AV9):

*Lemma.* Let $R$ be a Noetherian domain. Let $f:M\to N$ be a map of $R$-modules. Assume $M$ is finite, $N$ is torsion free, and that for every prime $\mathfrak{p}$ of $R$ one of the following happens:

(I) $M\_{\mathfrak{p}}\to N\_{\mathfrak{p}}$ is an isomorphism, or

(II) $\mathrm{depth}(M\_{\mathfrak{p}})\geq 2$.

Then $f$ is an isomorphism.

Now we get map $f\_* \mathscr{O}\_Y(K\_Y)\to \mathscr{O}\_X(K\_X)$ which is isomorphism outside $0$ and $\mathscr{O}\_X(K\_X)$ is torsion free since it is reflexive. Over $0:=\mathfrak{p}\_0$ we have $\mathrm{depth}(M\_{\mathfrak{p}\_0})=\mathrm{depth}(R\_{\mathfrak{p}\_0})\geq 2$ by normality ($S\_2$). Hence $K\_X$ is Cartier and hence by the same reason, we get $f^* \mathscr{O}\_X(K\_X)\cong \mathscr{O}\_Y(K\_Y)$. $\blacksquare$

**I will omit the whole proofs in  section 4.2 and 4.3 for now and I will read it when I need or want to read it...**

### Section 4.4. Elliptic Surface Singularities
**Proposition 4.45.** For the proof of (3), we find a section of $L$ generates $L$ near $E$ and $L\equiv\_f0$, then why $L\cong\mathscr{O}\_Y$?
  
**Proposition 4.47.** For the final step of the first paragraph, why $\omega\_Y(Z)\cong\mathscr{O}\_Y$? For the first sentence of the second paragraph, why $f^* \mathscr{O}\_X(K\_X)\cong\mathscr{O}\_Y$ when $K\_X$ Cartier?

**Theorem 4.57.** In step 4, why $K\_{B^* X}=p\_* K\_Y$ and $K\_{Y}=p^* K\_{B^* X}$? In step 5, why when $k=2$ the $B^* X$ is the normalization of blowing up?

## Chapter 5. Singularities of the Minimal Model Program
**Geography of singularities:** The geography of singularity types with implications looks like this:

![](/my_pics/2023-02-09-1.png)

### Section 5.1. Rational Singularities
**Definition 5.2.** For the fact that over normal scheme a torsion free sheaf $F$ is $S\_2$ iff it is reflexive, we refer the proof in [Tag 0AVB](https://stacks.math.columbia.edu/tag/0AVB). $\blacksquare$

**Lemma 5.12.** We may let $Y$ is a **normal** variety in this proof. Moreover, we can give a simply proof of (2) implies (1) as follows (taken from [RatKovacs00][^1] Lemma 1, seems without using the **normality**):

*Proof.* GR vanishing Theorem told us that $\omega\_Y\simeq Rf\_* \omega\_X$, hence by Grothendieck duality we get
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
\mathscr{O}_Y&\simeq R\mathscr{H}om_Y(\omega_Y,\omega_Y)\simeq R\mathscr{H}om_Y(Rf_* \omega_X,\omega_Y)\\
  &\simeq Rf_*R\mathscr{H}om_X(\omega_X,\omega_X)\simeq Rf_*\mathscr{O}_X
\end{align*}
</p>
</body>
</html>
well done. $\blacksquare$

For more things, a more advanced results about rational singularities we refer [RatKovacs17][^2], and papers [RatKovacs00][^1], [Dais02][^3] (Theorem 1.4) and [Kol96][^4] (section 11) are also introduced some results about rational singularities. $\blacksquare$

**Proposition 5.13.** For the final step, we need to use the following result: if $f:Y\to X$ be a resolution of singularities ($X$ normal) with $E=f^{-1}(\mathrm{Sing}(X))$ and natural inclusions $\iota: \mathrm{Reg}(X)\to X$, $j:Y\backslash E\to Y$. Consider the diagram:
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
Y\backslash E \ar[d]^{\cong} \ar[r]^j & Y\ar[d]_f \\
\mathrm{Reg}(X) \ar[r]^{\iota} & X
}
\end{xy}
$$
</p>
</body>
</html>
Hence we have 

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
f_*\omega_Y&\hookrightarrow f_*j_*j^*\omega_Y=\iota_*\omega_{\mathrm{Reg}(X)}=\omega_{X}
\end{align*}
</p>
</body>
</html>
which is an injection, well done. $\blacksquare$

### Section 5.2. Log Terminal Singularities
**Lemma 5.17.** How to use (2.32) to deduce (2)?

**Proposition 5.20.(1)(2)(3)/Corollary 5.21.** For the some details in the proofs of these, we refer the whole section 2.3 in [Kol13][^5]! For example, 2.40 for (1) and 2.41-2.42 for (2)(3) and 2.49-2.51 for Corollary 5.21. $\blacksquare$

**Corollary 5.24.** Here is the kind of converse of comments of Corollary 3.53 in [KMII](https://dvlxlwz.github.io/2023/01/18/Some-Remarks-of-the-Kollar-and-Mori's-Birational-Geometry-of-Algebraic-Varieties-II/), taken from 7.12 in the book [HDAG01][^6]:

*Lemma.* If $f:Y\to X$ is proper birational where $X$ is normal and $Y$ is normal which satisfied that any Cartier divisor can be the difference of two effective Cartier divisors with no common component. Then for any exceptional Cartier $F$ in $Y$, we have $f\_* \mathscr{O}\_Y(F)\cong\mathscr{O}\_X$ if and only if $F$ effective.

*Proof.* Let $F=F\_1-F\_2$ be the difference of two effective Cartier divisors with no common component. Hence $f\_* \mathscr{O}\_Y(F)\subset f\_* \mathscr{O}\_Y(F\_1)\cong\mathscr{O}\_X$. It is therefore a sheaf of ideals that defines a subscheme of $X$ supported on $f(F\_2)$. Well done. $\blacksquare$

For the condition of $Y$ in *Lemma*, we can not always have, but if $Y$ admits an ample line bundle or using the Fulton's trick (after some blowing up of ideal of denominators, in the proof in Section 2.4 of his famous book), we can get it. $\blacksquare$

### Section 5.4. Inversion of Adjunction
**Proposition 5.46/Remark 5.47.** Not that the condition that $S$ is Cartier in codimension $2$ aiming to use the adjunction formula (see Remark 5.47). For some more general case this needs some correction terms. Here we refer [JK92][^7] section 16 (and section 17 is the conclusions of inversion of adjunction) and more advanced [Kol13][^5] chapter 4 (or more precisely, section 4.1). $\blacksquare$

**Corollary 5.52.** We may let $X$ quasi-projective in order to use the Proposition 2.43. $\blacksquare$

[^1]: [RatKovacs00] Sándor J. Kovács. A characterization of rational singularities. Duke Math. J. 102(2): 187-191 (1 April 2000).

[^2]: [RatKovacs17] Sándor J. Kovács. Rational singularities. [Arxiv,1703.02269](https://arxiv.org/pdf/1703.02269.pdf) (7 March 2017).

[^3]: [Dais02] Dimitrios I. Dais. RESOLVING 3-DIMENSIONAL TORIC SINGULARITIES. Séminaires & Congrès, 6, 2002, p. 155–186.

[^4]: [Kol96] János Kollár. Singularities of Pairs. [Arxiv,1703.02269](https://arxiv.org/pdf/alg-geom/9601026.pdf), 1996.

[^5]: [Kol13] János Kollár. Singularities of the Minimal Model Program, 2013.

[^6]: [HDAG01] Olivier Debarre. Higher-Dimensional Algebraic Geometry, Springer. 2001.

[^7]: [JK92] JÁNOS KOLLÁR (éd.). Flips and abundance for algebraic threefolds - A summer seminar at the University of Utah (Salt Lake City, 1991). Astérisque, tome 211 (1992).
