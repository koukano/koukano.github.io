---
layout: article
title: "フロベニウス法：漸化式・整数差・対数解"
seo_title: "フロベニウス法：漸化式・整数差・対数解｜超幾何関数"
description: "特性指数から級数の漸化式を求め、指数差が整数でない場合と整数の場合の解の形を整理します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
  - "NIST, <a href=\"https://dlmf.nist.gov/2.7#i\">Digital Library of Mathematical Functions: Regular Singularities: Fuchs–Frobenius Theory</a>."
---

[特性方程式の導出](/articles/hypergeometric-indicial-equation.html)で扱った $y''+P(x)y'+Q(x)y=0$ を考え、特性指数を $\alpha,\beta$ とする。$y=x^\alpha u$ による変換後の係数を

$$
\widetilde P(x)=P(x)+\frac{2\alpha}{x},
\qquad
\widetilde Q(x)=Q(x)+\frac{\alpha P(x)}x
+\frac{\alpha(\alpha-1)}{x^2}
$$

と書く。$\alpha$ が特性方程式の根であるとき、$\widetilde Q$ の $x^{-2}$ の係数は $0$ となる。

<div class="math-box proposition-box" markdown="1">

<div class="math-box-title">命題：解析的な因子の係数を決める漸化式</div>

$u=\sum_{n=0}^{\infty}a_nx^n$ を代入すると、係数比較から得る漸化式は

$$
(n+2)(\widetilde p_{-1}+n+1)a_{n+2}
+\sum_{k=0}^{n+1}
\left(k\widetilde p_{n+1-k}+\widetilde q_{n-k}\right)a_k=0,
\qquad n\geq-1.
$$

また、$x^{-1}$ の係数について

$$
\widetilde p_{-1}=2\alpha+p_{-1}
=1+\alpha-\beta
$$

が成り立つ。ノートでは、この係数と特性指数の差を結び付けて、級数の係数が決まる条件を検討している。

</div>

## 指数の差による場合分け

原点の近傍で $x^\alpha$ と $\log x$ の枝を固定する。以下の解の形は、原ノートの整数差の場合の記述を NIST DLMF §2.7(i), equations (2.7.4)–(2.7.6) と照合して修正したものである。


<div class="math-box theorem-box" markdown="1">

<div class="math-box-title">定理：指数差が整数でない場合（Nonresonant Case）</div>

$\alpha-\beta\notin\mathbb Z$ のとき、独立な2つの解を

$$
y_1=x^\alpha u(x),\qquad y_2=x^\beta v(x)
$$

と書ける。$u,v$ は原点で解析的で、$u(0)=v(0)=1$ と正規化できる。

</div>

<div class="math-box theorem-box" markdown="1">

<div class="math-box-title">定理：指数差が整数の場合（Resonant Case）</div>

$\beta-\alpha=m\in\mathbb Z_{\geq0}$ とする。指数 $\beta$ に対応する解を

$$
y_1=x^\beta v(x),\qquad v(0)=1
$$

と書ける。もう1つの独立な解には、一般に対数項を含む形

$$
y_2=x^\alpha u(x)+C y_1\log x
$$

が必要となる。$u,v$ は原点で解析的で、$C$ は定数である。$m>0$ の場合は $C=0$ となることもあるが、常に対数項を除けるとは限らない。重根の場合 $m=0$ は、第2解に対数項が必要である。

</div>

## 小さい指数で係数決定が止まり得る理由

<div class="math-box lemma-box" markdown="1">

<div class="math-box-title">補題：共鳴する次数の係数</div>

指数 $\alpha$ に対する漸化式の $a_{n+2}$ の係数は

$$
(n+2)(n+2+\alpha-\beta).
$$

$k=n+2$ と置けば $k(k-m)$ であり、$m>0$ のとき $k=m$ で $0$ となる。一方、指数 $\beta$ の側では $k(k+m)$ となり、$k\geq1$ で $0$ にならない。

</div>

したがって、原ノートの $\alpha<\beta$ の場合には、非零の先頭係数を持つ級数解が保証される側を $\beta$ とする。小さい指数 $\alpha$ の側は、消える係数に対応する条件と対数項を確認する必要がある。

## 続けて読む

[← 特性方程式と特性指数の導出](/articles/hypergeometric-indicial-equation.html)

[無限遠点の確定特異点と変数変換 →](/articles/hypergeometric-singularity-at-infinity.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)

出典ノート：『超幾何方程式.pdf』2〜3ページ。
