---
layout: post
title: Some of the rules of typing blogs.
date: 2019-11-07
last_modified_at: 2022-12-09
tags: [others]
toc:  true
math: true
excerpt_separator: <!--more-->
---

Some basic rules and codes in this Jekyll and HTML.
<!--more-->

## Inline HTML elements

HTML defines a long list of available inline tags, a complete list of which can be found on the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

- **To bold text**, use `**To bold text**`.
- *To italicize text*, use `*To italicize text*`.
- <mark>To highlight</mark>, use `<mark>To highlight</mark>`.
- Abbreviations, like <abbr title="HyperText Markup Langage">HTML</abbr> should use `<abbr>`, with an optional `title` attribute for the full phrase.
- Citations, like <cite>&mdash; Mark Otto</cite>, should use `<cite>`.
- <del>Deleted</del> text should use `<del>` and <ins>inserted</ins> text should use `<ins>`.
- Superscript <sup>text</sup> uses `<sup>` and subscript <sub>text</sub> uses `<sub>`.

Most of these elements are styled by browsers with few modifications on our part.

## How to use LaTeX here?
### Basic settings

First, we add the following codes in *_includes/head.html*:

```
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
<script type="text/x-mathjax-config">

MathJax.Ajax.config.path["Contrib"] = "//cdn.mathjax.org/mathjax/contrib";

  MathJax.Hub.Config({
    tex2jax: {
      skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
      inlineMath: [              // start/end delimiter pairs for in-line math
      ['$', '$']
    ],
    displayMath: [             // start/end delimiter pairs for display math
      ['$$', '$$'],
      ['\\[', '\\]']
    ],
    processEscapes: true,
    processEnvironments: true,
    },
    
    TeX: { 
    equationNumbers: {autoNumber: "AMS"},
    extensions: ["[Contrib]/xyjax/xypic.js"]
    }
  });
</script>
```

After set *math: true*, we can use the LaTeX codes, such as $\int_{S}\omega\in\{\iint\}$ given by
```markdown
$\int_{S}\omega\in\{\iint\}$
```
and 
\\[
H^i_{DR}(X/S):=H^iR\Gamma(X,\Omega_{X/S}^*)
\\]
given by
```markdown
\\[
H^i_{DR}(X/S):=H^iR\Gamma(X,\Omega_{X/S}^*)
\\]
```
Hence we can write math now! 
> Note that we need to use `\_` instead of `_` and use `\\{…\\}` instead of `\{…\}`.

### Math environments and mutiple lines
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
  When $a \ne 0$, there are two solutions to $ax^2 + bx + c = 0$ and they are
  \begin{align}
  DDD\\
  eee\\
  eee
  \end{align}
and
\begin{align}
&\left\langle L_1,M\right\rangle _{\pi}\otimes\left\langle L_2,M\right\rangle _{\pi}\cong\left\langle L_1\otimes L_2,M\right\rangle _{\pi}\\
&\left\langle L,M_1\right\rangle _{\pi}\otimes\left\langle L,M_2\right\rangle _{\pi}\cong\left\langle L,M_1\otimes M_2\right\rangle _{\pi};
\end{align}
</p>
</body>
</html>

given by

```
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
  When $a \ne 0$, there are two solutions to $ax^2 + bx + c = 0$ and they are
  \begin{align}
  DDD\\
  eee\\
  eee
  \end{align}
and
\begin{align}
&\left\langle L_1,M\right\rangle _{\pi}\otimes\left\langle L_2,M\right\rangle _{\pi}\cong\left\langle L_1\otimes L_2,M\right\rangle _{\pi}\\
&\left\langle L,M_1\right\rangle _{\pi}\otimes\left\langle L,M_2\right\rangle _{\pi}\cong\left\langle L,M_1\otimes M_2\right\rangle _{\pi};
\end{align}
</p>
</body>
</html>
```


### Commutative diagrams I - AMSCD environment (not useful)
As
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
S' @>^{66} >> Y\\
@V^{55}VV @VV V\\
S @> >> X
\end{CD}
\end{equation}
</p>
</body>
</html>

given by
```
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
S' @>^{66} >> Y\\
@V^{55}VV @VV V\\
S @> >> X
\end{CD}
\end{equation}
</p>
</body>
</html>
```

### Commutative diagrams II - XyJax (or XyPic.js) environment (very useful)
As
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
U \ar@/_/[ddr]_y \ar@{.>}[dr]|{\langle x,y \rangle} \ar@/^/[drr]^x \\
 & X \times_Z Y \ar[d]^q \ar[r]_p & X \ar[d]_f \\
 & Y \ar[r]^g & Z
}
\end{xy}
$$
</p>
</body>
</html>

given by
```
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
U \ar@/_/[ddr]_y \ar@{.>}[dr]|{\langle x,y \rangle} \ar@/^/[drr]^x \\
 & X \times_Z Y \ar[d]^q \ar[r]_p & X \ar[d]_f \\
 & Y \ar[r]^g & Z
}
\end{xy}
$$
</p>
</body>
</html>
```

## Others
### Adding tables
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Upvotes</th>
      <th>Downvotes</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td>Totals</td>
      <td>21</td>
      <td>23</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>10</td>
      <td>11</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>4</td>
      <td>3</td>
    </tr>
    <tr>
      <td>Charlie</td>
      <td>7</td>
      <td>9</td>
    </tr>
  </tbody>
</table>

given by

```
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Upvotes</th>
      <th>Downvotes</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td>Totals</td>
      <td>21</td>
      <td>23</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>10</td>
      <td>11</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>4</td>
      <td>3</td>
    </tr>
    <tr>
      <td>Charlie</td>
      <td>7</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
```

### Adding pictures

After upload a picture, we get:

![Text](/my_pics/text1.jpg)

given by `![Text](/my_pics/text1.jpg)`.


### Adding footnotes

I'm happy[^1]!

given by
```markdown
I'm happy[^1]!

[^1]: Well lucky!
```

[^1]: Well lucky!

### Something useful

[Markdown codes](https://copyfuture.com/blogs-details/20201209221922052b2m9f6d5nrhw3wv).

## Excerpt

We need add this at the first place of our blog:
```
---
layout: post
title: Text the excerptions
date: 2022-11-14
last_modified_at: 2022-11-14
tags: [others]
toc:  true
math: true
excerpt_separator: <!--more-->
---
```
Then we need to write
```
<!--more-->
```
to end the excerption.

## Comments
See [A new comments system for my static Jekyll site](https://aristath.github.io/blog/static-site-comments-using-github-issues-api).
