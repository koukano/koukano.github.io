---
layout: article
title: "ガンマ関数と一般化二項定理"
category: "gamma-function"
category_label: "ガンマ関数"
---

二項定理は、指数が整数でない場合にも無限級数として拡張できる。その係数はガンマ関数を用いて表すことができる。

## 1. 一般化二項定理

<div class="math-box theorem-box">

<div class="math-box-title">一般化二項定理</div>

$\lvert x\rvert<1$ とする。任意の複素数 $\alpha$ に対して、

$$
(1+x)^\alpha
=
\sum_{n=0}^{\infty}
\binom{\alpha}{n}x^n
$$

が成り立つ。

</div>

ここで、

$$
\binom{\alpha}{n}
=
\frac{
\alpha(\alpha-1)\cdots(\alpha-n+1)
}{
n!
}.
$$

## 2. 負の指数の場合

$\alpha=-p$ とすると、

$$
(1-t)^{-p}
=
\sum_{n=0}^{\infty}
(-1)^n
\binom{-p}{n}
t^n.
$$

係数について、

$$
(-1)^n
\binom{-p}{n}
=
\frac{
p(p+1)\cdots(p+n-1)
}{
n!
}
$$

である。

ガンマ関数の関数方程式から、

$$
p(p+1)\cdots(p+n-1)
=
\frac{\Gamma(n+p)}
{\Gamma(p)}
$$

なので、

<div class="math-box theorem-box">

<div class="math-box-title">ガンマ関数による二項係数</div>

$$
(-1)^n
\binom{-p}{n}
=
\frac{\Gamma(n+p)}
{n!\,\Gamma(p)}.
$$

</div>

したがって、

$$
(1-t)^{-p}
=
\sum_{n=0}^{\infty}
\frac{\Gamma(n+p)}
{n!\,\Gamma(p)}
t^n.
$$

この表示は、ベータ関数やMellin–Barnes積分で現れる級数を整理するときに用いられる。

## 次の記事

[Mellin変換とMellin反転公式](/articles/mellin-transform-inversion.html)
