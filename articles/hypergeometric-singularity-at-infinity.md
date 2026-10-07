---
layout: article
title: "無限遠点の確定特異点と変数変換"
seo_title: "無限遠点の確定特異点と変数変換｜超幾何関数"
description: "x=1/t の変換により無限遠点を原点へ移し、変換後の方程式と係数の正則性を確認します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
---

2階方程式 $y''+P(x)y'+Q(x)y=0$ で $x=1/t$ と変換し、$Y(t)=y(1/t)$ と書く。ノートの変換後の方程式は

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

が正則であることである。ノートでは、これを $P(x)$ が無限遠で少なくとも1位、$Q(x)$ が少なくとも2位の零点を持つという形でも述べている。

</div>

## 続けて読む

[← フロベニウス法：漸化式・整数差・対数解](/articles/hypergeometric-frobenius-solutions.html)

[3つの確定特異点とフックスの関係式 →](/articles/hypergeometric-three-singularities.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)

出典ノート：『超幾何方程式.pdf』3ページ。
