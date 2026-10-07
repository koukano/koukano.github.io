---
layout: article
title: "線形系の無限遠点と3つの特異点の変換"
seo_title: "線形系の無限遠点と3つの特異点の変換｜超幾何関数"
description: "線形系のz=1/tによる変換と、0・1・aから0・1・∞への1次分数変換を整理します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
---

<div class="math-box proposition-box" markdown="1">

<div class="math-box-title">命題：線形系の無限遠点の変換</div>

線形系 $dX/dz=A(z)X/z$ で $z=1/t$ と変換すると、

$$
\frac{dX}{dt}=-\frac1t A(1/t)X.
$$

$z=0$ のほかに $z=\infty$ も確定特異点となる場合を調べよう。ここでは、$A$ が定数行列となる形を考える。

</div>

## 3つの有限特異点を移す

さらに、有限の3点 $0,1,a$ を扱う場合には、

$$
\frac{dX}{dz}=\frac{A(z)}{z(z-1)(z-a)}X
$$

と書く。無限遠が確定特異点でない場合には、

$$
A(z)=A_0+A_1z
$$

という1次の形を得ている。また、

$$
z=\frac{at}{t+(a-1)}
$$

という変換を用いて、特異点を $t=0,1,\infty$ に移す。

## 続けて読む

[← 線形系の級数解と係数ベクトルの漸化式](/articles/hypergeometric-matrix-series-solutions.html)

[2成分の線形系から2階微分方程式を導く →](/articles/hypergeometric-system-elimination.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)
