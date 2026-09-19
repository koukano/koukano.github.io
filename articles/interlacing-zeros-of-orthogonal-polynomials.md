---
layout: article
title: "直交多項式の零点の交互性"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

$n$ 次と $(n+1)$ 次の正規直交多項式の零点には、互い違いに並ぶという重要な性質がある。本記事では、この交互性だけを扱う。

前の記事で、$\phi_n$ は直交区間 $(a,b)$ に相異なる $n$ 個の単純零点を持つことを示した。

<div class="math-box theorem-box">

<div class="math-box-title">定理：隣り合う次数の零点の交互性</div>

$\phi_n$ と $\phi_{n+1}$ の零点は区間 $(a,b)$ で交互に現れる。また、$\phi_n$ と $\phi_{n+1}$ は共通の零点を持たない。

</div>

## 証明

$\phi_n$ の隣り合う零点を

$$
x_r<x_{r+1}
$$

とする。

クリストッフェル・ダルブーの公式の対角形から、

$$
\sum_{k=0}^{n-1}\phi_k(x)^2
=
\frac{k_n}{k_{n+1}}
\left[
\phi_n(x)\phi_{n+1}'(x)
-
\phi_n'(x)\phi_{n+1}(x)
\right]
$$

が成り立つ。

$x=x_r$ では $\phi_n(x_r)=0$ なので、

$$
\sum_{k=0}^{n-1}\phi_k(x_r)^2
=
-
\frac{k_n}{k_{n+1}}
\phi_n'(x_r)\phi_{n+1}(x_r).
$$

左辺は正であり、$k_n/k_{n+1}>0$ だから、

$$
\phi_n'(x_r)\phi_{n+1}(x_r)<0.
$$

同様に、

$$
\phi_n'(x_{r+1})\phi_{n+1}(x_{r+1})<0.
$$

一方、$x_r$ と $x_{r+1}$ は $\phi_n$ の隣り合う単純零点である。したがって $\phi_n$ は各零点を通過するたびに符号を変え、

$$
\phi_n'(x_r)\phi_n'(x_{r+1})<0
$$

となる。

上の3つの不等式を合わせると、

$$
\phi_{n+1}(x_r)\phi_{n+1}(x_{r+1})<0
$$

を得る。

$\phi_{n+1}$ は連続なので、中間値の定理から

$$
(x_r,x_{r+1})
$$

の中に $\phi_{n+1}$ の零点が少なくとも1つ存在する。

$\phi_n$ には $n$ 個、$\phi_{n+1}$ には $n+1$ 個の単純零点があるため、この性質を各隣接零点に適用すると、両者の零点は区間内で交互に並ぶことが分かる。

最後に、共通零点を持たないことを示す。ある点 $x_0$ で

$$
\phi_n(x_0)=\phi_{n+1}(x_0)=0
$$

と仮定する。

3項間漸化式

$$
\phi_{n+1}(x)
-
(A_nx+B_n)\phi_n(x)
+
C_n\phi_{n-1}(x)
=
0
$$

に $x=x_0$ を代入すると、

$$
C_n\phi_{n-1}(x_0)=0.
$$

$C_n>0$ なので、

$$
\phi_{n-1}(x_0)=0.
$$

同じ議論を繰り返すと、

$$
\phi_{n+1}(x_0)
=
\phi_n(x_0)
=
\cdots
=
\phi_0(x_0)
=
0
$$

となる。

しかし $\phi_0$ は $0$ でない定数多項式であるから矛盾する。

したがって $\phi_n$ と $\phi_{n+1}$ は共通零点を持たず、その零点は交互に現れる。$\square$

## 関連記事

- [直交多項式の零点：区間内の単純零点](/articles/zeros-of-orthogonal-polynomials.html)
- [クリストッフェル・ダルブーの公式](/articles/christoffel-darboux-formula.html)
