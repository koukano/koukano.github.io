---
layout: article
title: "高次数の直交多項式と零点の分布"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

直交多項式の零点には、隣り合う次数だけでなく、離れた次数の間にも規則性がある。本記事では、ガウスの求積公式を利用して零点の分布をさらに詳しく調べる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：異なる次数の零点の間隔</div>

$m>n\geq2$ とする。このとき、$\phi_n$ の隣り合う2つの零点の間には、$\phi_m$ の零点が少なくとも1つ存在する。

</div>

## 1. $\phi_m$ の零点で $\phi_n$ の符号を見る

$\phi_m$ の零点を

$$
x_1<x_2<\cdots<x_m
$$

とする。数列

$$
\phi_n(x_1),
\phi_n(x_2),
\ldots,
\phi_n(x_m)
$$

の符号変化を考える。

もし符号変化が少なすぎると仮定すると、高々 $n-1$ 次の多項式 $p$ を選んで、

$$
p(x_k)\phi_n(x_k)\geq0
$$

をすべての $k$ で成り立たせることができ、少なくとも1点では厳密な不等号が成り立つ。

一方、$p$ の次数は $n-1$ 以下なので、直交性から、

$$
\int_a^b
w(x)p(x)\phi_n(x)\,dx
=
0.
$$

ところが、$\phi_m$ の零点を標本点とするガウスの求積公式を用いると、

$$
\int_a^b
w(x)p(x)\phi_n(x)\,dx
=
\sum_{k=1}^{m}
p(x_k)\phi_n(x_k)\lambda_{k,m}.
$$

クリストッフェル数は正なので右辺は正になり、矛盾する。

この議論から、$\phi_m$ の零点を並べたとき $\phi_n$ の値は十分な回数だけ符号を変えなければならず、中間値の定理によって零点の配置に制約が生じる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：有限区間における零点の稠密化</div>

$(\alpha,\beta)$ を $(a,b)$ の任意の部分区間とする。区間 $(a,b)$ が有界であるとき、$n$ を十分大きくすれば $\phi_n$ は $(\alpha,\beta)$ に少なくとも1つ零点を持つ。

</div>

## 2. ワイエルシュトラスの近似定理を使う

$(\alpha,\beta)$ の内部では正、外部では負になるような連続関数を考える。十分小さい $\varepsilon>0$ に対して、

$$
f(x)
=
\begin{cases}
(x-\alpha)(\beta-x)-\varepsilon,
& x\in(\alpha,\beta),\\
-\varepsilon,
& x\notin(\alpha,\beta)
\end{cases}
$$

のような関数を用いている。

ワイエルシュトラスの近似定理により、この $f$ を一様に近似する多項式 $p$ をとることができる。$\varepsilon$ を十分小さく選べば、

$$
\int_a^b
w(x)p(x)\,dx
>
0
$$

となる一方、$(\alpha,\beta)$ の外では $p(x)<0$ とできる。

もし $\phi_n$ が $(\alpha,\beta)$ に零点を持たないと仮定すると、$\phi_n$ のすべての零点は区間の外にある。ガウスの求積公式から、

$$
\int_a^b
w(x)p(x)\,dx
=
\sum_{k=1}^{n}
p(x_k)\lambda_{k,n}
$$

となるが、$\lambda_{k,n}>0$ かつ $p(x_k)<0$ なので右辺は負になる。これは積分が正であることに矛盾する。

したがって、高次数の直交多項式の零点は有限区間の内部に次第に広く分布していく。

## 3. 無限区間の場合

この零点の稠密化に関する結果は $(a,b)$ が無限区間の場合にはそのまま成立しない。有限区間という仮定が重要である。

## 次の記事

[ベッセルの不等式とパーセヴァルの等式](/articles/bessel-parseval-orthogonal-polynomials.html)
