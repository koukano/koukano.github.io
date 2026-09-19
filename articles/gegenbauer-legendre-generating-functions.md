---
layout: article
title: "ゲーゲンバウアー多項式とルジャンドル多項式の母関数"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

ゲーゲンバウアー多項式の3項間漸化式を母関数へ変換すると、閉じた形の母関数を導くことができる。さらに、パラメータを特別な値に選ぶことでルジャンドル多項式の母関数が得られる。

## 1. ゲーゲンバウアー多項式の漸化式

ゲーゲンバウアー多項式を $C_n^\lambda(x)$ とすると、

$$
(n+1)C_{n+1}^\lambda(x)
-
2(n+\lambda)xC_n^\lambda(x)
+
(n+2\lambda-1)C_{n-1}^\lambda(x)
=
0
$$

という3項間漸化式を満たす。

初期値は、

$$
C_0^\lambda(x)=1,
\qquad
C_1^\lambda(x)=2\lambda x
$$

である。

## 2. 母関数を導入する

$$
G(x,t)
=
\sum_{n=0}^{\infty}
C_n^\lambda(x)t^n
$$

とおく。

3項間漸化式に $t^n$ を掛けて $n$ について和をとり、$G$ とその $t$ 微分で整理すると、

$$
(1-2xt+t^2)
\frac{\partial G}{\partial t}
=
2\lambda(x-t)G
$$

という微分方程式が得られる。

## 3. 微分方程式を解く

両辺を $G(1-2xt+t^2)$ で割ると、

$$
\frac{1}{G}
\frac{\partial G}{\partial t}
=
\frac{2\lambda(x-t)}
{1-2xt+t^2}.
$$

右辺は、

$$
-\lambda
\frac{\partial}{\partial t}
\log(1-2xt+t^2)
$$

と書けるので、積分すると、

$$
\log G
=
-\lambda
\log(1-2xt+t^2)
+
C.
$$

初期条件

$$
G(x,0)=1
$$

から $C=0$ となり、

<div class="math-box theorem-box">

<div class="math-box-title">ゲーゲンバウアー多項式の母関数</div>

$$
G(x,t)
=
\frac{1}
{(1-2xt+t^2)^\lambda}
=
\sum_{n=0}^{\infty}
C_n^\lambda(x)t^n.
$$

</div>

## 4. ルジャンドル多項式

$\lambda=\frac12$ とすると、

$$
C_n^{1/2}(x)
=
P_n(x)
$$

となり、

<div class="math-box theorem-box">

<div class="math-box-title">ルジャンドル多項式の母関数</div>

$$
\frac{1}
{\sqrt{1-2xt+t^2}}
=
\sum_{n=0}^{\infty}
P_n(x)t^n.
$$

</div>

この母関数は、ルジャンドル多項式を静電ポテンシャルやラプラス方程式と結びつける際にも現れる。

## 5. ノルム

ルジャンドル多項式の直交性と母関数を用いると、

$$
\int_{-1}^{1}
P_n(x)^2\,dx
=
\frac{2}{2n+1}
$$

という規格化が得られる。

## 次の記事

[ルジャンドル多項式とラプラス方程式](/articles/legendre-polynomials-laplace-equation.html)
