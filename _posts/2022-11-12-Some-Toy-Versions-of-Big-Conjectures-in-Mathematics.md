---
layout: post
title: Some Toy Versions of Big Conjectures in Mathematics
date: 2022-11-12
last_modified_at: 2022-12-24
tags: [Other Math]
toc:  true
math: true
excerpt_separator: <!--more-->
---
Here we use the basic algebraic geometry to prove some toy versions of big conjectures in math, such as Fermat's conjecture for polynomials and $ABC$-conjecture for polynomials.

<!--more-->
## 1. Fermat's conjecture for polynomials
**Theorem 1.1.** Let $f,g,h\in k[x]$ be nonconstant polynomials such that no irreducible divides all of $f,g,h$ where $k$ be an algebraically closed field of characteristic zero. If \\[f^n+g^n=h^n,\\] then $n\leq 2$.

*Proof.* Let $Z:=V\_+(x^n+y^n-z^n)\subset\mathbb{P}^2$. Let $F,G,H\in k[s,t]$ be the homogenized $f,g,h$. Easy to see that the Fermat equation holds at whole $\mathbb{P}^1$, that is, $F^n+G^n=H^n$. Now consider \\[\psi:\mathbb{P}^1\to Z\subset\mathbb{P}^2,[s:t]\mapsto[F(s,t):G(s,t):H(s,t)].\\]
This is nonconstant (since they are relatively prime), by Riemann-Hurwitz theorem we get
\\[0=g(\mathbb{P}^1)\geq g(Z)=\frac{(n-1)(n-2)}{2},\\] hence $n\leq 2$. $\blacksquare$

## 2. $ABC$-conjecture for polynomials
**Lemma 2.1. (Belyi’s theorem, 1979).** Let $X$ be a connected nonsingular curve. Then the following are equivalent:

(i) $X$ defined over $\overline{\mathbb{Q}}$;

(ii) There exists a Belyi map $\phi:X\to\mathbb{P}^1$, that is, the branch Locus of $\phi$ is in the set $\\{0,1,\infty\\}$.

**Theorem 2.2. (Mason-Stothers theorem).** Let $f,g,h\in k[x]$ be nonconstant polynomials such that no irreducible divides all of $f,g,h$ where $k$ be an algebraically closed field of characteristic zero. If \\[f(x)+g(x)=h(x),\\] then 
\\[h:=\max\\{\deg f,\deg g,\deg h\\}\leq \deg\mathrm{rad}(fgh)-1\\]
where $\mathrm{rad}(F)$ means the product of the distinct irreducible factors of $F$.

*Proof.* Let $\phi=\frac{g}{h}$ be a rational function of degree $h$ which induce $\phi:\mathbb{P}^1\to\mathbb{P}^1$.
