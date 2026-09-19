---
layout: article
title: "ワトソンの補題"
category: "gamma-function"
category_label: "ガンマ関数"
---

ラプラス型積分では、パラメータが大きくなると積分の主要な寄与が端点の近くから現れる。ワトソンの補題は、この事実を漸近展開として定式化する。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ワトソンの補題</div>

$\lambda>0$ とし、$t\to0^+$ のとき

$$
f(t)
\sim
\sum_{n=0}^{\infty}
a_n t^{n+\lambda-1}
$$

とする。また、ラプラス積分

$$
I(x)
=
\int_0^\infty e^{-xt}f(t)\,dt
$$

が十分大きな $x>0$ に対して収束するとする。

このとき $x\to+\infty$ で、

$$
I(x)
\sim
\sum_{n=0}^{\infty}
a_n
\Gamma(n+\lambda)
x^{-(n+\lambda)}
$$

が成り立つ。

</div>

## 証明

任意の $N\geq0$ に対して、$t\to0^+$ で

$$
f(t)
=
\sum_{n=0}^{N}
a_n t^{n+\lambda-1}
+
R_N(t),
$$

かつ

$$
R_N(t)
=
o\left(t^{N+\lambda-1}\right)
$$

と書ける。

積分を小さな $\delta>0$ を用いて

$$
I(x)
=
\int_0^\delta e^{-xt}f(t)\,dt
+
\int_\delta^\infty e^{-xt}f(t)\,dt
$$

と分ける。

後半は $e^{-x\delta}$ を含むため、$x\to\infty$ で任意のべき $x^{-M}$ より速く減衰する。

前半に有限項の展開を代入すると、

$$
\int_0^\delta e^{-xt}f(t)\,dt
=
\sum_{n=0}^{N}
a_n
\int_0^\delta
e^{-xt}t^{n+\lambda-1}\,dt
+
\int_0^\delta e^{-xt}R_N(t)\,dt.
$$

各主項で $u=xt$ と置けば、

$$
\int_0^\delta
e^{-xt}t^{n+\lambda-1}\,dt
=
x^{-(n+\lambda)}
\int_0^{x\delta}
e^{-u}u^{n+\lambda-1}\,du.
$$

$x\to\infty$ とすると右端の積分は

$$
\Gamma(n+\lambda)
$$

に収束する。

また剰余項は $R_N(t)=o(t^{N+\lambda-1})$ を用いることで、

$$
\int_0^\delta e^{-xt}R_N(t)\,dt
=
o\left(x^{-(N+\lambda)}\right)
$$

と評価できる。

したがって任意の $N$ について、

$$
I(x)
=
\sum_{n=0}^{N}
a_n\Gamma(n+\lambda)x^{-(n+\lambda)}
+
o\left(x^{-(N+\lambda)}\right),
$$

すなわち定理の漸近展開を得る。$\square$

## 次の記事

[スターリングの公式](/articles/gamma-stirling-formula.html)
