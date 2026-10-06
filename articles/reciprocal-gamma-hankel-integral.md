---
layout: article
title: "逆ガンマ関数のハンケル積分表示（Hankel Integral Representation of the Reciprocal Gamma Function）"
seo_title: "逆ガンマ関数のハンケル積分表示｜1/Γ(z) の公式"
description: "逆ガンマ関数 1/Γ(z) のハンケル積分表示を、積分路と分枝の取り方を含めて数式で整理します。"
category: "gamma-function"
category_label: "ガンマ関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
  - 'NIST, <a href="https://dlmf.nist.gov/5.9#E2">Digital Library of Mathematical Functions: Gamma Function: Hankel’s Loop Integral</a>.'
---

逆ガンマ関数 $1/\Gamma(z)$ は、ハンケル型積分によって直接表すことができる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：逆ガンマ関数のハンケル表示（Hankel Representation of the Reciprocal Gamma Function）</div>

ハンケル型積分路 $H$ は、正の実軸の下側から原点へ進み、原点を時計回りに回って上側から $+\infty$ へ戻る向きにとる。$(-s)^{-z}$ は $-\pi<\arg(-s)<\pi$ の分枝を用いる。原点を回る円の半径を正の値に固定すれば、すべての $z\in\mathbb C$ に対して、

$$
\frac1{\Gamma(z)}
=
\frac1{2\pi i}
\int_H
e^{-s}(-s)^{-z}\,ds
$$

が成り立つ。

</div>

## 証明

まず $0<\operatorname{Re}z<1$ で示す。この範囲では原点の小円の半径を $0$ に近づけてもその寄与が消える。前の記事のハンケル型積分表示で $z$ を $1-z$ に置き換えると、

$$
\Gamma(1-z)
=
\frac{1}{2i\sin\pi(1-z)}
\int_H
e^{-s}(-s)^{-z}\,ds.
$$

ここで、

$$
\sin\pi(1-z)=\sin\pi z
$$

だから、

$$
\int_H
e^{-s}(-s)^{-z}\,ds
=
2i\sin\pi z\,\Gamma(1-z).
$$

オイラーの反射公式

$$
\Gamma(z)\Gamma(1-z)
=
\frac{\pi}{\sin\pi z}
$$

を用いると、

$$
\sin\pi z\,\Gamma(1-z)
=
\frac{\pi}{\Gamma(z)}.
$$

したがって、

$$
\int_H
e^{-s}(-s)^{-z}\,ds
=
\frac{2\pi i}{\Gamma(z)}.
$$

両辺を $2\pi i$ で割れば、

$$
\frac1{\Gamma(z)}
=
\frac1{2\pi i}
\int_H
e^{-s}(-s)^{-z}\,ds
$$

を得る。

一般の $z$ に対しては、小円の半径を正の値に固定する。積分路の変形によりその半径を変えても積分値は変わらず、無限遠では $e^{-s}$ が減衰するため、この積分は $z$ の整関数を定める。逆ガンマ関数も整関数なので、一致の定理によって上の等式は複素平面全体へ拡張される。各実軸部分を別々に積分してから小円の半径を $0$ にする操作は、$\operatorname{Re}z\geq1$ ではそのまま行えない。
<div class="proof-end">\(\square\)</div>

## 具体例：z = 1 では留数で計算できる

$z=1$ のとき、被積分関数は $-e^{-s}/s$ となり、分枝の違いがなくなる。正の実軸の上下の積分は逆向きなので相殺し、原点を時計回りに回る円の積分が残る。その留数は $-1$ であるから、

$$
\int_H\frac{-e^{-s}}{s}\,ds=(-2\pi i)(-1)=2\pi i,
\qquad
\frac1{2\pi i}\int_H\frac{-e^{-s}}{s}\,ds=1.
$$

これは $1/\Gamma(1)=1$ と一致する。この場合、小円の寄与は $0$ にならず、むしろ答え全体を与える。

## 次の記事

[ワトソンの補題](/articles/gamma-stirling-watson.html)
