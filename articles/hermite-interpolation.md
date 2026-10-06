---
layout: article
title: "エルミート補間（Hermite Interpolation）"
seo_title: "エルミート補間とは？補間公式と剰余項"
description: "関数値と導関数の値を同時に一致させるエルミート補間について、定義、補間多項式、剰余項を数式で整理します。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

ラグランジュ補間では関数値だけを一致させるが、エルミート補間では関数値と導関数の値を同時に一致させる。本記事では、この補間公式と剰余項を扱う。

<div class="math-box definition-box">

<div class="math-box-title">定義：エルミート補間（Hermite Interpolation）</div>

相異なる標本点 $x_1,\ldots,x_n$ に対して、$2n-1$ 次以下の多項式 $F$ が

$$
F(x_k)=f(x_k),
\qquad
F'(x_k)=f'(x_k)
$$

をすべての $1\leq k\leq n$ で満たすとき、$F$ をエルミート補間多項式という。

</div>

## 1. ラグランジュ基本多項式を利用する

$\Phi(x)=\prod_{i=1}^n(x-x_i)$ と定め、ラグランジュ補間で用いた

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

## 2. エルミート補間公式（Hermite Interpolation Formula）

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

<div class="math-box-title">定理：エルミート補間公式（Hermite Interpolation Formula）</div>

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

剰余項では、標本点と評価点を含む実閉区間 $[a,b]$ 上で $f$ が実数値の $C^{2n}$ 関数であるとする。エルミート補間の誤差に対して、

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

## 具体例：両端の値と傾きを指定する

区間 $[0,1]$ で $F(0)=0$、$F'(0)=0$、$F(1)=1$、$F'(1)=0$ を満たす3次以下の多項式を求める。$F(x)=ax^3+bx^2+cx+d$ とおけば、最初の2条件から $c=d=0$、残りから $a+b=1$、$3a+2b=0$ となる。

$$
a=-2,\qquad b=3,\qquad F(x)=3x^2-2x^3.
$$

実際、$F'(x)=6x(1-x)$ は両端で $0$ である。関数値だけの直線補間 $F(x)=x$ と比べ、端点で水平になるという傾きの情報まで反映できている。

## 次の記事

[ガウスの求積公式とクリストッフェル数](/articles/gaussian-quadrature.html)
