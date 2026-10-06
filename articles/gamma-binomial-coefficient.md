---
layout: article
title: "ガンマ関数による二項係数の表示（Binomial Coefficients in Terms of the Gamma Function）"
seo_title: "ガンマ関数による二項係数の表示｜公式と証明"
description: "ガンマ関数を用いて一般化された二項係数を表す公式を示し、その成立条件と証明を数式で整理します。"
category: "gamma-function"
category_label: "ガンマ関数"
---

<div class="math-box theorem-box">

<div class="math-box-title">定理：ガンマ関数による二項係数（Binomial Coefficients in Terms of the Gamma Function）</div>

$p\notin\{0,-1,-2,\ldots\}$ とし、$n=0,1,2,\ldots$ とする。このとき、

$$
(-1)^n
\binom{-p}{n}
=
\frac{\Gamma(n+p)}
{n!\,\Gamma(p)}.
$$

</div>

## 証明

二項係数の定義から、

$$
\begin{aligned}
(-1)^n\binom{-p}{n}
&=
(-1)^n
\frac{
(-p)(-p-1)\cdots(-p-n+1)
}{n!}\\
&=
\frac{
p(p+1)\cdots(p+n-1)
}{n!}.
\end{aligned}
$$

ガンマ関数の関数方程式

$$
\Gamma(z+1)=z\Gamma(z)
$$

を $n$ 回用いると、

$$
\Gamma(p+n)
=
p(p+1)\cdots(p+n-1)\Gamma(p).
$$

したがって、

$$
p(p+1)\cdots(p+n-1)
=
\frac{\Gamma(p+n)}{\Gamma(p)}.
$$

これを代入すれば、

$$
(-1)^n
\binom{-p}{n}
=
\frac{\Gamma(n+p)}
{n!\,\Gamma(p)}.
$$


<div class="proof-end">\(\square\)</div>

## 具体例：半整数の係数をガンマ関数で計算する

$p=1/2$、$n=2$ の場合を考える。本文の公式の右辺は

$$
\frac{\Gamma(5/2)}{2!\,\Gamma(1/2)}
=\frac{3\sqrt\pi/4}{2\sqrt\pi}=\frac38.
$$

左辺も $(-1)^2\binom{-1/2}{2}=(-1/2)(-3/2)/2=3/8$ で一致する。この値は $(1+x)^{-1/2}=1-x/2+3x^2/8+\cdots$ の2次の係数に当たる。

## 次の記事

[Mellin変換とMellin反転公式](/articles/mellin-transform-inversion.html)
