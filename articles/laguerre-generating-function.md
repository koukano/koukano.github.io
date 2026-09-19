---
layout: article
title: "ラゲール多項式の母関数"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

一般化ラゲール多項式 $L_n^\alpha(x)$ の母関数を求める。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ラゲール多項式の母関数</div>

$|t|<1$ のとき、

$$
\frac{1}{(1-t)^{\alpha+1}}
\exp\left(
-\frac{xt}{1-t}
\right)
=
\sum_{n=0}^{\infty}
L_n^\alpha(x)t^n.
$$

</div>

## 証明

ロドリゲスの公式から、一般化ラゲール多項式は

$$
L_n^\alpha(x)
=
\sum_{k=0}^{n}
(-1)^k
\binom{n+\alpha}{n-k}
\frac{x^k}{k!}
$$

と書ける。

したがって、

$$
\sum_{n=0}^{\infty}
L_n^\alpha(x)t^n
=
\sum_{n=0}^{\infty}
\sum_{k=0}^{n}
(-1)^k
\binom{n+\alpha}{n-k}
\frac{x^k}{k!}t^n.
$$

$n=m+k$ とおいて和の順序を入れ替えると、

$$
\sum_{k=0}^{\infty}
\frac{(-x)^k}{k!}
t^k
\sum_{m=0}^{\infty}
\binom{m+k+\alpha}{m}
t^m.
$$

一般化二項定理より、

$$
\sum_{m=0}^{\infty}
\binom{m+k+\alpha}{m}
t^m
=
(1-t)^{-k-\alpha-1}.
$$

したがって、

$$
\begin{aligned}
\sum_{n=0}^{\infty}
L_n^\alpha(x)t^n
&=
\sum_{k=0}^{\infty}
\frac{(-x)^k}{k!}
t^k
(1-t)^{-k-\alpha-1}\\
&=
(1-t)^{-\alpha-1}
\sum_{k=0}^{\infty}
\frac1{k!}
\left(
-\frac{xt}{1-t}
\right)^k\\
&=
\frac{1}{(1-t)^{\alpha+1}}
\exp\left(
-\frac{xt}{1-t}
\right).
\end{aligned}
$$

これで示された。$\square$

## 次の記事

[ゲーゲンバウアー多項式の母関数](/articles/gegenbauer-legendre-generating-functions.html)
