---
layout: article
title: "ガンマ関数の極と留数"
seo_title: "ガンマ関数の極と留数｜非正整数の単純極を計算"
description: "ガンマ関数 Γ(z) が 0,-1,-2,… に単純極を持つことと、各極での留数 Res Γ(z)=(-1)^n/n! を導きます。"
category: "gamma-function"
category_label: "ガンマ関数"
---

関数方程式を繰り返し使うと、ガンマ関数を左半平面へ解析接続できる。その際、非正整数に単純極が現れる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ガンマ関数の極と留数</div>

ガンマ関数 $\Gamma(z)$ は

$$
z=0,-1,-2,\ldots
$$

に単純極を持つ。また $n=0,1,2,\ldots$ に対して、

$$
\operatorname*{Res}_{z=-n}\Gamma(z)
=
\frac{(-1)^n}{n!}
$$

が成り立つ。

</div>

## 証明

関数方程式を繰り返すと、

$$
\Gamma(z)
=
\frac{
\Gamma(z+n+1)
}{
z(z+1)\cdots(z+n)
}
$$

となる。

$z=-n$ の近くでは $z+n$ だけが $0$ になり、他の因子

$$
z,z+1,\ldots,z+n-1
$$

は $0$ にならない。

したがって、

$$
\operatorname*{Res}_{z=-n}\Gamma(z)
=
\lim_{z\to-n}
(z+n)\Gamma(z).
$$

上の表示を代入すると、

$$
\operatorname*{Res}_{z=-n}\Gamma(z)
=
\lim_{z\to-n}
\frac{
\Gamma(z+n+1)
}{
z(z+1)\cdots(z+n-1)
}.
$$

分子は

$$
\Gamma(1)=1
$$

に収束する。

分母は

$$
(-n)(-n+1)\cdots(-1)
=
(-1)^n n!
$$

に収束するので、

$$
\operatorname*{Res}_{z=-n}\Gamma(z)
=
\frac1{(-1)^n n!}
=
\frac{(-1)^n}{n!}.
$$

さらに分母には $z+n$ が1次で現れ、分子は $z=-n$ で正則かつ $0$ でない。したがって $z=-n$ は単純極である。$\square$

## 次の記事

[オイラーの反射公式](/articles/gamma-reflection-hankel.html)
