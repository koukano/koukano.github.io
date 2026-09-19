---
layout: article
title: "逆ガンマ関数のハンケル積分表示"
category: "gamma-function"
category_label: "ガンマ関数"
---

逆ガンマ関数 $1/\Gamma(z)$ は、ハンケル型積分によって直接表すことができる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：逆ガンマ関数のハンケル表示</div>

ハンケル型積分路 $H$ を前の記事と同じ向きにとると、

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

前の記事のハンケル型積分表示で $z$ を $1-z$ に置き換えると、

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

を得る。$\square$

## 次の記事

[ワトソンの補題](/articles/gamma-stirling-watson.html)
