---
layout: article
title: "ワイエルシュトラスの近似定理とベルンシュタイン多項式"
category: "special-functions"
category_label: "特殊関数"
---

直交多項式の近似理論を考える準備として、ワイエルシュトラスの近似定理を扱う。証明にはベルンシュタイン多項式を用いる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ワイエルシュトラスの近似定理</div>

$f$ を閉区間 $[a,b]$ 上の連続関数とする。任意の $\varepsilon>0$ に対して、ある多項式 $p$ が存在し、

$$
\lvert f(x)-p(x)\rvert<\varepsilon
$$

がすべての $x\in[a,b]$ で成り立つ。

</div>

区間を一次変換することで、$[0,1]$ の場合を考えれば十分である。

## 1. ベルンシュタイン多項式

$f\in C[0,1]$ に対して、

$$
B_n(x;f)
=
\sum_{k=0}^{n}
\binom{n}{k}
f\left(\frac{k}{n}\right)
x^k(1-x)^{n-k}
$$

をベルンシュタイン多項式という。

まず $f(x)=1,x,x^2$ に対する計算を行い、その後一般の連続関数へ拡張する。

## 2. 基本的な3つの計算

二項定理から、

$$
1
=
\sum_{k=0}^{n}
\binom{n}{k}
x^k(1-x)^{n-k}
$$

が成り立つので、

$$
B_n(x;1)=1.
$$

同様に、

$$
B_n(x;x)=x
$$

を得る。

さらに、

$$
B_n(x;x^2)
=
x^2+\frac{x(1-x)}{n}
$$

であるため、

$$
\left|
x^2-B_n(x;x^2)
\right|
=
\frac{x(1-x)}{n}
\leq
\frac{1}{4n}.
$$

したがって、$1,x,x^2$ については $n\to\infty$ でベルンシュタイン多項式が元の関数へ一様収束する。

## 3. 一様連続性を使う

$f$ は $[0,1]$ 上連続なので一様連続である。したがって任意の $\varepsilon>0$ に対して、ある $\delta>0$ が存在し、

$$
\left|
x-\frac{k}{n}
\right|
<
\delta
$$

ならば、

$$
\left|
f(x)
-
f\left(\frac{k}{n}\right)
\right|
<
\frac{\varepsilon}{2}
$$

となる。

また $f$ は有界なので、

$$
\lvert f(x)\rvert\leq M
$$

となる $M>0$ が存在する。

## 4. 誤差を2つに分ける

ベルンシュタイン多項式との差を、

$$
f(x)-B_n(x;f)
$$

とし、和を

$$
\left|
x-\frac{k}{n}
\right|
<
\delta
$$

の部分と、

$$
\left|
x-\frac{k}{n}
\right|
\geq
\delta
$$

の部分に分ける。

近い部分では一様連続性から誤差は $\varepsilon/2$ 以下に抑えられる。一方、遠い部分では、

$$
1
\leq
\frac{1}{\delta^2}
\left(
x-\frac{k}{n}
\right)^2
$$

を利用し、

$$
\sum_{k=0}^{n}
\binom{n}{k}
\left(
x-\frac{k}{n}
\right)^2
x^k(1-x)^{n-k}
=
\frac{x(1-x)}{n}
$$

を用いることで、

$$
\text{遠い部分の誤差}
\leq
\frac{2M}{4\delta^2n}
$$

と評価できる。

したがって $n$ を十分大きくとれば、

$$
\lvert f(x)-B_n(x;f)\rvert
<
\varepsilon
$$

が $[0,1]$ 上一様に成り立つ。よってワイエルシュトラスの近似定理が得られる。

## 5. 直交多項式との関係

この定理は、連続関数を多項式で近似できることを保証する。この結果は、直交多項式による近似や $L^2$ 空間における完備性の議論へつながる。

## 次の記事

[直交多項式の零点](/articles/zeros-of-orthogonal-polynomials.html)
