---
layout: article
title: "ゲーゲンバウアー多項式の母関数"
seo_title: "ゲーゲンバウアー多項式の母関数｜公式と導出"
description: "ゲーゲンバウアー多項式 C_n^λ(x) の母関数 (1-2xt+t²)^(-λ) を3項間漸化式から導きます。"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

ゲーゲンバウアー多項式の3項間漸化式から母関数を導く。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ゲーゲンバウアー多項式の母関数</div>

$$
\frac{1}{(1-2xt+t^2)^\lambda}
=
\sum_{n=0}^{\infty}
C_n^\lambda(x)t^n.
$$

</div>

## 証明

ゲーゲンバウアー多項式は

$$
(n+1)C_{n+1}^\lambda(x)
-
2(n+\lambda)xC_n^\lambda(x)
+
(n+2\lambda-1)C_{n-1}^\lambda(x)
=
0
$$

を満たす。

母関数を

$$
G(x,t)
=
\sum_{n=0}^{\infty}
C_n^\lambda(x)t^n
$$

とおく。

漸化式に $t^n$ を掛けて $n\geq0$ について和をとり、初期値

$$
C_0^\lambda(x)=1,
\qquad
C_1^\lambda(x)=2\lambda x
$$

を用いて整理すると、

$$
(1-2xt+t^2)
\frac{\partial G}{\partial t}
=
2\lambda(x-t)G
$$

を得る。

したがって、

$$
\frac{1}{G}
\frac{\partial G}{\partial t}
=
\frac{2\lambda(x-t)}
{1-2xt+t^2}.
$$

右辺は

$$
-\lambda
\frac{\partial}{\partial t}
\log(1-2xt+t^2)
$$

なので、$t$ について積分すると、

$$
\log G
=
-\lambda
\log(1-2xt+t^2)
+
C(x).
$$

$t=0$ では $G(x,0)=C_0^\lambda(x)=1$ だから $C(x)=0$ である。

よって、

$$
G(x,t)
=
(1-2xt+t^2)^{-\lambda}.
$$

したがって、

$$
\frac{1}{(1-2xt+t^2)^\lambda}
=
\sum_{n=0}^{\infty}
C_n^\lambda(x)t^n.
$$

$\square$

## 次の記事

[ルジャンドル多項式の母関数](/articles/legendre-generating-function.html)
