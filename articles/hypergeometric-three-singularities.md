---
layout: article
title: "3つの確定特異点とフックスの関係式"
seo_title: "3つの確定特異点とフックスの関係式｜超幾何関数"
description: "確定特異点を0・1・∞に配置した方程式の係数と、特性指数の総和に関するフックスの関係式を整理します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
---

ノートでは、3つの確定特異点を1次分数変換で $0,1,\infty$ に移す。

2階方程式を

$$
y''+P(x)y'+Q(x)y=0
$$

と書くと、$0,1$ において $P$ は高々1位、$Q$ は高々2位の極を持ち、無限遠では[無限遠点の判定条件](/articles/hypergeometric-singularity-at-infinity.html)を満たす。

<div class="math-box proposition-box" markdown="1">

<div class="math-box-title">命題：0・1・∞を扱う2階方程式の係数</div>

ノートに記載された係数の形を、定数の記号を分けて書けば、

$$
P(x)=\frac{ax+b}{x(1-x)},
\qquad
Q(x)=\frac{cx^2+dx+e}{x^2(1-x)^2}.
$$

</div>

<div class="math-box theorem-box" markdown="1">

<div class="math-box-title">定理：フックスの関係式（Fuchs Relation）</div>

ノートに記載されたフックスの定理は、上の型の方程式について、$0,1,\infty$ における特性指数の総和が $1$ になるというものである。

</div>

## 続けて読む

[← 無限遠点の確定特異点と変数変換](/articles/hypergeometric-singularity-at-infinity.html)

[確定特異点を持つ線形系と固有値 →](/articles/hypergeometric-linear-systems.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)

出典ノート：『超幾何方程式.pdf』4ページ。
