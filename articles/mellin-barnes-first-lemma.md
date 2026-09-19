---
layout: article
title: "Mellin–Barnes積分とBarnesの第一補題"
category: "gamma-function"
category_label: "ガンマ関数"
---

Mellin–Barnes積分では、複数のガンマ関数を含む積分を複素平面上の縦の積分路で考える。積分路を左右に移動させることで留数の和へ変換でき、特殊関数の評価に利用できる。

## 1. 基本となる積分

次の積分を考える。

$$
I
=
\frac{1}{2\pi i}
\int_L
\Gamma(a+s)
\Gamma(b+s)
\Gamma(c-s)
\Gamma(d-s)
\,ds.
$$

$\Gamma(a+s)$ と $\Gamma(b+s)$ の極は左側に、$\Gamma(c-s)$ と $\Gamma(d-s)$ の極は右側にくるように積分路 $L$ をとる。

## 2. 極の位置

$\Gamma(a+s)$ の極は、

$$
s=-a-n,
\qquad
n=0,1,2,\ldots
$$

にある。

同様に、

$$
\Gamma(b+s)
$$

の極は $s=-b-n$ にあり、

$$
\Gamma(c-s),
\qquad
\Gamma(d-s)
$$

の極はそれぞれ $s=c+n$、$s=d+n$ にある。

したがって、積分路 $L$ は左側の2系列の極と右側の2系列の極を分離するように選ぶ。

## 3. スターリングの公式による評価

積分路を閉じるためには、大きな半円上で積分が消えることを確認する必要がある。ここでガンマ関数にスターリングの公式を適用すると、積分関数が十分速く減衰する条件を調べることができる。

## 4. Barnesの第一補題

<div class="math-box theorem-box">

<div class="math-box-title">Barnesの第一補題</div>

積分路 $L$ が極を上のように分離し、積分が収束する条件のもとで、

$$
\frac{1}{2\pi i}
\int_L
\Gamma(a+s)
\Gamma(b+s)
\Gamma(c-s)
\Gamma(d-s)
\,ds
=
\frac{
\Gamma(a+c)
\Gamma(b+c)
\Gamma(a+d)
\Gamma(b+d)
}{
\Gamma(a+b+c+d)
}.
$$

</div>

## 5. 留数による計算

左側へ積分路を閉じると、

$$
s=-a-n
$$

および、

$$
s=-b-n
$$

における留数の和が現れる。各留数にはガンマ関数の反射公式とベータ関数が用いられ、得られた2つの級数を整理すると右辺のガンマ関数の積へまとまる。

Mellin–Barnes積分では、ガンマ関数の極の配置、反射公式、スターリングの公式が同時に重要になる。

## 次の記事

[Mellin変換による代数方程式の解の表示](/articles/mellin-algebraic-equation.html)
