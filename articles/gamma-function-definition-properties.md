---
layout: article
title: "ガンマ関数の定義と基本的性質"
category: "gamma-function"
category_label: "ガンマ関数"
---

ガンマ関数は階乗を複素数へ拡張する特殊関数である。本記事では、オイラー積分、ガウスの極限表示、ワイエルシュトラス積表示を確認し、関数方程式、極、留数を整理する。

## 1. オイラー積分による定義

<div class="math-box definition-box">

<div class="math-box-title">定義：ガンマ関数</div>

$\operatorname{Re}z>0$ に対して、

$$
\Gamma(z)
=
\int_0^\infty e^{-t}t^{z-1}\,dt
$$

と定める。

</div>

この積分は $t=0$ と $t=\infty$ の両方で収束を考える必要がある。$t=\infty$ では指数関数 $e^{-t}$ が多項式的な増大より速く減衰し、$t=0$ では $t^{z-1}$ の積分可能性から $\operatorname{Re}z>0$ が必要になる。

## 2. ガウスの極限表示

<div class="math-box theorem-box">

<div class="math-box-title">ガウスの表示</div>

$$
\Gamma(z)
=
\lim_{n\to\infty}
\frac{n!\,n^z}
{z(z+1)\cdots(z+n)}
$$

が成り立つ。ただし、

$$
z\neq0,-1,-2,\ldots
$$

とする。

</div>

この表示では、オイラー積分の定義域である右半平面を越えてガンマ関数を考えることができる。分母に現れる

$$
z,\ z+1,\ z+2,\ldots
$$

から、非正整数が特別な点になることも分かる。

## 3. ワイエルシュトラスの積表示

オイラー・マスケローニ定数を

$$
\gamma
=
\lim_{n\to\infty}
\left(
\sum_{k=1}^{n}\frac1k-\log n
\right)
$$

とする。

<div class="math-box theorem-box">

<div class="math-box-title">ワイエルシュトラスの積表示</div>

$$
\frac{1}{\Gamma(z)}
=
ze^{\gamma z}
\prod_{n=1}^{\infty}
\left(
1+\frac{z}{n}
\right)e^{-z/n}.
$$

</div>

この積は、各因子の $1/n$ 次の項を指数因子によって打ち消すことで収束する形になっている。

## 4. 関数方程式

オイラー積分に部分積分を適用すると、

$$
\Gamma(z+1)
=
z\Gamma(z)
$$

を得る。

<div class="math-box theorem-box">

<div class="math-box-title">ガンマ関数の関数方程式</div>

$$
\Gamma(z+1)=z\Gamma(z).
$$

</div>

特に、

$$
\Gamma(1)=1
$$

であるから、正整数 $n$ に対して、

$$
\Gamma(n+1)=n!
$$

となる。これが、ガンマ関数が階乗の拡張と呼ばれる理由である。

## 5. 解析接続

関数方程式を変形すると、

$$
\Gamma(z)
=
\frac{\Gamma(z+1)}{z}
$$

となる。右辺は $\operatorname{Re}z>-1$ まで意味を持つため、これによってガンマ関数を左側へ解析接続できる。同じ操作を繰り返すことで、非正整数を除く複素平面全体へ拡張できる。

## 6. 極と留数

ガンマ関数は、

$$
z=0,-1,-2,\ldots
$$

に1位の極を持つ。

$z=-n$ における留数は、

$$
\operatorname*{Res}_{z=-n}\Gamma(z)
=
\lim_{z\to-n}(z+n)\Gamma(z)
=
\frac{(-1)^n}{n!}
$$

である。

<div class="math-box theorem-box">

<div class="math-box-title">ガンマ関数の極と留数</div>

ガンマ関数 $\Gamma(z)$ は非正整数に単純極を持ち、

$$
\operatorname*{Res}_{z=-n}\Gamma(z)
=
\frac{(-1)^n}{n!}
\qquad
(n=0,1,2,\ldots)
$$

が成り立つ。

</div>

## 次の記事

[オイラーの反射公式とハンケルの積分表示](/articles/gamma-reflection-hankel.html)
