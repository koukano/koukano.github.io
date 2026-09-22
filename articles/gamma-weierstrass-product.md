---
layout: article
title: "ワイエルシュトラスの積表示"
seo_title: "ワイエルシュトラスの積表示｜逆ガンマ関数の無限積"
description: "逆ガンマ関数 1/Γ(z) のワイエルシュトラス積表示を導き、整関数性と非正整数に現れる零点との関係を説明します。"
category: "gamma-function"
category_label: "ガンマ関数"
---

ガウスの極限表示を整理すると、逆ガンマ関数を無限積として表せる。この表示から、$1/\Gamma(z)$ が整関数であることや、その零点が非正整数に現れることが分かる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ワイエルシュトラスの積表示</div>

オイラー・マスケローニ定数を

$$
\gamma
=
\lim_{n\to\infty}
\left(
\sum_{k=1}^{n}\frac1k-\log n
\right)
$$

とする。このとき、

$$
\frac1{\Gamma(z)}
=
ze^{\gamma z}
\prod_{k=1}^{\infty}
\left(1+\frac{z}{k}\right)e^{-z/k}
$$

が成り立つ。

</div>

## 証明

ガウスの極限表示から、

$$
\frac1{\Gamma(z)}
=
\lim_{n\to\infty}
\frac{z(z+1)\cdots(z+n)}
{n!\,n^z}.
$$

分子から $1,2,\ldots,n$ をくくると、

$$
\frac1{\Gamma(z)}
=
z
\lim_{n\to\infty}
n^{-z}
\prod_{k=1}^{n}
\left(1+\frac{z}{k}\right).
$$

調和数

$$
H_n
=
\sum_{k=1}^{n}\frac1k
$$

を用いると、

$$
n^{-z}
=
e^{-z\log n}
=
e^{-zH_n}
e^{z(H_n-\log n)}.
$$

したがって、

$$
\frac1{\Gamma(z)}
=
z
\lim_{n\to\infty}
e^{z(H_n-\log n)}
\prod_{k=1}^{n}
\left(1+\frac{z}{k}\right)e^{-z/k}.
$$

$H_n-\log n\to\gamma$ だから、

$$
e^{z(H_n-\log n)}
\longrightarrow
e^{\gamma z}.
$$

また、

$$
\log\left(1+\frac{z}{k}\right)-\frac{z}{k}
=
O\left(\frac1{k^2}\right)
$$

であり、

$$
\sum_{k=1}^{\infty}\frac1{k^2}
$$

は収束する。そのため、

$$
\prod_{k=1}^{\infty}
\left(1+\frac{z}{k}\right)e^{-z/k}
$$

はコンパクト集合上一様に収束する。

以上より、

$$
\frac1{\Gamma(z)}
=
ze^{\gamma z}
\prod_{k=1}^{\infty}
\left(1+\frac{z}{k}\right)e^{-z/k}
$$

を得る。
<div class="proof-end">\(\square\)</div>

## 次の記事

[ガンマ関数の関数方程式](/articles/gamma-functional-equation.html)
