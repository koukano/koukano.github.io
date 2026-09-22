---
layout: article
title: "オイラーの反射公式"
seo_title: "オイラーの反射公式｜Γ(z)Γ(1-z)=π/sinπz の証明"
description: "ガンマ関数のオイラーの反射公式 Γ(z)Γ(1-z)=π/sin(πz) を、成立条件とともに証明します。"
category: "gamma-function"
category_label: "ガンマ関数"
---

ガンマ関数の $z$ と $1-z$ における値は、正弦関数を通して結びついている。

<div class="math-box theorem-box">

<div class="math-box-title">定理：オイラーの反射公式</div>

$z\notin\mathbb{Z}$ に対して、

$$
\Gamma(z)\Gamma(1-z)
=
\frac{\pi}{\sin\pi z}
$$

が成り立つ。

</div>

## 証明

ワイエルシュトラスの積表示から、

$$
\frac1{\Gamma(z)}
=
ze^{\gamma z}
\prod_{n=1}^{\infty}
\left(1+\frac{z}{n}\right)e^{-z/n}
$$

である。

$z$ を $-z$ に置き換えると、

$$
\frac1{\Gamma(-z)}
=
-z e^{-\gamma z}
\prod_{n=1}^{\infty}
\left(1-\frac{z}{n}\right)e^{z/n}.
$$

両式を掛けると指数因子が消え、

$$
\frac1{\Gamma(z)\Gamma(-z)}
=
-z^2
\prod_{n=1}^{\infty}
\left(1-\frac{z^2}{n^2}\right).
$$

一方、関数方程式

$$
\Gamma(1-z)
=
-z\Gamma(-z)
$$

より、

$$
\frac1{\Gamma(z)\Gamma(1-z)}
=
z
\prod_{n=1}^{\infty}
\left(1-\frac{z^2}{n^2}\right).
$$

ここで正弦関数のオイラー積

$$
\frac{\sin\pi z}{\pi}
=
z
\prod_{n=1}^{\infty}
\left(1-\frac{z^2}{n^2}\right)
$$

を用いると、

$$
\frac1{\Gamma(z)\Gamma(1-z)}
=
\frac{\sin\pi z}{\pi}.
$$

両辺の逆数をとれば、

$$
\Gamma(z)\Gamma(1-z)
=
\frac{\pi}{\sin\pi z}
$$

を得る。
<div class="proof-end">\(\square\)</div>

## 系

$z=\tfrac12$ とすると、

$$
\Gamma\left(\frac12\right)^2
=
\pi.
$$

$\Gamma(1/2)>0$ なので、

$$
\Gamma\left(\frac12\right)
=
\sqrt{\pi}.
$$

## 次の記事

[ガンマ関数のハンケル型積分表示](/articles/gamma-hankel-integral.html)
