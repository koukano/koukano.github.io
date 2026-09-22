---
layout: article
title: "直交多項式の零点：区間内の単純零点"
seo_title: "直交多項式の零点｜区間内にn個の単純零点を持つ理由"
description: "n次の正規直交多項式が直交区間の内部にちょうどn個の相異なる単純零点を持つことを、直交性を用いて証明します。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

直交多項式の基本的な性質として、$n$ 次の正規直交多項式は直交区間の内部にちょうど $n$ 個の相異なる零点を持つ。本記事では、この定理だけを扱い、直交性を用いて証明する。

$n$ 次の正規直交多項式を $\phi_n$ とし、内積を

$$
\langle f,g\rangle
=
\int_a^b w(x)f(x)g(x)\,dx
$$

とする。重み関数は $(a,b)$ 上で正であるとする。

<div class="math-box theorem-box">

<div class="math-box-title">定理：直交多項式の零点</div>

$n$ 次の正規直交多項式 $\phi_n$ は、区間 $(a,b)$ に相異なる $n$ 個の零点を持つ。すなわち、すべての零点は $(a,b)$ の内部にあり、しかもすべて単純零点である。

</div>

## 証明

$\phi_n$ が $(a,b)$ 内に持つ、奇数重複度の零点を

$$
x_1,x_2,\ldots,x_k
$$

とする。$\phi_n$ は $n$ 次多項式なので $k\leq n$ である。ここで $k<n$ と仮定して矛盾を導く。

次の $k$ 次多項式を考える。

$$
p_k(x)
=
(x-x_1)(x-x_2)\cdots(x-x_k).
$$

$k<n$ なので、$p_k$ は $\phi_0,\phi_1,\ldots,\phi_{n-1}$ の線形結合として表せる。したがって $\phi_n$ の直交性から

$$
\langle p_k,\phi_n\rangle=0
$$

である。

一方、$p_k$ は $\phi_n$ の奇数重複度の零点を一つずつ因子として持つ。そのため積

$$
p_k(x)\phi_n(x)
$$

では、$(a,b)$ 内の零点の重複度がすべて偶数になる。よってこの積は $(a,b)$ で符号を変えない。

必要なら $p_k$ 全体に $-1$ を掛けることで、

$$
p_k(x)\phi_n(x)\geq0
\qquad (a<x<b)
$$

としてよい。

しかも $p_k\phi_n$ は恒等的に $0$ ではない。重み関数 $w(x)$ は $(a,b)$ 上で正なので、

$$
\langle p_k,\phi_n\rangle
=
\int_a^b
w(x)p_k(x)\phi_n(x)\,dx
>0
$$

となる。

これは先ほどの

$$
\langle p_k,\phi_n\rangle=0
$$

に矛盾する。

したがって $k<n$ は不可能であり、

$$
k=n
$$

でなければならない。つまり $\phi_n$ は $(a,b)$ 内に少なくとも $n$ 個の奇数重複度の零点を持つ。

しかし $\phi_n$ は $n$ 次多項式なので、零点の総数は重複度込みで高々 $n$ 個である。したがって、これら $n$ 個の零点はすべて相異なり、重複度はすべて $1$ である。

よって $\phi_n$ は $(a,b)$ に相異なる $n$ 個の単純零点を持つ。
<div class="proof-end">\(\square\)</div>

## 次の記事

[直交多項式の零点の交互性](/articles/interlacing-zeros-of-orthogonal-polynomials.html)
