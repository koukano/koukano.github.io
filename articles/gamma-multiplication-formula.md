---
layout: article
title: "ガンマ関数の乗法公式と倍角公式"
category: "gamma-function"
category_label: "ガンマ関数"
---

ガンマ関数の積には、引数を等間隔にずらした複数のガンマ関数を1つのガンマ関数へまとめる乗法公式がある。本記事ではその公式と、特別な場合である倍角公式を扱う。

## 1. 乗法公式

正整数 $m$ に対して、

<div class="math-box theorem-box">

<div class="math-box-title">ガウスの乗法公式</div>

$$
\Gamma(z)
\Gamma\left(z+\frac1m\right)
\Gamma\left(z+\frac2m\right)
\cdots
\Gamma\left(z+\frac{m-1}{m}\right)
=
(2\pi)^{\frac{m-1}{2}}
m^{\frac12-mz}
\Gamma(mz).
$$

</div>

ガウスの極限表示を各因子に適用し、積をまとめると、左辺と $\Gamma(mz)$ の比が $z$ に依存しない定数因子へ整理される。最後にスターリングの公式を用いて、その定数を決定する。

## 2. 定数因子の決定

積

$$
G(z)
=
\Gamma(z)
\Gamma\left(z+\frac1m\right)
\cdots
\Gamma\left(z+\frac{m-1}{m}\right)
$$

を考える。

ガウス表示を用いると、$G(z)$ と $\Gamma(mz)$ の比は、

$$
G(z)
=
C_m\,
m^{\frac12-mz}
\Gamma(mz)
$$

という形になる。スターリングの公式を比較することで、

$$
C_m
=
(2\pi)^{\frac{m-1}{2}}
$$

を得る。

## 3. 倍角公式

$m=2$ とすると、

<div class="math-box theorem-box">

<div class="math-box-title">ルジャンドルの倍角公式</div>

$$
\Gamma(z)
\Gamma\left(z+\frac12\right)
=
2^{1-2z}
\sqrt{\pi}\,
\Gamma(2z).
$$

</div>

これは乗法公式の最も基本的な場合である。

## 次の記事

[ベータ関数とガンマ関数](/articles/beta-function-gamma.html)
