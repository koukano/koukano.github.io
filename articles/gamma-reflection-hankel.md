---
layout: article
title: "オイラーの反射公式とハンケルの積分表示"
category: "gamma-function"
category_label: "ガンマ関数"
---

ガンマ関数を右半平面から左半平面へ解析接続する際には、反射公式と複素積分表示が重要になる。本記事では、オイラーの反射公式とハンケル型積分表示を扱う。

## 1. オイラーの反射公式

<div class="math-box theorem-box">

<div class="math-box-title">オイラーの反射公式</div>

$$
\Gamma(z)\Gamma(1-z)
=
\frac{\pi}{\sin\pi z},
\qquad
z\neq0,\pm1,\pm2,\ldots
$$

が成り立つ。

</div>

ワイエルシュトラスの積表示から、

$$
\frac{1}
{\Gamma(z)\Gamma(-z)}
=
-z^2
\prod_{k=1}^{\infty}
\left(
1-\frac{z^2}{k^2}
\right)
$$

を得る。さらに、

$$
\Gamma(1-z)
=
-z\Gamma(-z)
$$

を使うことで、

$$
\frac{1}
{\Gamma(z)\Gamma(1-z)}
$$

を無限積として表すことができる。

この無限積を $\sin\pi z$ の無限積と比較すると反射公式が得られる。

## 2. 特別な値

反射公式に

$$
z=\frac12
$$

を代入すると、

$$
\Gamma\left(\frac12\right)^2
=
\pi
$$

である。したがって、

$$
\Gamma\left(\frac12\right)
=
\sqrt{\pi}
$$

を得る。

## 3. 鍵穴型の積分路

複素平面で負の実軸を分岐切断とし、原点を小さく回りながら負の実軸の両側を通る積分路 $C$ を考える。$(-s)^{z-1}$ の偏角が積分路の上下で異なることを利用すると、オイラー積分と複素積分を結びつけることができる。

<div class="math-box theorem-box">

<div class="math-box-title">ハンケル型積分表示</div>

$$
\Gamma(z)
=
-\frac{1}
{2i\sin\pi z}
\int_C
e^{-s}(-s)^{z-1}\,ds
$$

という表示が得られる。

</div>

この式は、積分路が原点のまわりを回ることによって分岐の違いを取り込み、ガンマ関数の解析接続を複素積分として表している。

## 4. 逆ガンマ関数の積分表示

上の表示とオイラーの反射公式を組み合わせると、

<div class="math-box theorem-box">

<div class="math-box-title">逆ガンマ関数のハンケル表示</div>

$$
\frac{1}{\Gamma(z)}
=
\frac{1}{2\pi i}
\int_C
e^{-s}(-s)^{-z}\,ds.
$$

</div>

この積分表示は $1/\Gamma(z)$ を複素積分として表すものであり、ガンマ関数を用いたMellin–Barnes積分にもつながる。

## 次の記事

[ワトソンの補題とスターリングの公式](/articles/gamma-stirling-watson.html)
