---
layout: article
title: "級数展開と特異点：べき級数からローラン展開まで"
seo_title: "級数展開と特異点：べき級数からローラン展開まで｜超幾何関数"
description: "べき級数・解析接続からローラン展開、極、留数、真性特異点までを続けて解説します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
---

微分方程式の級数解を考える前に、解析関数と特異点の基本を押さえよう。

## この記事の目次

- [べき級数・解析関数・解析接続](#power-series)
- [ローラン展開と特異点：極・留数・真性特異点](#laurent-singularities)

<h2 id="power-series">べき級数・解析関数・解析接続</h2>

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：べき級数（Power Series）</div>

中心を $c\in\mathbb C$ とする級数

$$
\sum_{n=0}^{\infty}a_n(z-c)^n
=a_0+a_1(z-c)+\cdots
$$

を、$c$ を中心とするべき級数という。

</div>

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：解析関数（Analytic Function）</div>

定義域 $D$ の各点 $c$ を中心とするべき級数で表せる関数 $f(z)$ を解析関数という。ここで、級数は正の収束半径を持ち、その和が $f(z)$ に等しいものとする。

</div>

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：解析接続（Analytic Continuation）</div>

$D$ を含む定義域 $G$ に定義された解析関数 $g$ が、$D\cap G$ 上で $f$ と等しいとき、$g$ を $f$ の解析接続という。

</div>

<h2 id="laurent-singularities">ローラン展開と特異点：極・留数・真性特異点</h2>

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：ローラン展開の特異部と正則部（Laurent Expansion）</div>

$f(z)$ が円環領域

$$
0\leq r<|z-c|<\rho
$$

で解析的であるとき、ローラン展開を

$$
f(z)=\sum_{k=1}^{\infty}\frac{a_{-k}}{(z-c)^k}
+\sum_{n=0}^{\infty}a_n(z-c)^n
$$

と書く。負のべきからなる部分を**特異部**、非負のべきからなる部分を**正則部**という。

</div>

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：極・留数・真性特異点（Poles, Residues and Essential Singularities）</div>

中心 $c$ の穿孔近傍でローラン展開を考える。

特異部が有限で、最高の負のべきが $(z-c)^{-\ell}$ であるとき、$z=c$ は $\ell$ 位の極である。係数 $a_{-1}$ は $c$ における留数で、

$$
\operatorname{Res}(f,c)=a_{-1}
$$

と表す。特異部が無限項からなる場合、$z=c$ は真性特異点である。関数が正則でない点を特異点という。

</div>

## 続けて読む

[確定特異点とフロベニウス法：特性指数・対数解・フックスの関係式 →](/articles/hypergeometric-frobenius-solutions.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)
