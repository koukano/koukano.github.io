---
layout: article
title: "ルジャンドルの倍角公式（Legendre's Duplication Formula）"
seo_title: "ルジャンドルの倍角公式｜ガンマ関数の公式と証明"
description: "ガンマ関数のルジャンドルの倍角公式 Γ(z)Γ(z+1/2)=2^(1-2z)√πΓ(2z) をガウスの乗法公式から導きます。"
category: "gamma-function"
category_label: "ガンマ関数"
---

<div class="math-box theorem-box">

<div class="math-box-title">定理：ルジャンドルの倍角公式（Legendre's Duplication Formula）</div>

$2z\notin\lbrace 0,-1,-2,\ldots\rbrace $ のとき、

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


<div class="proof-end">\(\square\)</div>

## 具体例：Γ(3/2) を倍角公式で求める

倍角公式に $z=1$ を代入すると、

$$
\Gamma(1)\Gamma\left(\frac32\right)
=2^{-1}\sqrt\pi\,\Gamma(2).
$$

$\Gamma(1)=\Gamma(2)=1$ なので、$\Gamma(3/2)=\sqrt\pi/2$ となる。半整数の値が、整数のガンマ関数と $\sqrt\pi$ を使って計算できる例である。
