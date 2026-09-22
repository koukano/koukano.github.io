---
layout: article
title: "異なる次数の直交多項式の零点の分離（Separation of Zeros of Orthogonal Polynomials of Different Degrees）"
seo_title: "異なる次数の直交多項式の零点の分離｜零点配置の定理"
description: "m>n の直交多項式について、n次多項式の隣り合う零点の間にm次多項式の零点が存在することを証明します。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

隣り合う次数だけでなく、離れた次数の直交多項式の零点にも規則性がある。本記事では、$m>n$ のときの零点の配置をガウスの求積公式を用いて示す。

<div class="math-box theorem-box">

<div class="math-box-title">定理：異なる次数の零点の分離（Separation of Zeros of Different Degrees）</div>

$m>n\geq2$ とする。このとき、$\phi_n$ の隣り合う2つの零点の間には、$\phi_m$ の零点が少なくとも1つ存在する。

</div>

## 証明

$\phi_m$ の零点を

$$
x_1<x_2<\cdots<x_m
$$

とする。これらはすべて単純零点である。

数列

$$
\phi_n(x_1),\phi_n(x_2),\ldots,\phi_n(x_m)
$$

の符号変化を考える。

この数列の符号変化が高々 $n-1$ 回しかないと仮定する。すると、符号が変化する位置に合わせて零点を置くことで、高々 $n-1$ 次の多項式 $p$ を選び、

$$
p(x_k)\phi_n(x_k)\geq0
\qquad
(k=1,\ldots,m)
$$

をすべての $k$ で成り立たせることができる。

さらに $m>n-1$ なので、すべての $x_k$ が $p$ の零点になることはない。したがって少なくとも1つの $k$ について

$$
p(x_k)\phi_n(x_k)>0
$$

となる。

一方、$\deg p\leq n-1$ だから、直交性より

$$
\int_a^b
w(x)p(x)\phi_n(x)\,dx
=
\langle p,\phi_n\rangle
=
0.
$$

ところが、$\phi_m$ の零点 $x_1,\ldots,x_m$ を節点とするガウスの求積公式を $p\phi_n$ に適用できる。実際、

$$
\deg(p\phi_n)
\leq
(n-1)+n
=
2n-1
<
2m-1
$$

である。

したがって、

$$
\int_a^b
w(x)p(x)\phi_n(x)\,dx
=
\sum_{k=1}^{m}
\lambda_{k,m}
p(x_k)\phi_n(x_k).
$$

クリストッフェル数は

$$
\lambda_{k,m}>0
$$

であり、各項は非負、少なくとも1項は正なので、

$$
\sum_{k=1}^{m}
\lambda_{k,m}
p(x_k)\phi_n(x_k)
>0.
$$

これは積分が $0$ であることに矛盾する。

よって数列

$$
\phi_n(x_1),\ldots,\phi_n(x_m)
$$

には少なくとも $n$ 回の符号変化が存在する。

したがって、$\phi_m$ の零点の中から

$$
x_{k_1}<x_{k_2}<\cdots<x_{k_{n+1}}
$$

を選び、

$$
\phi_n(x_{k_1}),
\phi_n(x_{k_2}),
\ldots,
\phi_n(x_{k_{n+1}})
$$

の符号が交互になるようにできる。

中間値の定理より、各区間

$$
(x_{k_j},x_{k_{j+1}})
$$

には $\phi_n$ の零点が少なくとも1つ存在する。

$\phi_n$ の零点は全部で $n$ 個なので、これらが $\phi_n$ のすべての零点である。したがって、$\phi_n$ の隣り合う2つの零点の間には、少なくとも1つの $\phi_m$ の零点が存在する。
<div class="proof-end">\(\square\)</div>

## 次の記事

[有限区間における直交多項式の零点の稠密化](/articles/zeros-dense-orthogonal-polynomials.html)
