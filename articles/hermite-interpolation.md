---
layout: article
title: "エルミート補間"
seo_title: "エルミート補間とは？補間公式と剰余項"
description: "関数値と導関数の値を同時に一致させるエルミート補間について、定義、補間多項式、剰余項を数式で整理します。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

ラグランジュ補間では関数値だけを一致させるが、エルミート補間では関数値と導関数の値を同時に一致させる。本記事では、この補間公式と剰余項を扱う。

<div class="math-box definition-box">

<div class="math-box-title">定義：エルミート補間</div>

相異なる標本点 $x_1,\ldots,x_n$ に対して、$2n-1$ 次以下の多項式 $F$ が

$$
F(x_k)=f(x_k),
\qquad
F'(x_k)=f'(x_k)
$$

をすべての $1\leq k\leq n$ で満たすとき、$F$ をエルミート補間多項式という。

</div>

## 1. ラグランジュ基本多項式を利用する

ラグランジュ補間で用いた

$$
\rho_j(x)
=
\frac{\Phi(x)}
{(x-x_j)\Phi'(x_j)}
$$

を使う。

ここでは、

$$
\tau_j(x)
=
(x-x_j)\rho_j(x)^2
$$

および、

$$
\sigma_j(x)
=
\left[
1
-
(x-x_j)
\frac{\Phi''(x_j)}
{\Phi'(x_j)}
\right]
\rho_j(x)^2
$$

を導入する。

これらは、

$$
\sigma_j(x_k)=\delta_{jk},
\qquad
\sigma_j'(x_k)=0,
$$

$$
\tau_j(x_k)=0,
\qquad
\tau_j'(x_k)=\delta_{jk}
$$

を満たす。

## 2. エルミート補間公式

したがって、

$$
F(x)
=
\sum_{k=1}^{n}
\left[
f(x_k)\sigma_k(x)
+
f'(x_k)\tau_k(x)
\right]
$$

とおけば、

$$
F(x_j)=f(x_j),
\qquad
F'(x_j)=f'(x_j)
$$

が成り立つ。

<div class="math-box theorem-box">

<div class="math-box-title">定理：エルミート補間公式</div>

上で定義した $\sigma_k,\tau_k$ を用いると、

$$
F(x)
=
\sum_{k=1}^{n}
\left[
f(x_k)\sigma_k(x)
+
f'(x_k)\tau_k(x)
\right]
$$

は $f$ の値と1階導関数の値を各標本点で一致させる。

</div>

## 3. 剰余項

エルミート補間の誤差に対して、

$$
g(x)
=
f(x)-F(x)-K\Phi(x)^2
$$

を考えている。$F$ は各 $x_k$ で関数値と1階導関数を一致させるため、

$$
g(x_k)=g'(x_k)=0.
$$

したがって各 $x_k$ は少なくとも2重零点となる。さらに新しい点 $x$ で $g(x)=0$ となるよう $K$ を選び、ロルの定理を繰り返すことで、ある $\xi$ に対して、

$$
g^{(2n)}(\xi)=0
$$

を得る。

$\Phi$ の最高次係数を $k_n$ とすると、

$$
K
=
\frac{f^{(2n)}(\xi)}
{k_n^2(2n)!}
$$

となり、

$$
f(x)-F(x)
=
\frac{f^{(2n)}(\xi)}
{k_n^2(2n)!}
\Phi(x)^2
$$

という形の剰余項が得られる。

## 次の記事

[ガウスの求積公式とクリストッフェル数](/articles/gaussian-quadrature.html)
