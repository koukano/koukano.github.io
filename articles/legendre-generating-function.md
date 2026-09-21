---
layout: article
title: "ルジャンドル多項式の母関数"
seo_title: "ルジャンドル多項式の母関数｜公式と導出"
description: "ルジャンドル多項式 P_n(x) の母関数 1/√(1-2xt+t²) を、ゲーゲンバウアー多項式との関係から導きます。"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

ルジャンドル多項式は、ゲーゲンバウアー多項式の特殊な場合として得られる。その母関数も同様に導かれる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ルジャンドル多項式の母関数</div>

$$
\frac{1}{\sqrt{1-2xt+t^2}}
=
\sum_{n=0}^{\infty}
P_n(x)t^n.
$$

</div>

## 証明

ゲーゲンバウアー多項式の母関数

$$
\frac{1}{(1-2xt+t^2)^\lambda}
=
\sum_{n=0}^{\infty}
C_n^\lambda(x)t^n
$$

において、

$$
\lambda=\frac12
$$

とおく。

このとき、

$$
C_n^{1/2}(x)=P_n(x)
$$

であるため、

$$
\frac{1}{\sqrt{1-2xt+t^2}}
=
\sum_{n=0}^{\infty}
P_n(x)t^n
$$

を得る。$\square$

## 関連記事

- [ゲーゲンバウアー多項式の母関数](/articles/gegenbauer-legendre-generating-functions.html)
- [ルジャンドル多項式とラプラス方程式](/articles/legendre-polynomials-laplace-equation.html)
