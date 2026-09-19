---
layout: article
title: "ベータ関数とガンマ関数の関係"
category: "gamma-function"
category_label: "ガンマ関数"
---

ベータ関数を

$$
B(x,y)
=
\int_0^1 t^{x-1}(1-t)^{y-1}\,dt
$$

と定める。ただし最初は

$$
\operatorname{Re}x>0,
\qquad
\operatorname{Re}y>0
$$

とする。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ベータ関数とガンマ関数</div>

$$
B(x,y)
=
\frac{\Gamma(x)\Gamma(y)}
{\Gamma(x+y)}
$$

が成り立つ。

</div>

## 証明

ガンマ関数の積を二重積分として書く。

$$
\Gamma(x)\Gamma(y)
=
\int_0^\infty\int_0^\infty
e^{-(u+v)}
u^{x-1}v^{y-1}
\,du\,dv.
$$

ここで

$$
r=u+v,
\qquad
t=\frac{u}{u+v}
$$

とおく。すると

$$
u=rt,
\qquad
v=r(1-t),
$$

であり、

$$
r>0,
\qquad
0<t<1.
$$

ヤコビアンは

$$
\left|
\frac{\partial(u,v)}
{\partial(r,t)}
\right|
=
r
$$

なので、

$$
du\,dv=r\,dr\,dt.
$$

したがって、

$$
\begin{aligned}
\Gamma(x)\Gamma(y)
&=
\int_0^\infty\int_0^1
e^{-r}
(rt)^{x-1}
(r(1-t))^{y-1}
r\,dt\,dr\\
&=
\left(
\int_0^\infty
e^{-r}r^{x+y-1}\,dr
\right)
\left(
\int_0^1
t^{x-1}(1-t)^{y-1}\,dt
\right).
\end{aligned}
$$

第1因子は

$$
\Gamma(x+y)
$$

であり、第2因子は

$$
B(x,y)
$$

である。

よって、

$$
\Gamma(x)\Gamma(y)
=
\Gamma(x+y)B(x,y).
$$

両辺を $\Gamma(x+y)$ で割れば、

$$
B(x,y)
=
\frac{\Gamma(x)\Gamma(y)}
{\Gamma(x+y)}
$$

を得る。$\square$

## 次の記事

[ベータ関数のポッホハマー積分表示](/articles/beta-pochhammer-contour.html)
