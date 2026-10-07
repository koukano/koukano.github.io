---
layout: article
title: "ルジャンドル多項式の母関数（Generating Function for Legendre Polynomials）"
seo_title: "ルジャンドル多項式の母関数｜公式と導出"
description: "ルジャンドル多項式 P_n(x) の母関数 1/√(1-2xt+t²) を、ゲーゲンバウアー多項式との関係から導きます。"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
  - 'NIST, <a href="https://dlmf.nist.gov/18.12#E11">Digital Library of Mathematical Functions: Generating Functions: Legendre</a>.'
---

ルジャンドル多項式は、ゲーゲンバウアー多項式の特殊な場合として得られる。その母関数も同様に導かれる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ルジャンドル多項式の母関数（Generating Function for Legendre Polynomials）</div>

$x\in[-1,1]$、$|t|<1$ とし、平方根は $t=0$ で値 $1$ をとる正則な分枝を選ぶ。このとき、

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

を得る。
<div class="proof-end">\(\square\)</div>

## 具体例：母関数から P₂ を取り出す

一般化二項定理の展開

$$
(1+u)^{-1/2}=1-u/2+3u^2/8+O(u^3)
$$

に $u=-2xt+t^2$ を代入する。$x\in[-1,1]$ を固定し、$t^2$ まで整理すると、

$$
\frac1{\sqrt{1-2xt+t^2}}
=1+xt+\frac{3x^2-1}{2}t^2+O(t^3).
$$

したがって $P_0=1$、$P_1=x$、$P_2=(3x^2-1)/2$ を読み取れる。例えば $x=0$ では $1/\sqrt{1+t^2}=1-t^2/2+\cdots$ となり、$P_2(0)=-1/2$ と一致する。

## 関連記事

- [ゲーゲンバウアー多項式の母関数](/articles/gegenbauer-legendre-generating-functions.html)
- [ルジャンドル多項式とラプラス方程式](/articles/legendre-polynomials-laplace-equation.html)
