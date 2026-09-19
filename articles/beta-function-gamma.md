---
layout: article
title: "ベータ関数とガンマ関数"
category: "gamma-function"
category_label: "ガンマ関数"
---

ベータ関数はガンマ関数と密接に結びついた二変数の特殊関数である。本記事では、ベータ関数の定義、ガンマ関数との関係、複素積分を用いた解析接続を扱う。

## 1. ベータ関数の定義

<div class="math-box definition-box">

<div class="math-box-title">定義：ベータ関数</div>

$\operatorname{Re}x>0$、$\operatorname{Re}y>0$ に対して、

$$
B(x,y)
=
\int_0^1
t^{x-1}(1-t)^{y-1}\,dt
$$

と定める。

</div>

## 2. ガンマ関数との関係

<div class="math-box theorem-box">

<div class="math-box-title">ベータ関数とガンマ関数</div>

$$
B(x,y)
=
\frac{\Gamma(x)\Gamma(y)}
{\Gamma(x+y)}
$$

が成り立つ。

</div>

証明では、

$$
\Gamma(x)\Gamma(y)
=
\int_0^\infty
\int_0^\infty
e^{-(u+v)}
u^{x-1}v^{y-1}
\,du\,dv
$$

を考え、

$$
u=r\cos^2\theta,
\qquad
v=r\sin^2\theta
$$

と変数変換する。$r$ に関する積分と $\theta$ に関する積分が分離し、後者をさらに $t=\cos^2\theta$ で変換するとベータ積分が現れる。

## 3. ポッホハマー型積分路

ベータ積分は最初、

$$
\operatorname{Re}x>0,
\qquad
\operatorname{Re}y>0
$$

で定義される。解析接続のため、分岐点 $0$ と $1$ のまわりを回る積分路を考える。

$t^{x-1}$ と $(1-t)^{y-1}$ は、それぞれ $0$ と $1$ を一周すると位相因子を得る。積分路の各部分を組み合わせると、

$$
\int_C
t^{x-1}(1-t)^{y-1}\,dt
=
\left(
1-e^{2\pi i x}
\right)
\left(
1-e^{2\pi i y}
\right)
B(x,y)
$$

となる。

したがって、

<div class="math-box theorem-box">

<div class="math-box-title">ベータ関数の複素積分表示</div>

$$
B(x,y)
=
\frac{1}
{
(1-e^{2\pi i x})
(1-e^{2\pi i y})
}
\int_C
t^{x-1}(1-t)^{y-1}\,dt.
$$

</div>

この表示によって、もとの積分が直接収束しない領域にもベータ関数を解析接続できる。

## 次の記事

[ガンマ関数の対数微分：ディガンマ関数](/articles/digamma-function.html)
