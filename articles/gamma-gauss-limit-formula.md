---
layout: article
title: "ガウスの極限表示"
seo_title: "ガウスの極限表示とは？ガンマ関数の有限積表示"
description: "ガンマ関数を有限積の極限として表すガウスの極限表示を、成立条件と解析接続へのつながりを含めて解説します。"
category: "gamma-function"
category_label: "ガンマ関数"
---

ガンマ関数は積分だけでなく、有限積の極限としても表せる。この表示は、ガンマ関数の解析接続や無限積表示につながる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ガウスの極限表示</div>

$z\neq0,-1,-2,\ldots$ に対して、

$$
\Gamma(z)
=
\lim_{n\to\infty}
\frac{n!\,n^z}
{z(z+1)\cdots(z+n)}
$$

が成り立つ。

</div>

## 証明

まず $\operatorname{Re}z>0$ とする。

次の積分を考える。

$$
I_n(z)
=
\int_0^1
t^{z-1}(1-t)^n\,dt.
$$

部分積分を繰り返すと、

$$
I_n(z)
=
\frac{n!}
{z(z+1)\cdots(z+n)}.
$$

一方、

$$
t=\frac{u}{n}
$$

と変数変換すると、

$$
n^z I_n(z)
=
\int_0^n
u^{z-1}
\left(1-\frac{u}{n}\right)^n
\,du.
$$

固定した $u\geq0$ に対して、

$$
\left(1-\frac{u}{n}\right)^n
\longrightarrow
e^{-u}
$$

である。

また $0\leq u\leq n$ では

$$
\left(1-\frac{u}{n}\right)^n
\leq
e^{-u}
$$

が成り立つので、$\operatorname{Re}z>0$ のもとで優収束定理を適用できる。

したがって、

$$
\begin{aligned}
\lim_{n\to\infty}
n^z I_n(z)
&=
\int_0^\infty
u^{z-1}e^{-u}\,du\\
&=
\Gamma(z).
\end{aligned}
$$

$I_n(z)$ の表示を代入すると、

$$
\Gamma(z)
=
\lim_{n\to\infty}
\frac{n!\,n^z}
{z(z+1)\cdots(z+n)}
$$

を得る。

右辺は $z=0,-1,-2,\ldots$ を除いて有理関数列の極限として意味を持ち、ガンマ関数の解析接続と一致する。よって定理が得られる。
<div class="proof-end">\(\square\)</div>

## 次の記事

[ワイエルシュトラスの積表示](/articles/gamma-weierstrass-product.html)
