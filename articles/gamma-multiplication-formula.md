---
layout: article
title: "ガウスの乗法公式"
seo_title: "ガウスの乗法公式｜ガンマ関数の積公式と証明"
description: "ガンマ関数のガウスの乗法公式を示し、正整数 m に対する積表示とルジャンドルの倍角公式との関係を整理します。"
category: "gamma-function"
category_label: "ガンマ関数"
---

<div class="math-box theorem-box">

<div class="math-box-title">定理：ガウスの乗法公式</div>

正整数 $m$ に対して、

$$
\prod_{k=0}^{m-1}
\Gamma\left(z+\frac{k}{m}\right)
=
(2\pi)^{\frac{m-1}{2}}
m^{\frac12-mz}
\Gamma(mz)
$$

が成り立つ。

</div>

## 証明

$$
F(z)
=
m^{mz}
\frac{
\displaystyle\prod_{k=0}^{m-1}
\Gamma\left(z+\frac{k}{m}\right)
}{
\Gamma(mz)
}
$$

とおく。

$z$ を $z+1/m$ に置き換えると、分子では因子が一つずつずれ、

$$
\prod_{k=0}^{m-1}
\Gamma\left(z+\frac1m+\frac{k}{m}\right)
=
\frac{\Gamma(z+1)}{\Gamma(z)}
\prod_{k=0}^{m-1}
\Gamma\left(z+\frac{k}{m}\right)
=
z
\prod_{k=0}^{m-1}
\Gamma\left(z+\frac{k}{m}\right).
$$

一方、

$$
\Gamma(mz+1)=mz\Gamma(mz).
$$

したがって、

$$
F\left(z+\frac1m\right)=F(z).
$$

つまり $F$ は周期 $1/m$ を持つ。

そこで $z$ を正の実軸上で大きくし、各ガンマ関数にスターリングの公式を適用する。整理すると、

$$
F(z)
\longrightarrow
(2\pi)^{\frac{m-1}{2}}m^{1/2}.
$$

周期性より、任意の固定した $z$ に対して $z+n/m$ とずらしても $F$ の値は変わらないため、

$$
F(z)
=
(2\pi)^{\frac{m-1}{2}}m^{1/2}.
$$

よって、

$$
\prod_{k=0}^{m-1}
\Gamma\left(z+\frac{k}{m}\right)
=
(2\pi)^{\frac{m-1}{2}}
m^{\frac12-mz}
\Gamma(mz).
$$

$\square$

## 次の記事

[ルジャンドルの倍角公式](/articles/legendre-duplication-formula.html)
