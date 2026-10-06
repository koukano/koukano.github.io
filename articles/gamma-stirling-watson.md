---
layout: article
title: "ワトソンの補題（Watson's Lemma）"
seo_title: "ワトソンの補題とは？ラプラス型積分の漸近展開"
description: "ワトソンの補題を用いて、ラプラス型積分の端点近傍から得られる漸近展開の考え方と成立条件を整理します。"
category: "gamma-function"
category_label: "ガンマ関数"
---

ラプラス型積分では、パラメータが大きくなると積分の主要な寄与が端点の近くから現れる。ワトソンの補題は、この事実を漸近展開として定式化する。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ワトソンの補題（Watson's Lemma）</div>

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

について、ある $x_0>0$ で $\int_0^\infty e^{-x_0t}|f(t)|\,dt<\infty$ とする。この条件のもとで $I(x)$ はすべての $x\geq x_0$ に対して絶対収束する。

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

$x\geq x_0$ のとき、後半は

$$
\left|\int_\delta^\infty e^{-xt}f(t)\,dt\right|
\leq e^{-(x-x_0)\delta}
\int_\delta^\infty e^{-x_0t}|f(t)|\,dt
$$

と評価できる。したがって、$x\to\infty$ で任意のべき $x^{-M}$ より速く減衰する。

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

に収束する。さらに $\int_{x\delta}^{\infty}e^{-u}u^{n+\lambda-1}\,du$ は指数的に小さくなるため、上限を $\infty$ に置き換える誤差は任意の逆べきより速く減衰する。

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

すなわち定理の漸近展開を得る。
<div class="proof-end">\(\square\)</div>

## 具体例：1 / (1 + t) を含むラプラス積分

$x>0$ に対して $I(x)=\int_0^\infty e^{-xt}/(1+t)\,dt$ を考える。原点付近の展開を、余りを含む恒等式として書くと、

$$
\frac1{1+t}=1-t+t^2-\frac{t^3}{1+t}.
$$

$\int_0^\infty e^{-xt}t^n\,dt=n!/x^{n+1}$ を各項に使うと、

$$
I(x)=\frac1x-\frac1{x^2}+\frac2{x^3}+R(x),
\qquad |R(x)|\leq\int_0^\infty e^{-xt}t^3\,dt=\frac6{x^4}.
$$

例えば $x=10$ なら $I(10)$ は $0.092$ と近似でき、誤差は $0.0006$ 以下である。端点付近の係数から、積分の漸近展開が得られる具体例である。

## 次の記事

[スターリングの公式](/articles/gamma-stirling-formula.html)
