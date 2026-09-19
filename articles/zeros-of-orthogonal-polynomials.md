---
layout: article
title: "直交多項式の零点と交互性"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

直交多項式の重要な性質の一つに、零点が直交区間の内部に現れ、しかも隣り合う次数の零点が交互に並ぶという性質がある。本記事では、この事実を直交性とクリストッフェル・ダルブーの公式から示す。

<div class="math-box theorem-box">

<div class="math-box-title">定理：零点の位置と重複度</div>

$n$ 次の正規直交多項式 $\phi_n$ は、区間 $(a,b)$ に相異なる $n$ 個の零点を持つ。

</div>

## 1. 零点がすべて区間内にあること

$\phi_n$ が $(a,b)$ に持つ奇数重複度の零点を

$$
x_1,x_2,\ldots,x_k
$$

とする。$k<n$ と仮定して矛盾を導く。

$$
p_k(x)
=
(x-x_1)(x-x_2)\cdots(x-x_k)
$$

とおく。$p_k$ の次数は $k<n$ なので、直交性から、

$$
\langle p_k,\phi_n\rangle=0.
$$

一方、$p_k(x)\phi_n(x)$ では、$(a,b)$ 内の奇数重複度の零点が $p_k$ によって打ち消され、符号変化が生じない。必要なら $p_k$ の符号を反転することで、

$$
p_k(x)\phi_n(x)\geq0
$$

としてよい。重み関数 $w(x)>0$ であるから、

$$
\langle p_k,\phi_n\rangle
=
\int_a^b
w(x)p_k(x)\phi_n(x)\,dx
>0
$$

となり、先ほどの

$$
\langle p_k,\phi_n\rangle=0
$$

と矛盾する。

したがって $\phi_n$ は $(a,b)$ 内に $n$ 個の零点を持つ。次数が $n$ なので、これらはすべて単純零点である。

<div class="math-box theorem-box">

<div class="math-box-title">定理：隣り合う次数の零点の交互性</div>

$\phi_n$ と $\phi_{n+1}$ の零点は $(a,b)$ 内で交互に現れ、両者が同じ点を零点として持つことはない。

</div>

## 2. クリストッフェル・ダルブーの公式を使う

$x_r$ を $\phi_n$ の零点とする。対角型のクリストッフェル・ダルブーの公式から、

$$
\sum_{k=0}^{n-1}
\phi_k(x_r)^2
=
-\frac{k_n}{k_{n+1}}
\phi_n'(x_r)\phi_{n+1}(x_r)
>0
$$

を得る。したがって、

$$
\phi_n'(x_r)\phi_{n+1}(x_r)<0.
$$

同様に、隣り合う零点 $x_r,x_{r+1}$ について、

$$
\phi_n'(x_r)\phi_{n+1}(x_r)<0,
$$

$$
\phi_n'(x_{r+1})\phi_{n+1}(x_{r+1})<0
$$

が成り立つ。

$x_r,x_{r+1}$ は $\phi_n$ の単純な隣接零点なので、

$$
\phi_n'(x_r)\phi_n'(x_{r+1})<0.
$$

したがって、

$$
\phi_{n+1}(x_r)\phi_{n+1}(x_{r+1})<0.
$$

$\phi_{n+1}$ は連続なので、中間値の定理より $(x_r,x_{r+1})$ に少なくとも1つ零点を持つ。

同じ議論を逆向きに適用することで、$\phi_{n+1}$ の隣り合う零点の間にも $\phi_n$ の零点が存在する。

## 3. 共通零点を持たないこと

もし、

$$
\phi_{n+1}(x_r)
=
\phi_n(x_r)
=
0
$$

が成り立つと仮定する。3項間漸化式から、

$$
\phi_{n-1}(x_r)=0
$$

となる。同じ議論を繰り返すと、

$$
\phi_{n+1}(x_r)
=
\phi_n(x_r)
=
\cdots
=
\phi_0(x_r)
=
0
$$

となる。しかし $\phi_0$ は $0$ でない定数なので矛盾する。

したがって、隣り合う次数の正規直交多項式は共通零点を持たず、その零点は区間内で交互に並ぶ。

## 次の記事

[直交多項式による最良近似](/articles/best-approximation-orthogonal-polynomials.html)
