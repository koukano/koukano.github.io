---
layout: article
title: "エルミート多項式の母関数（Generating Function for Hermite Polynomials）"
seo_title: "エルミート多項式の母関数｜公式と導出"
description: "エルミート多項式の母関数を定義から導き、各次数の多項式を1つの生成関数にまとめる方法を解説します。"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

重み $e^{-x^2/2}$ に対応するエルミート多項式

$$
H_n(x)
=
(-1)^n e^{x^2/2}
\frac{d^n}{dx^n}e^{-x^2/2}
$$

について、すべての次数を1つの関数にまとめる母関数を求める。

<div class="math-box theorem-box">

<div class="math-box-title">定理：エルミート多項式の母関数（Generating Function for Hermite Polynomials）</div>

$$
e^{-t^2/2+tx}
=
\sum_{n=0}^{\infty}
H_n(x)\frac{t^n}{n!}.
$$

</div>

## 証明

$$
e^{-t^2/2+tx}
=
e^{x^2/2}
e^{-(x-t)^2/2}
$$

と変形する。

関数

$$
f(x)=e^{-x^2/2}
$$

を考えると、テイラー展開より

$$
f(x-t)
=
\sum_{n=0}^{\infty}
\frac{(-t)^n}{n!}
f^{(n)}(x).
$$

両辺に $e^{x^2/2}$ を掛けると、

$$
e^{x^2/2}e^{-(x-t)^2/2}
=
\sum_{n=0}^{\infty}
\frac{t^n}{n!}
\left[
(-1)^n
e^{x^2/2}
\frac{d^n}{dx^n}
e^{-x^2/2}
\right].
$$

角括弧の中はロドリゲスの公式による $H_n(x)$ である。したがって、

$$
e^{-t^2/2+tx}
=
\sum_{n=0}^{\infty}
H_n(x)\frac{t^n}{n!}
$$

を得る。
<div class="proof-end">\(\square\)</div>

## 具体例：母関数から最初の4項を読み取る

本文と同じ、重み $e^{-x^2/2}$ の規格化を使う。$x$ を固定して指数関数を $t=0$ で展開すると、

$$
e^{xt-t^2/2}
=1+xt+\frac{x^2-1}{2}t^2+\frac{x^3-3x}{6}t^3+O(t^4).
$$

母関数の係数は $H_n(x)/n!$ なので、

$$
H_0=1,\qquad H_1=x,\qquad H_2=x^2-1,\qquad H_3=x^3-3x.
$$

例えば $t^2$ の係数をそのまま $H_2$ と読むと2倍ずれる。指数型母関数では、係数に $n!$ を掛けて多項式を取り出す。

## 次の記事

[ラゲール多項式の母関数](/articles/laguerre-generating-function.html)
