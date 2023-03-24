---
layout: post
title: Reading program on moduli space of curves
date: 2022-11-15
last_modified_at: 2023-03-25
tags: [Math Programs]
toc:  true
math: true
excerpt_separator: <!--more-->
---
This is my plan of the reading program of the moduli space of curves, aiming to discover the geometrical properties of stacks $\mathscr{M}\_{g,n}$ and $\overline{\mathscr{M}}\_{g,n}$ and their coarse moduli spaces.

<!--more-->

Here is our notes: [Notes on moduli space of curves](https://dvlxlwz.github.io/MyBlogs/my_notes/ModuliSpaceCurvesReadingNotes.pdf).
This is another teaching plan: [Algebraic Curves and Surfaces I: Moduli of Curves](https://deopurkar.github.io/teaching/moduli/curvescourse.pdf).

## 1. The timeline

Maybe **9/20/2022 -- 4/20/2023**.

## 2. Preliminaries we need

Including the basic theory of schemes and cohomology of coherent sheaves (such as R. Hartshorne's book[^3] chapter 2,3), the basic theory of curves and a little bit surface theory (such as R. Hartshorne's book[^3] chapter 4,5.1 and something in [ACGH85][^2]) and the basic theory of algebraic spaces, algebraic stacks including the Keel-Mori theorem (such as chapter 2,3,4 in Jarod Alper's notes[^4] or Martin Olsson's book[^5]).

## 3. The basic results
The main reference are the chapter 5 in Jarod Alper's notes[^4] and the book [ACG11][^1].
### 3.1. The basic facts of curves

Basic but important properties of single and families of curves; the varieties associated to curves, such as Jacobian, Picard and etc.

### 3.2. The moduli stack of smooth curves

We will show the moduli stack of smooth curves $\mathscr{M}\_g$ is a smooth locally of finite type Deligne-Mumford stack when $g\geq 2$. Actually when $g=1$, $\mathscr{M}\_1$ is not a stack! When $g=0$ and we consider the stack over $(Sch/k)$ where $k$ is algebraically closed, then $\mathscr{M}_0\cong BPGL_2$.

### 3.3. The nodal curves and stable curves

We will consider the detailed properties of the nodal curves and stable curves using some nice tools (such as $\delta$-invariant) and detailed deformation theory of them, including Kuranishi family. This is the fundamental of the moduli space of curves since the Kuranishi family gives us the "local charts" (étale locally, of course) of $\overline{\mathscr{M}}\_{g,n}$ and $\overline{M}\_{g,n}$ over $\mathbb{C}$.

### 3.4. The several stacks

We will consider

\\[\mathscr{M}\_{g,n}\subset\overline{\mathscr{M}}\_{g,n}\subset\mathscr{M}^{ss}\_{g,n}\subset\mathscr{M}^{pre}\_{g,n}\subset\mathscr{M}^{\leq nodal}\_{g,n}\subset\mathscr{M}^{all}\_{g,n}\\]

are all algebraic stacks locally of finite type over Z. Then the moduli stack of n-pointed stable curves $\overline{\mathscr{M}}\_{g,n}$ is a quasi-compact smooth Deligne-Mumford stack of dimension $3g−3+n$.

### 3.5. The stable reduction

The stable reduction in $\mathrm{char}(k)=0$ by using some birational geometry of surfaces. This shows that the moduli stack of $n$-pointed stable curves $\overline{\mathscr{M}}\_{g,n}$ is also a proper Deligne-Mumford stack (then by Keel-Mori theorem, we get it has a coarse moduli space).

### 3.6. Irreducibility and projectivity

The irreducibility of the moduli stack of stable curves $\overline{\mathscr{M}}\_{g,n}$ and projectivity of that coarse moduli space $\overline{M}\_{g,n}$ (Janos Kollar’s method). Hence when we consider the stack over $Sch/k$, then the coarse moduli space $\overline{M}\_{g,n}$ is a projective variety over $k$!

## 4. Some geometry properties of the moduli space of curves

### 4.1. Basic theory of boundary geometry

We will consider the graphs and dual graphs of nodal and stable curves. Using these we will construct more general gluing maps which is very important.

### 4.2. Line bundles and Picard groups of the moduli stack of stable curves

We will first consider some special line bundles on the moduli stack of stable curves $\overline{\mathscr{M}}\_{g,n}$, including Hodge bundle, point bundles and boundary divisors, tangent bundle, cotangent bundle and normal bundle. Then we will introduce some tools, called determinant $d\_{\pi}$ and Deligne pairing. Next we will show that 

\\[\mathrm{Pic}(\overline{\mathscr{M}}\_{g,n})\otimes\mathbb{Q}\cong\mathrm{Pic}(\overline{M}\_{g,n})\otimes\mathbb{Q}\\]

and more properties. These things we follows [ACG11][^1]. Finally we may discuss more special topics:

(1) State some J. Harer's results[^8][^9] (using the Teichmüller space constructed as in John H. Hubbard and Sarah Koch’s paper[^6]) about the groups $\mathrm{Pic}(M\_{g,n})\otimes\mathbb{Q}$ and $\mathrm{Pic}(\overline{M}\_{g,n})\otimes\mathbb{Q}$. These are summarized in Irene Schwarz's paper[^7]. These will be used at below.

(2) For Enrico Arbarello and Maurizio Cornalba’s paper [The Picard groups of the moduli spaces of curves](https://www.sciencedirect.com/science/article/pii/0040938387900565) we will find the explicit generators of moduli stack of stable curves/smooth curves. Actually we may show that for $g\geq3$, the group $\mathrm{Pic}(\overline{\mathscr{M}}\_{g})$ is freely generated by $\lambda,\delta\_{irr},\delta\_{1},...,\delta\_{\left\lfloor g/2\right\rfloor}$ and $\mathrm{Pic}(\mathscr{M}\_{g})$ is freely generated by $\lambda$. When $g\geq3$, the group $\mathrm{Pic}(\overline{\mathscr{M}}\_{g,n})$ is freely generated by $\lambda,\delta\_{irr},\delta\_{i},\psi_i$ and $\mathrm{Pic}(\mathscr{M}\_{g,n})$ is freely generated by $\lambda,\psi_i$.

(3) Use the Gorthendieck-Riemann-Roch to compute some fundamental relations, such as $K\_{\overline{\scr{M}}\_{g,n}}=13\lambda+\psi-2\delta$. Here we refer [ACG11][^1] Section XIII.7. This due to D. Mumford.

(4) For Enrico Arbarello and Maurizio Cornalba’s paper [Divisors in the moduli spaces of curves](https://arxiv.org/pdf/0810.5373.pdf) we may learn some relations before and after the gluing map $\xi\_{\Gamma}$ of dual graphs $\Gamma$. Need to add.

(5) We will give a glimpse of ample divisors and $F$-conjecture. We may refer Izzet Coskun's survey [BiMS10][^10] and Angela Gibney, Sean Keel, and Ian Morrison's famous paper [GKM02][^11] as [Towards the ample cone](https://www.ams.org/journals/jams/2002-15-02/S0894-0347-01-00384-8/S0894-0347-01-00384-8.pdf).

### 4.3. The Kodaira dimension of the moduli space of stable curves
First we will state many recent results about this, such that when $g\geq 22$, the space $\overline{M}\_{g}$ is of general type and some results about small genus with makred points. Then we will prove the classical result thatwhen $g\geq 24$, the space $\overline{M}\_{g}$ is of general type (We may will refer David Eisenbud and Joe Harris’s papers: including [Limit linear series: Basic theory](https://link.springer.com/article/10.1007/BF01389094) and [The Kodaira dimension of the moduli space of curves of genus>=23](https://link.springer.com/article/10.1007/BF01388710)).

### 4.4. Hassett-Keel program of the moduli space of stable curves
Actually we now can discover something about canonical model and log canonical model of $\overline{M}\_{g}$ when $g\gg 0$ by famous BCHM.
This is called **Hassett-Keel program**. 
In fact if we let
\\[\overline{M}\_{g}(\alpha)=\mathrm{Proj}\left(\bigoplus\_{n\geq0}
H^0\left(\overline{\scr{M}}\_{g},\left\lfloor n(K\_{\overline{\scr{M}}\_{g}}+\alpha\delta)\right\rfloor\right)\right),\\]
then one can get Hassett-Hyeon theorem (We will focus on the first two results):

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
\overline{M}_{g}(\alpha)\cong\left\{
\begin{align*}
	\overline{M}_{g},&\alpha\in(9/11,1]\\
	\overline{M}_{g}^{ps},&\alpha\in(7/10,9/11]\\
	\overline{M}_{g}^{c},&\alpha=7/10\\
	\overline{M}_{g}^{h},&\alpha\in(2/3-\varepsilon,7/10)
\end{align*}\right.
$$
</p>
</body>
</html>

Moreover, in series of papers (as [Alper17][^13]), Jarod Alper, Maksym Fedorchuk, David Smyth, and Frederick van der Wyck find that if we let
\\[\overline{M}\_{g,n}(\alpha)=\mathrm{Proj}\left(\bigoplus\_{n\geq0}
H^0\left(\overline{\scr{M}}\_{g},\left\lfloor n(K\_{\overline{\scr{M}}\_{g}}+\alpha\delta+(1-\alpha)\psi)\right\rfloor\right)\right)\\]
Actually, as the case of Deligne-Mumford stability, for all $\alpha>2/3+\varepsilon$, where $0<\varepsilon\ll 1$, they go through the following steps by some recent theory of algebraic stacks of Alper's:

(a) Construct an algebraic stack $\overline{\scr{M}}\_{g,n}(\alpha)$ of $\alpha$-stable curves;

(b) Construct a good moduli space $\overline{\scr{M}}\_{g,n}(\alpha)\to\overline{\mathbb{M}}\_{g,n}(\alpha)$;

(c) Show that $K\_{\overline{\scr{M}}\_{g}}+\alpha\delta+(1-\alpha)\psi$ on $\overline{\scr{M}}\_{g,n}(\alpha)$
descends to an ample line bundle on $\overline{\mathbb{M}}\_{g,n}(\alpha)$, and conclude that
$\overline{\mathbb{M}}\_{g,n}(\alpha)\cong\overline{M}\_{g,n}(\alpha)$.

### 4.5. Intersection theory of moduli space of curves

We may refer Letterio Gatto’s book: [Intersection theory on moduli space of curves](https://impa.br/wp-content/uploads/2017/04/Mon_61.pdf) but I may not use it. I use the chapter XVII in [ACG11][^1]. 

(I) First we define Chow rings of moduli stack and coarse moduli space of curves (as $\overline{M}\_{g,n}$ is not smooth), then introduce some basic cycles in it, such as Mumford-Morita-Miller classes and $\lambda$-classes. 

(II) We will give some fundamental relations of classes between forgetful maps and gluing maps (we will omit the proofs of these as they are boring). 

(III) Finally, I will introduce the tautological ring with relative theorems and conjectures. More precesely, I will introduce Witten’s Conjecture and give a sketch of the Kontsevich’s proof; I will introduce Poincaré duality conjecture (Hain-Looijenga) and Faber’s conjecture (with some results about it).

### 4.5. Cohomology of the moduli space of curves

We may also follow Enrico Arbarello and Maurizio Cornalba’s paper: [Calculating cohomology groups of moduli spaces of curves via algebraic geometry](http://www.numdam.org/item/PMIHES_1998__88__97_0.pdf). In this paper they showed that $H^k(\overline{M}\_{g,n},\mathbb{Q})=0$ for $k=1,3,5$ and all $g$ and $n$ such that $2g-2+n>0$, next they showed that for all $g$ and $n$ such that $2g-2+n>0$, the group $H^k(\overline{M}\_{g,n},\mathbb{Q})$ is generated by $\kappa\_1,\psi\_i,\delta\_{irr},\delta\_j$.

## 5. Alterations and the moduli space of curves
### 5.1. Extensions of stable curves - the first results

This is the first and most naive result, that is, generalize the stable reduction over DVR into some general normal integral schemes!

Actually this can be showed by a technical lemma (le lemme de Gabber) easily. Then we will give a canonical construction which play the same role in Gabber's lemma, that is, the $\ell$-level structure of moduli stack $\mathscr{M}\_g$ aming to kill all the non-trivial automorphisms. This forms an algebraic space ${}\_{\ell}\mathscr{M}\_g$ over $\mathrm{Spec}\mathbb{Z}[1/\ell]$. After some normalization we get ${}\_{\ell}\overline{\mathscr{M}}\_g$ over $\overline{\mathscr{M}}\_g$. Deligne shows that ${}\_{\ell}\overline{\mathscr{M}}\_g$ is a proper algebraic space. Hence by Chow's lemma we get the results.

### 5.2. de Jong's Alterations

Here we may refer Brian Conrad’s notes: [Alterations](http://virtualmath1.stanford.edu/~conrad/249BW17Page/index.html) and Dan Abramovich and Frans Oort's paper [Alt98][^12]. The main result due to A. Johan de Jong, a weakened form of Hironaka's resolution of singularities of any characteristic:

**Theorem.(A. Johan de Jong-1996)** Let $X$ be a variety over a field $k$. For $Z\subset X$ be any proper closed subset, there exists
and alteration $f:X'\to X$ and an open immersion $j:X'\hookrightarrow\overline{X}'$ such that 
	
(i) $\overline{X}'$ is regular and projective;
	
(ii) The subscheme 
\\[\left(j(f^{-1}(Z))\cup(\overline{X}'\backslash j(X'))\right)\_{\mathrm{red}}\subset\overline{X}'\\]
is a strict normal crossings divisor.

Actually to prove the de Jong’s main theorem, we need to use the general theory of moduli stack
of curves! There are many useful conclusion at the way proving this theorem and in this section
we will give a sketch of the proof.

## 6. A glimpse of Kontsevich’s moduli space of stable maps

Need to add.

[^1]: [ACG11] Geometry of Algebraic Curves, Volumn II, Enrico Arbarello, Maurizio Cornalba, Phillip A. Griffiths, 2011, Springer. See: [ACG11](https://link.springer.com/book/10.1007/978-3-540-69392-5).

[^2]: [ACGH85] Enrico Arbarello, Maurizio Cornalba, Phillip A. Griffiths, and Joe Harris. Geometry of Algebraic Curves, Volume I, volume 267. Springer, 1985.

[^3]: [Har77] Robin Hartshorne. Algebraic geometry, volume 52. Springer Science & Business Media, 1977.

[^4]: [SM] Jarod Alper. Stacks and Moduli. 2022-10-13. See: [Stacks and Moduli](https://sites.math.washington.edu/~jarod/moduli.pdf).

[^5]: [MO16] Martin Olsson. Algebraic spaces and stacks, volume 62. American Mathematical Soc, 2016.

[^6]: [Teich13] John H. Hubbard and Sarah Koch, An analytic construction of the Deligne-Mumford compactification of the moduli space of curves, [An analytic construction of the Deligne-Mumford compactification of the moduli space of curves](https://arxiv.org/abs/1301.0062).

[^7]: [BiMC21] Irene Schwarz. Birational geometry of moduli spaces of pointed curves, 2021.

[^8]: [Harer83] John Harer. The second homology group of the mapping class group of an orientable surface. Inventiones Mathematicae, 72(2):221–239, 1983.

[^9]: [Harer88] John Harer. The cohomology of the moduli space of curves. In Theory of moduli, pages 138–221. Springer, 1988.

[^10]: [BiMS10] Izzet Coskun. Birational geometry of moduli spaces. [Birational geometry of moduli spaces](http://homepages.math.uic.edu/~coskun/utah-notes.pdf), 2010.

[^11]: [GKM02] Angela Gibney, Sean Keel, and Ian Morrison. Towards the ample cone of $\overline{M}\_{g,n}$. J. Amer. Math. Soc, 15, 2002.

[^12]: [Alt98] Dan Abramovich, Frans Oort. Alterations and resolution of singularities. 1998. [arXiv:math/9806100](https://arxiv.org/abs/math/9806100)

[^13]: [Alper17] Jarod Alper, Maksym Fedorchuk, David Smyth, and Frederick van der Wyck. Second flip in the Hassett-Keel program: a local description. Compositio Mathematica, 153:1547 – 1583, 2017.
