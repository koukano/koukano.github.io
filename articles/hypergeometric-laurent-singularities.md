---
layout: article
title: "ローラン展開と特異点：極・留数・真性特異点"
seo_title: "ローラン展開と特異点：極・留数・真性特異点｜超幾何関数"
description: "ローラン展開を特異部と正則部に分け、極の位数、留数、真性特異点を整理します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
---

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

[← べき級数・解析関数・解析接続](/articles/hypergeometric-power-series.html)

[2階線形微分方程式の確定特異点 →](/articles/hypergeometric-regular-singular-points.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)
