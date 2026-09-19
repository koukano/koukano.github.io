---
layout: article
title: "母関数とは何か：エルミート多項式とラゲール多項式"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

多項式列を1つずつ扱う代わりに、すべての次数の多項式を1つの級数にまとめる方法が母関数である。本記事では母関数の定義を確認し、エルミート多項式とラゲール多項式の母関数を扱う。

## 1. 母関数の定義

数列 $\{a_n\}$ に対して、

$$
f(x)
=
\sum_{n=0}^{\infty}
a_nx^n
$$

と表される関数 $f$ を、その数列の母関数という。

同様に、多項式列 $\{\phi_n(x)\}$ に対して、

$$
F(t,x)
=
\sum_{n=0}^{\infty}
a_n\phi_n(x)t^n
$$

という形の級数を考えることで、すべての $\phi_n$ を1つの関数の中にまとめることができる。

## 2. エルミート多項式の母関数

重み $e^{-x^2/2}$ に対応するエルミート多項式では、

<div class="math-box theorem-box">

<div class="math-box-title">エルミート多項式の母関数</div>

$$
e^{-t^2/2+tx}
=
\sum_{n=0}^{\infty}
H_n(x)
\frac{t^n}{n!}.
$$

</div>

右辺を $t$ のべき級数として見れば、$t^n$ の係数から $H_n(x)$ を取り出すことができる。

## 3. ラゲール多項式の母関数

ラゲール多項式 $L_n^\alpha(x)$ については、

<div class="math-box theorem-box">

<div class="math-box-title">ラゲール多項式の母関数</div>

$$
\frac{1}
{(1-t)^{\alpha+1}}
\exp\left(
-\frac{xt}{1-t}
\right)
=
\sum_{n=0}^{\infty}
L_n^\alpha(x)t^n.
$$

</div>

この公式も、右辺の $t^n$ の係数を比較することで各次数のラゲール多項式を取り出せる。

## 4. 母関数を使う利点

母関数を用いると、多項式列全体を1つの関数として扱うことができる。そのため、漸化式の導出、微分公式の導出、積分表示の導出などをまとめて行える。

特に、次の記事ではゲーゲンバウアー多項式の3項間漸化式から母関数を導き、その特殊な場合としてルジャンドル多項式の母関数を得る。

## 次の記事

[ゲーゲンバウアー多項式とルジャンドル多項式の母関数](/articles/gegenbauer-legendre-generating-functions.html)
