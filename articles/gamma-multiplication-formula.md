---
layout: article
title: "ガウスの乗法公式（Gauss's Multiplication Formula）"
seo_title: "ガウスの乗法公式｜ガンマ関数の積公式と証明"
description: "ガンマ関数のガウスの乗法公式を示し、正整数 m に対する積表示とルジャンドルの倍角公式との関係を整理します。"
category: "gamma-function"
category_label: "ガンマ関数"
---

<div class="math-box theorem-box">

<div class="math-box-title">定理：ガウスの乗法公式（Gauss's Multiplication Formula）</div>

正整数 $m$ に対して、$mz\notin\lbrace 0,-1,-2,\ldots\rbrace $ のとき、

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

まず実数 $z>0$ を考える。そこで $z$ を正の実軸上で大きくし、各ガンマ関数にスターリングの公式を適用する。整理すると、

$$
F(z)
\longrightarrow
(2\pi)^{\frac{m-1}{2}}m^{1/2}.
$$

周期性より、任意の固定した実数 $z>0$ に対して $z+n/m$ とずらしても $F$ の値は変わらないため、

$$
F(z)
=
(2\pi)^{\frac{m-1}{2}}m^{1/2}.
$$

正の実軸上でこの等式を得たので、一致の定理と有理型関数の解析接続により、両辺が有限なすべての複素数 $z$ でも成立する。よって、

$$
\prod_{k=0}^{m-1}
\Gamma\left(z+\frac{k}{m}\right)
=
(2\pi)^{\frac{m-1}{2}}
m^{\frac12-mz}
\Gamma(mz).
$$


<div class="proof-end">\(\square\)</div>

## 具体例：3個のガンマ関数を1つにまとめる

乗法公式で $m=3$、$z=1/3$ とおくと、

$$
\Gamma\left(\frac13\right)\Gamma\left(\frac23\right)\Gamma(1)
=(2\pi)^{(3-1)/2}3^{1/2-1}\Gamma(1)
=\frac{2\pi}{\sqrt3}.
$$

引数が $1/3$ ずつずれた3つの因子が、引数 $3z=1$ のガンマ関数にまとまった。$\Gamma(1)=1$ を使えば、反射公式で得られる積の値とも一致する。

## 次の記事

[ルジャンドルの倍角公式](/articles/legendre-duplication-formula.html)
