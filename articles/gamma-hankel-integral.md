---
layout: article
title: "ガンマ関数のハンケル型積分表示"
seo_title: "ガンマ関数のハンケル積分表示｜積分路・分枝・公式"
description: "ガンマ関数のハンケル型積分表示を、分岐切断、積分路の向き、成立条件とともに複素積分で解説します。"
category: "gamma-function"
category_label: "ガンマ関数"
---

ガンマ関数は、分岐をもつ複素積分を使って表すことができる。

このページでは、正の実軸を分岐切断とし、正の実軸の下側から原点へ進み、原点を回って上側から $+\infty$ へ戻るハンケル型積分路 $H$ を用いる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ガンマ関数のハンケル型積分表示</div>

まず $0<\operatorname{Re}z<1$ とする。上の積分路と分枝を用いると、

$$
\Gamma(z)
=
\frac{1}{2i\sin\pi z}
\int_H
e^{-s}(-s)^{z-1}\,ds
$$

が成り立つ。右辺はその後解析接続によって拡張できる。

</div>

## 証明

積分路の下側では $s=x-i0$ と書ける。このとき

$$
\arg(-s)=\pi
$$

なので、

$$
(-s)^{z-1}
=
x^{z-1}e^{i\pi(z-1)}.
$$

下側は $x=+\infty$ から $x=0$ へ向かうから、その寄与は

$$
-
e^{i\pi(z-1)}
\int_0^\infty
e^{-x}x^{z-1}\,dx.
$$

上側では

$$
\arg(-s)=-\pi
$$

なので、

$$
(-s)^{z-1}
=
x^{z-1}e^{-i\pi(z-1)}.
$$

上側は $0$ から $+\infty$ へ向かうため、その寄与は

$$
e^{-i\pi(z-1)}
\int_0^\infty
e^{-x}x^{z-1}\,dx.
$$

$0<\operatorname{Re}z<1$ では原点を回る小円の寄与は半径を $0$ にすると消える。したがって、

$$
\begin{aligned}
\int_H e^{-s}(-s)^{z-1}\,ds
&=
\left[
e^{-i\pi(z-1)}
-
e^{i\pi(z-1)}
\right]
\Gamma(z)\\
&=
2i\sin(\pi z)\Gamma(z).
\end{aligned}
$$

よって、

$$
\Gamma(z)
=
\frac{1}{2i\sin\pi z}
\int_H
e^{-s}(-s)^{z-1}\,ds.
$$

これで示された。$\square$

## 次の記事

[逆ガンマ関数のハンケル積分表示](/articles/reciprocal-gamma-hankel-integral.html)
