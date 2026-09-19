---
layout: article
title: "ルジャンドルの倍角公式"
category: "gamma-function"
category_label: "ガンマ関数"
---

<div class="math-box theorem-box">

<div class="math-box-title">定理：ルジャンドルの倍角公式</div>

$$
\Gamma(z)
\Gamma\left(z+\frac12\right)
=
2^{1-2z}\sqrt{\pi}\,\Gamma(2z).
$$

</div>

## 証明

ガウスの乗法公式

$$
\prod_{k=0}^{m-1}
\Gamma\left(z+\frac{k}{m}\right)
=
(2\pi)^{\frac{m-1}{2}}
m^{\frac12-mz}
\Gamma(mz)
$$

で $m=2$ とおく。

左辺は

$$
\Gamma(z)\Gamma\left(z+\frac12\right)
$$

となり、右辺は

$$
(2\pi)^{1/2}
2^{1/2-2z}
\Gamma(2z).
$$

ここで

$$
(2\pi)^{1/2}2^{1/2-2z}
=
2^{1-2z}\sqrt{\pi}
$$

なので、

$$
\Gamma(z)
\Gamma\left(z+\frac12\right)
=
2^{1-2z}\sqrt{\pi}\,\Gamma(2z).
$$

$\square$
