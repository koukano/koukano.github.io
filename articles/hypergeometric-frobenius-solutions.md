---
layout: article
title: "確定特異点とフロベニウス法：特性指数・対数解・フックスの関係式"
seo_title: "確定特異点とフロベニウス法：特性指数・対数解・フックスの関係式｜超幾何関数"
description: "確定特異点の定義から特性方程式と級数解を導き、整数差・対数解、無限遠点、フックスの関係式まで解説します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
  - "NIST, <a href=\"https://dlmf.nist.gov/2.7#i\">Digital Library of Mathematical Functions: Regular Singularities: Fuchs–Frobenius Theory</a>."
---

2階線形微分方程式の確定特異点を調べ、特性指数を使って解の形を求めよう。有限点から無限遠点へ、順に考えていく。

## この記事の目次

- [2階線形微分方程式の確定特異点](#regular-singular-points)
- [特性方程式と特性指数の導出](#indicial-equation)
- [フロベニウス法：漸化式・整数差・対数解](#frobenius-solutions)
- [無限遠点の確定特異点と変数変換](#singularity-at-infinity)
- [3つの確定特異点とフックスの関係式](#three-singularities)

<h2 id="regular-singular-points">2階線形微分方程式の確定特異点</h2>

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：確定特異点（Regular Singular Point）</div>

2階線形微分方程式

$$
y''+P(x)y'+Q(x)y=0
$$

に対し、係数の特異点 $x=c$ で $P(x)$ が高々1位の極、$Q(x)$ が高々2位の極を持つとき、$x=c$ を**確定特異点**という。

</div>

有限の確定特異点の近傍では、変数を平行移動して $c=0$ とする。無限遠点を調べる場合は $x=1/t$ と変換する。

<h2 id="indicial-equation">特性方程式と特性指数の導出</h2>

2階方程式 $y''+P(x)y'+Q(x)y=0$ の確定特異点 $x=0$ を考える。その近傍で、係数を

$$
\begin{aligned}
P(x)&=p_{-1}x^{-1}+p_0+p_1x+\cdots,\\
Q(x)&=q_{-2}x^{-2}+q_{-1}x^{-1}+q_0+\cdots
\end{aligned}
$$

と展開し、$y=x^{\alpha}u$ とおく。微分すると、

$$
\begin{aligned}
y'&=x^{\alpha}u'+\alpha x^{\alpha-1}u,\\
y''&=x^{\alpha}u''+2\alpha x^{\alpha-1}u'
+\alpha(\alpha-1)x^{\alpha-2}u.
\end{aligned}
$$

したがって、$u$ に対する方程式は

$$
u''+\left(P(x)+\frac{2\alpha}{x}\right)u'
+\frac{\alpha(\alpha-1)+\alpha xP(x)+x^2Q(x)}{x^2}u=0.
$$

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：特性方程式と特性指数（Indicial Equation and Exponents）</div>

$u$ の係数の $x^{-2}$ の項を消す条件は、

$$
\alpha(\alpha-1)+p_{-1}\alpha+q_{-2}=0.
$$

これを特性方程式とし、その根を**特性指数**という。2つの根を $\alpha,\beta$ と書けば、根と係数の関係から

$$
\alpha+\beta=1-p_{-1}
$$

である。

</div>

<h2 id="frobenius-solutions">フロベニウス法：漸化式・整数差・対数解</h2>

[特性方程式の導出](/articles/hypergeometric-frobenius-solutions.html#indicial-equation)で扱った $y''+P(x)y'+Q(x)y=0$ を考え、特性指数を $\alpha,\beta$ とする。$y=x^\alpha u$ による変換後の係数を

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

が成り立つ。この係数と特性指数の差に注目し、級数の係数が決まる条件を調べよう。

</div>

### 指数の差による場合分け

原点の近傍で $x^\alpha$ と $\log x$ の枝を固定する。

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

### 小さい指数で係数決定が止まり得る理由

<div class="math-box lemma-box" markdown="1">

<div class="math-box-title">補題：共鳴する次数の係数</div>

指数 $\alpha$ に対する漸化式の $a_{n+2}$ の係数は

$$
(n+2)(n+2+\alpha-\beta).
$$

$k=n+2$ と置けば $k(k-m)$ であり、$m>0$ のとき $k=m$ で $0$ となる。一方、指数 $\beta$ の側では $k(k+m)$ となり、$k\geq1$ で $0$ にならない。

</div>

したがって、$\alpha<\beta$ の場合には、非零の先頭係数を持つ級数解が保証される側を $\beta$ とする。小さい指数 $\alpha$ の側は、消える係数に対応する条件と対数項を確認する必要がある。

<h2 id="singularity-at-infinity">無限遠点の確定特異点と変数変換</h2>

2階方程式 $y''+P(x)y'+Q(x)y=0$ で $x=1/t$ と変換し、$Y(t)=y(1/t)$ と書く。変換後の方程式は

$$
Y''+\left(\frac2t-\frac{P(1/t)}{t^2}\right)Y'
+\frac{Q(1/t)}{t^4}Y=0.
$$

<div class="math-box proposition-box" markdown="1">

<div class="math-box-title">命題：無限遠点を原点へ移した判定条件</div>

したがって、$x=\infty$ が確定特異点である条件は、$t=0$ の近傍で

$$
2-\frac{P(1/t)}t,
\qquad
\frac{Q(1/t)}{t^2}
$$

が正則であることである。これは、$P(x)$ が無限遠で少なくとも1位、$Q(x)$ が少なくとも2位の零点を持つという条件でも表せる。

</div>

<h2 id="three-singularities">3つの確定特異点とフックスの関係式</h2>

3つの確定特異点を1次分数変換で $0,1,\infty$ に移す。

2階方程式を

$$
y''+P(x)y'+Q(x)y=0
$$

と書くと、$0,1$ において $P$ は高々1位、$Q$ は高々2位の極を持ち、無限遠では[無限遠点の判定条件](/articles/hypergeometric-frobenius-solutions.html#singularity-at-infinity)を満たす。

<div class="math-box proposition-box" markdown="1">

<div class="math-box-title">命題：0・1・∞を扱う2階方程式の係数</div>

係数の形を、定数の記号を分けて書けば、

$$
P(x)=\frac{ax+b}{x(1-x)},
\qquad
Q(x)=\frac{cx^2+dx+e}{x^2(1-x)^2}.
$$

</div>

<div class="math-box theorem-box" markdown="1">

<div class="math-box-title">定理：フックスの関係式（Fuchs Relation）</div>

上の型の方程式では、$0,1,\infty$ における特性指数の総和が $1$ になる。

</div>

## 続けて読む

[← 級数展開と特異点：べき級数からローラン展開まで](/articles/hypergeometric-power-series.html)

[確定特異点を持つ線形系：固有値・級数解・特異点の変換 →](/articles/hypergeometric-linear-systems.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)
