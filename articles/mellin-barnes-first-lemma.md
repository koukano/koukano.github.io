---
layout: article
title: "Barnesの第一補題"
seo_title: "Barnesの第一補題とは？Mellin–Barnes積分の基本公式"
description: "Mellin–Barnes積分で現れる4つのガンマ関数の積を評価するBarnesの第一補題を、積分路と極の条件を含めて解説します。"
category: "gamma-function"
category_label: "ガンマ関数"
---

Mellin–Barnes積分で頻繁に現れる4つのガンマ関数の積は、Barnesの第一補題によって閉じた形に評価できる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：Barnesの第一補題</div>

積分路 $L$ を縦の直線にとり、

$$
\Gamma(a+s),\quad \Gamma(b+s)
$$

の極

$$
s=-a-n,\quad -b-n
\qquad(n=0,1,2,\ldots)
$$

が $L$ の左側に、

$$
\Gamma(c-s),\quad \Gamma(d-s)
$$

の極

$$
s=c+n,\quad d+n
$$

が右側に来るとする。

積分が収束する条件のもとで、

$$
\frac{1}{2\pi i}
\int_L
\Gamma(a+s)
\Gamma(b+s)
\Gamma(c-s)
\Gamma(d-s)
\,ds
=
\frac{
\Gamma(a+c)
\Gamma(a+d)
\Gamma(b+c)
\Gamma(b+d)
}{
\Gamma(a+b+c+d)
}
$$

が成り立つ。

</div>

積分路 $L$ は縦線 $\operatorname{Re}s=\sigma$ とし、$\Gamma(a+s),\Gamma(b+s)$ の極を左側、$\Gamma(c-s),\Gamma(d-s)$ の極を右側に分離するように選ぶ。

<figure class="article-figure">
  <img src="/images/figures/mellin-barnes-contour.svg" alt="左側の二つの極列と右側の二つの極列を分離する縦のMellin-Barnes積分路">
  <figcaption>図1：Mellin–Barnes積分路 $L:\operatorname{Re}s=\sigma$。左側に $s=-a-n,-b-n$、右側に $s=c+n,d+n$ の極が来るように $\sigma$ を選ぶ。</figcaption>
</figure>

## 証明

ベータ関数の積分表示

$$
B(u,v)
=
\int_0^\infty
\frac{x^{u-1}}{(1+x)^{u+v}}\,dx
=
\frac{\Gamma(u)\Gamma(v)}
{\Gamma(u+v)}
$$

を用いる。

まず、

$$
f(x)
=
\frac{x^a}{(1+x)^{a+c}}
$$

とおく。そのMellin変換は

$$
\begin{aligned}
F(s)
&=
\int_0^\infty
f(x)x^{s-1}\,dx\\
&=
\int_0^\infty
\frac{x^{a+s-1}}
{(1+x)^{a+c}}
\,dx\\
&=
\frac{
\Gamma(a+s)\Gamma(c-s)
}{
\Gamma(a+c)
}.
\end{aligned}
$$

同様に、

$$
g(x)
=
\frac{x^b}{(1+x)^{b+d}}
$$

とおけば、

$$
G(s)
=
\frac{
\Gamma(b+s)\Gamma(d-s)
}{
\Gamma(b+d)
}.
$$

Mellin変換のParseval型公式

$$
\frac{1}{2\pi i}
\int_L F(s)G(s)\,ds
=
\int_0^\infty
f(x)g(1/x)\frac{dx}{x}
$$

を用いる。

ここで、

$$
\begin{aligned}
g(1/x)
&=
\frac{x^{-b}}
{(1+x^{-1})^{b+d}}\\
&=
\frac{x^d}
{(1+x)^{b+d}}.
\end{aligned}
$$

したがって、

$$
\begin{aligned}
f(x)g(1/x)\frac1x
&=
\frac{
x^{a+d-1}
}{
(1+x)^{a+b+c+d}
}.
\end{aligned}
$$

よって、

$$
\begin{aligned}
\int_0^\infty
f(x)g(1/x)\frac{dx}{x}
&=
\int_0^\infty
\frac{x^{a+d-1}}
{(1+x)^{a+b+c+d}}
\,dx\\
&=
B(a+d,b+c)\\
&=
\frac{
\Gamma(a+d)\Gamma(b+c)
}{
\Gamma(a+b+c+d)
}.
\end{aligned}
$$

一方、

$$
F(s)G(s)
=
\frac{
\Gamma(a+s)
\Gamma(b+s)
\Gamma(c-s)
\Gamma(d-s)
}{
\Gamma(a+c)\Gamma(b+d)
}.
$$

したがってParseval型公式から、

$$
\begin{aligned}
&\frac{1}{2\pi i}
\int_L
\Gamma(a+s)
\Gamma(b+s)
\Gamma(c-s)
\Gamma(d-s)
\,ds\\
&\qquad=
\Gamma(a+c)\Gamma(b+d)
\frac{
\Gamma(a+d)\Gamma(b+c)
}{
\Gamma(a+b+c+d)
}.
\end{aligned}
$$

すなわち、

$$
\frac{1}{2\pi i}
\int_L
\Gamma(a+s)
\Gamma(b+s)
\Gamma(c-s)
\Gamma(d-s)
\,ds
=
\frac{
\Gamma(a+c)
\Gamma(a+d)
\Gamma(b+c)
\Gamma(b+d)
}{
\Gamma(a+b+c+d)
}.
$$

これで示された。$\square$

## 補足：積分路の意味

$L$ は、左向きに並ぶ極

$$
-a-n,\quad -b-n
$$

と、右向きに並ぶ極

$$
c+n,\quad d+n
$$

を分離するように選ぶ。スターリングの公式により縦方向の減衰を評価でき、上の変形を正当化できる範囲で補題が成立する。

## 関連記事

- [Mellin変換とMellin反転公式](/articles/mellin-transform-inversion.html)
- [代数方程式の解のMellin変換](/articles/mellin-algebraic-transform.html)
