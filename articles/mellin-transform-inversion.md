---
layout: article
title: "Mellin変換（Mellin Transform）とMellin反転公式（Mellin Inversion Formula）"
seo_title: "Mellin変換とは？定義とMellin反転公式"
description: "Mellin変換の定義とMellin反転公式を、ガンマ関数やMellin–Barnes積分とのつながりを含めて整理します。"
category: "gamma-function"
category_label: "ガンマ関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
  - 'NIST, <a href="https://dlmf.nist.gov/2.5#i">Digital Library of Mathematical Functions: Mellin Transform Methods</a>.'
---

Mellin変換は、正の実軸上の関数を複素変数の関数へ移す積分変換である。ガンマ関数そのものもMellin変換として現れ、Mellin–Barnes積分を考えるための基礎になる。

## 1. Mellin変換（Mellin Transform）

<div class="math-box definition-box">

<div class="math-box-title">定義：Mellin変換（Mellin Transform）</div>

関数 $f(x)$ に対して、

$$
F(z)
=
\int_0^\infty
f(x)x^{z-1}\,dx
$$

を $f$ のMellin変換という。

</div>

積分が収束する $z$ の範囲は関数 $f$ によって異なり、通常は複素平面上の縦の帯状領域になる。

## 2. Mellin反転公式（Mellin Inversion Formula）

<div class="math-box theorem-box">

<div class="math-box-title">Mellin反転公式（Mellin Inversion Formula）</div>

例えば、ある実数 $c$ に対して

$$
\int_0^\infty |f(x)|x^{c-1}\,dx<\infty,
\qquad
\int_{-\infty}^{\infty}|F(c+it)|\,dt<\infty
$$

が成り立つとする。このとき、$f$ の連続点 $x>0$ で、

$$
f(x)
=
\frac{1}{2\pi i}
\int_{c-i\infty}^{c+i\infty}
F(z)x^{-z}\,dz
$$

が成り立つ。積分路は $\operatorname{Re}z=c$ という縦線を下から上へ進む。これは十分条件の一例であり、単にMellin変換の積分が存在することだけで反転公式が常に成り立つわけではない。

</div>

## 3. フーリエ変換との関係

Mellin反転公式は、変数変換

$$
x=e^u
$$

を行うことでフーリエ反転公式へ帰着できる。

実際、

$$
F(z)
=
\int_0^\infty
f(x)x^{z-1}\,dx
$$

で $x=e^u$ とすると、

$$
F(z)
=
\int_{-\infty}^{\infty}
f(e^u)e^{zu}\,du.
$$

さらに、

$$
z=\sigma-it
$$

とおけば、

$$
F(\sigma-it)
=
\int_{-\infty}^{\infty}
\left[
f(e^u)e^{\sigma u}
\right]
e^{-itu}\,du.
$$

これは

$$
f(e^u)e^{\sigma u}
$$

のフーリエ変換になっている。上の十分条件では $g(u)=f(e^u)e^{cu}$ とそのフーリエ変換がともに $L^1(\mathbb R)$ に属する。したがって連続点でフーリエ反転公式を適用し、$x=e^u$ へ戻すとMellin反転公式が得られる。

## 4. ガンマ関数との関係

$\operatorname{Re}z>0$ におけるオイラー積分

$$
\Gamma(z)
=
\int_0^\infty
e^{-x}x^{z-1}\,dx
$$

は、

$$
f(x)=e^{-x}
$$

のMellin変換そのものである。

## 具体例：指数関数の尺度を変える

$f(x)=e^{-2x}$ とする。$u=2x$ と置換すると、$\operatorname{Re}z>0$ で

$$
F(z)=\int_0^\infty e^{-2x}x^{z-1}\,dx
=2^{-z}\int_0^\infty e^{-u}u^{z-1}\,du
=2^{-z}\Gamma(z).
$$

例えば $F(1)=1/2$、$F(2)=1/4$ である。任意の $c>0$ では縦線上のガンマ関数の指数的減衰により反転の十分条件も満たされ、

$$
e^{-2x}=\frac1{2\pi i}\int_{c-i\infty}^{c+i\infty}\Gamma(z)(2x)^{-z}\,dz
\qquad(x>0)
$$

となる。元の変数の拡大・縮小が、変換後には因子 $2^{-z}$ として現れる。

## 次の記事

[Mellin–Barnes積分とBarnesの第一補題](/articles/mellin-barnes-first-lemma.html)
