---
layout: article
title: "ラグランジュ補間"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

直交多項式による近似から補間公式へ議論を進める。本記事では、まずラグランジュ補間を扱う。

$x_1,\ldots,x_n$ を相異なる標本点とし、$f$ をこれらの点で定義された関数とする。

<div class="math-box definition-box">

<div class="math-box-title">定義：ラグランジュ補間</div>

$n-1$ 次以下の多項式 $F$ が

$$
F(x_k)=f(x_k)
\qquad
(1\leq k\leq n)
$$

を満たすとき、$F$ を $f$ のラグランジュ補間多項式という。

</div>

## 1. 基本多項式

まず、

$$
\Phi(x)
=
\prod_{i=1}^{n}
(x-x_i)
$$

とおく。各 $j$ に対して、

$$
\rho_j(x)
=
\frac{\Phi(x)}
{(x-x_j)\Phi'(x_j)}
$$

と定める。$\rho_j$ は $n-1$ 次多項式であり、

$$
\rho_j(x_k)
=
\delta_{jk}
$$

を満たす。

実際、$k\neq j$ のとき $\Phi(x_k)=0$ なので、

$$
\rho_j(x_k)=0.
$$

一方 $k=j$ では、

$$
\lim_{x\to x_j}
\frac{\Phi(x)}
{(x-x_j)\Phi'(x_j)}
=
1
$$

となる。

## 2. 補間多項式

したがって、

$$
F(x)
=
\sum_{k=1}^{n}
f(x_k)\rho_k(x)
$$

とおけば、

$$
F(x_j)
=
\sum_{k=1}^{n}
f(x_k)\delta_{kj}
=
f(x_j)
$$

となる。これがラグランジュ補間公式である。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ラグランジュ補間公式</div>

相異なる $n$ 点 $x_1,\ldots,x_n$ に対して、

$$
F(x)
=
\sum_{k=1}^{n}
f(x_k)
\frac{\Phi(x)}
{(x-x_k)\Phi'(x_k)}
$$

は $f(x_k)$ を補間する $n-1$ 次以下の多項式である。

</div>

## 3. 剰余項

補間誤差についても扱う。$F$ をラグランジュ補間多項式とし、

$$
g(x)=f(x)-F(x)
$$

とおく。新しい点 $x$ をとり、

$$
g(x)=K\Phi(x)
$$

となるように $K$ を定める。$g(t)-K\Phi(t)$ は $n+1$ 個の零点を持つため、ロルの定理を繰り返し適用すると、ある $\xi$ が存在して、

$$
g^{(n)}(\xi)
-
K\Phi^{(n)}(\xi)
=
0
$$

となる。

$\Phi$ がモニックな $n$ 次多項式である場合、

$$
\Phi^{(n)}(\xi)=n!
$$

なので、

$$
K
=
\frac{f^{(n)}(\xi)}
{n!}
$$

となり、

$$
f(x)-F(x)
=
\frac{f^{(n)}(\xi)}
{n!}
\Phi(x)
$$

という形の剰余項が得られる。

## 次の記事

[エルミート補間](/articles/hermite-interpolation.html)
