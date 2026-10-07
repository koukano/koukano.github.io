---
layout: article
title: "2階線形微分方程式の確定特異点"
seo_title: "2階線形微分方程式の確定特異点｜超幾何関数"
description: "2階線形微分方程式で、係数の極の位数から確定特異点を判定する定義を整理します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
  - "NIST, <a href=\"https://dlmf.nist.gov/2.7#i\">Digital Library of Mathematical Functions: Regular Singularities: Fuchs–Frobenius Theory</a>."
---

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：確定特異点（Regular Singular Point）</div>

ノートでは、2階線形微分方程式

$$
y''+P(x)y'+Q(x)y=0
$$

に対し、係数の特異点 $x=c$ で $P(x)$ が高々1位の極、$Q(x)$ が高々2位の極を持つとき、$x=c$ を**確定特異点**という。

</div>

有限の確定特異点の近傍では、変数を平行移動して $c=0$ とする。無限遠点を調べる場合は $x=1/t$ と変換する。

判定条件の表現は、参考文献の NIST DLMF §2.7(i) と照合している。

## 続けて読む

[← ローラン展開と特異点：極・留数・真性特異点](/articles/hypergeometric-laurent-singularities.html)

[特性方程式と特性指数の導出 →](/articles/hypergeometric-indicial-equation.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)

出典ノート：『超幾何方程式.pdf』1〜2ページ。
