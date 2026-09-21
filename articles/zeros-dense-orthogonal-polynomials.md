---
layout: article
title: "有限区間における直交多項式の零点の稠密化"
seo_title: "直交多項式の零点の稠密化｜有限区間での分布"
description: "有限な直交区間で次数を大きくすると直交多項式の零点が区間全体に現れることを、部分区間ごとの存在として証明します。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

有限な直交区間では、次数を大きくすると直交多項式の零点は区間全体に現れるようになる。本記事では、その意味を「任意の部分区間に、十分高い次数では少なくとも1つ零点が入る」という形で示す。

<div class="math-box theorem-box">

<div class="math-box-title">定理：有限区間における零点の稠密化</div>

$(a,b)$ を有限区間とし、$(\alpha,\beta)$ をその任意の部分区間とする。このとき、$n$ を十分大きくとれば、正規直交多項式 $\phi_n$ は $(\alpha,\beta)$ に少なくとも1つ零点を持つ。

</div>

## 証明

$(\alpha,\beta)$ の内部で正の部分を持ち、その外側では負になる連続関数を作る。

十分小さい $\varepsilon>0$ に対して、

$$
f(x)
=
\begin{cases}
(x-\alpha)(\beta-x)-\varepsilon,
& x\in(\alpha,\beta),\\[4pt]
-\varepsilon,
& x\notin(\alpha,\beta)
\end{cases}
$$

とおく。

$x=\alpha,\beta$ では両方の式が $-\varepsilon$ になるため、$f$ は連続である。

$\varepsilon$ を十分小さく選べば、$(\alpha,\beta)$ の中央付近では $f$ が正になり、

$$
\int_a^b w(x)f(x)\,dx>0
$$

となるようにできる。

ワイエルシュトラスの近似定理より、たとえば

$$
|f(x)-p(x)|<\frac{\varepsilon}{2}
\qquad
(a\leq x\leq b)
$$

を満たす多項式 $p$ が存在する。

このとき $(\alpha,\beta)$ の外では $f(x)=-\varepsilon$ なので、

$$
p(x)
<
-\frac{\varepsilon}{2}
<0
$$

が成り立つ。

また近似を十分良くとることで、

$$
\int_a^b w(x)p(x)\,dx>0
$$

も成り立つようにできる。

ここで $p$ は固定された多項式なので、$n$ を十分大きくとれば

$$
\deg p\leq 2n-1
$$

となる。

このような $n$ に対し、$\phi_n$ が $(\alpha,\beta)$ に零点を持たないと仮定する。

$\phi_n$ の零点を

$$
x_1,x_2,\ldots,x_n
$$

とすると、すべて

$$
x_k\notin(\alpha,\beta)
$$

である。したがって、

$$
p(x_k)<0
\qquad
(k=1,\ldots,n).
$$

一方、$\phi_n$ の零点を節点とするガウスの求積公式を $p$ に適用すると、

$$
\int_a^b w(x)p(x)\,dx
=
\sum_{k=1}^{n}
\lambda_{k,n}p(x_k)
$$

となる。

クリストッフェル数はすべて正で、

$$
\lambda_{k,n}>0
$$

だから、右辺は

$$
\sum_{k=1}^{n}
\lambda_{k,n}p(x_k)
<0.
$$

しかし左辺は先ほど

$$
\int_a^b w(x)p(x)\,dx>0
$$

となるように選んだ。これは矛盾である。

したがって、十分大きな $n$ に対して $\phi_n$ は $(\alpha,\beta)$ に少なくとも1つ零点を持つ。$\square$

## 注意

この証明ではワイエルシュトラスの一様近似定理を有限区間上で用いている。そのため、直交区間が無限区間の場合には、この結論をそのまま適用することはできない。

## 関連記事

- [異なる次数の直交多項式の零点の分離](/articles/zeros-distribution-orthogonal-polynomials.html)
- [ガウスの求積公式とクリストッフェル数](/articles/gaussian-quadrature.html)
