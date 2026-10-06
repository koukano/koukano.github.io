---
layout: article
title: "ラゲール多項式の母関数（Generating Function for Laguerre Polynomials）"
seo_title: "ラゲール多項式の母関数｜一般化ラゲール多項式の公式"
description: "一般化ラゲール多項式 L_n^α(x) の母関数を示し、|t|<1 における公式を数式とともに整理します。"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

一般化ラゲール多項式 $L_n^\alpha(x)$ の母関数を求める。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ラゲール多項式の母関数（Generating Function for Laguerre Polynomials）</div>

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

これで示された。
<div class="proof-end">\(\square\)</div>

## 具体例：α = 0 の母関数を2次まで展開する

$\alpha=0$ とし、$x$ を固定する。幾何級数と指数関数の展開を掛け合わせると、

$$
\begin{aligned}
\frac1{1-t}\exp\left(-\frac{xt}{1-t}\right)
&=(1+t+t^2+O(t^3))\\
&\quad\cdot\left(1-xt+\left(\frac{x^2}{2}-x\right)t^2+O(t^3)\right)\\
&=1+(1-x)t+\left(1-2x+\frac{x^2}{2}\right)t^2+O(t^3).
\end{aligned}
$$

したがって $L_0^0=1$、$L_1^0=1-x$、$L_2^0=1-2x+x^2/2$ である。この母関数では $t^n$ の係数がそのまま $L_n^0(x)$ になる。

## 次の記事

[ゲーゲンバウアー多項式の母関数](/articles/gegenbauer-legendre-generating-functions.html)
