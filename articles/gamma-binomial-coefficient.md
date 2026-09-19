---
layout: article
title: "ガンマ関数による二項係数の表示"
category: "gamma-function"
category_label: "ガンマ関数"
---

<div class="math-box theorem-box">

<div class="math-box-title">定理：ガンマ関数による二項係数</div>

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

$\square$

## 次の記事

[Mellin変換とMellin反転公式](/articles/mellin-transform-inversion.html)
