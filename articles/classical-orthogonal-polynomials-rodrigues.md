---
layout: article
title: "ロドリゲスの公式と古典的直交多項式"
seo_title: "ロドリゲスの公式とは？古典的直交多項式を統一的に表す公式"
description: "ロドリゲスの公式を用いて、ヤコビ・ルジャンドル・チェビシェフ・ゲーゲンバウアー・ラゲール・エルミート多項式を整理します。"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

古典的直交多項式の多くは、重み関数と高階微分を用いるロドリゲスの公式によって統一的に表すことができる。本記事では、有限区間におけるヤコビ多項式から始め、ルジャンドル多項式、チェビシェフ多項式、ゲーゲンバウアー多項式、さらに無限区間におけるラゲール多項式とエルミート多項式までを整理する。

## 1. 有限区間におけるロドリゲスの公式

区間 $[-1,1]$ 上で重み関数 $w(x)$ を考える。$w$ が必要な回数だけ微分可能であり、端点で適切な消滅条件を満たすとき、

$$
P_n(x)
=
\frac{1}{w(x)}
\left(\frac{d}{dx}\right)^n
\left[
w(x)(1-x^2)^n
\right]
$$

という形の多項式を考えることができる。

このとき $0\leq k<n$ に対して、

$$
\int_{-1}^{1}
w(x)P_n(x)x^k\,dx
=
0
$$

が成り立つ。実際、ロドリゲスの公式を代入して部分積分を $n$ 回繰り返すと、$x^k$ は $n$ 回微分する前に $0$ となり、端点項も消える。

<div class="math-box theorem-box">

<div class="math-box-title">ロドリゲスの公式から得られる直交性</div>

$$
P_n(x)
=
\frac{1}{w(x)}
\left(\frac{d}{dx}\right)^n
\left[
w(x)(1-x^2)^n
\right]
$$

とし、境界項がすべて消えるとする。このとき、

$$
\int_{-1}^{1}
w(x)P_n(x)x^k\,dx
=
0
\qquad
(0\leq k<n)
$$

が成り立つ。

</div>

## 2. 重み関数の形

$n=1$ の場合を考えると、

$$
P_1(x)
=
\frac{1}{w(x)}
\frac{d}{dx}
\left[
w(x)(1-x^2)
\right]
$$

である。$P_1$ が1次多項式になるためには、

$$
\frac{w'(x)}{w(x)}(1-x^2)-2x
=
Ax+B
$$

となる定数 $A,B$ が存在すればよい。したがって、

$$
\frac{w'(x)}{w(x)}
=
\frac{(A+2)x+B}{1-x^2}.
$$

これを積分すると、定数 $C$ を用いて、

$$
w(x)
=
C(1-x)^\alpha(1+x)^\beta
$$

という形を得る。積分可能性を考えると、

$$
\alpha>-1,
\qquad
\beta>-1
$$

が必要になる。

## 3. ヤコビ多項式

重み関数

$$
w(x)
=
(1-x)^\alpha(1+x)^\beta
$$

に対して、定数因子を調整したロドリゲスの公式からヤコビ多項式が得られる。

<div class="math-box definition-box">

<div class="math-box-title">ヤコビ多項式</div>

$$
P_n^{(\alpha,\beta)}(x)
=
\frac{(-1)^n}{2^n n!}
(1-x)^{-\alpha}
(1+x)^{-\beta}
\frac{d^n}{dx^n}
\left[
(1-x)^{n+\alpha}
(1+x)^{n+\beta}
\right].
$$

</div>

ヤコビ多項式は、パラメータ $\alpha,\beta$ の選び方によって複数の代表的な直交多項式を含む。

## 4. ルジャンドル多項式

$\alpha=\beta=0$ とすると、

$$
P_n(x)
=
\frac{(-1)^n}{2^n n!}
\frac{d^n}{dx^n}
(1-x^2)^n
$$

を得る。これがルジャンドル多項式のロドリゲス表示である。

## 5. チェビシェフ多項式とゲーゲンバウアー多項式

$\alpha=\beta=-\frac12$ とすると、適切な定数倍によってチェビシェフ多項式が得られる。また、$\alpha=\beta$ としたヤコビ多項式の特別な場合としてゲーゲンバウアー多項式が現れる。

このように、ヤコビ多項式は有限区間 $[-1,1]$ 上の複数の古典的直交多項式をまとめる枠組みになっている。

## 6. ラゲール多項式

半無限区間 $(0,\infty)$ では、

$$
w(x)
=
x^\alpha e^{-x}
$$

という重み関数を考える。

<div class="math-box definition-box">

<div class="math-box-title">ラゲール多項式</div>

$$
L_n^\alpha(x)
=
\frac{1}{n!}
x^{-\alpha}e^x
\left(\frac{d}{dx}\right)^n
\left(
e^{-x}x^{n+\alpha}
\right).
$$

</div>

この形でも、部分積分によって低次数の多項式との直交性を確認できる。

## 7. エルミート多項式

全実軸 $(-\infty,\infty)$ では、

$$
w(x)
=
e^{-x^2/2}
$$

を重み関数として用いる。

<div class="math-box definition-box">

<div class="math-box-title">エルミート多項式</div>

$$
H_n(x)
=
(-1)^n
e^{x^2/2}
\left(\frac{d}{dx}\right)^n
e^{-x^2/2}.
$$

</div>

ここでのエルミート多項式は、重み $e^{-x^2/2}$ に対応する規格化を用いている。

## 8. まとめ

古典的直交多項式は、重み関数とロドリゲスの公式を通して統一的に理解できる。有限区間ではヤコビ多項式が中心となり、その特殊な場合としてルジャンドル多項式、チェビシェフ多項式、ゲーゲンバウアー多項式が現れる。一方、半無限区間ではラゲール多項式、全実軸ではエルミート多項式が現れる。

## 次の記事

[古典的直交多項式が満たす微分方程式](/articles/classical-orthogonal-polynomials-differential-equations.html)
