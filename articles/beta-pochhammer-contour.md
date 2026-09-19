---
layout: article
title: "ベータ関数のポッホハマー積分表示"
category: "gamma-function"
category_label: "ガンマ関数"
---

ベータ積分は最初、$\operatorname{Re}x>0$、$\operatorname{Re}y>0$ で定義される。分岐点 $0$ と $1$ のまわりを回るポッホハマー型積分路を使うと、複素積分による解析接続が得られる。

基点 $P\in(0,1)$ をとり、そこで

$
t^{x-1}(1-t)^{y-1}>0
$

となる主値から解析接続を始める。積分路 $C$ は、$P$ から出発して

$
1+\;\longrightarrow\;0+\;\longrightarrow\;1-\;\longrightarrow\;0-
$

の順に周回して $P$ に戻るポッホハマー二重ループとする。ここで $+$ は反時計回り、$-$ は時計回りを表す。

<figure class="article-figure">
  <img src="/images/figures/pochhammer-contour.svg" alt="基点Pから1と0を正負の向きに順に回るポッホハマー二重ループ積分路">
  <figcaption>図1：標準的なポッホハマー二重ループ積分路。基点 $P\in(0,1)$ から出発し、$1$ を反時計回り、$0$ を反時計回り、$1$ を時計回り、$0$ を時計回りに周回して $P$ に戻る。</figcaption>
</figure>

<div class="math-box theorem-box">

<div class="math-box-title">定理：ベータ関数のポッホハマー積分表示</div>

上の向きと分枝のもとで、

$$
\int_C
t^{x-1}(1-t)^{y-1}\,dt
=
(1-e^{2\pi i x})
(1-e^{2\pi i y})
B(x,y)
$$

が成り立つ。

したがって、

$$
B(x,y)
=
\frac{
\displaystyle
\int_C
t^{x-1}(1-t)^{y-1}\,dt
}{
(1-e^{2\pi i x})
(1-e^{2\pi i y})
}.
$$

</div>

## 証明

まず $\operatorname{Re}x>0$、$\operatorname{Re}y>0$ とする。$0$ と $1$ のまわりの小円の半径を $0$ に近づければ、小円部分の積分は消えるので、残るのは区間 $(0,1)$ の往復だけである。

$
p=e^{2\pi i x},
\qquad
q=e^{2\pi i y}
$

とおく。$0$ を反時計回りに一周すると $t^{x-1}$ は $p$ 倍され、$1$ を反時計回りに一周すると $(1-t)^{y-1}$ は $q$ 倍される。時計回りではそれぞれ逆数倍される。

基点 $P$ で積分を

$
I_0=\int_0^P t^{x-1}(1-t)^{y-1}\,dt,
\qquad
I_1=\int_P^1 t^{x-1}(1-t)^{y-1}\,dt
$

と分ける。図の順序 $(1+,0+,1-,0-)$ に沿って各区間の寄与を追うと、

$
(1-q)I_1
+
q(p-1)I_0
+
p(q-1)I_1
+
(1-p)I_0
$

となる。これを整理すると、

$
(1-p)(1-q)(I_0+I_1)
$

である。ところが

$
I_0+I_1
=
\int_0^1 t^{x-1}(1-t)^{y-1}\,dt
=
B(x,y)
$

なので、

$
\int_C t^{x-1}(1-t)^{y-1}\,dt
=
(1-e^{2\pi i x})(1-e^{2\pi i y})B(x,y)
$

を得る。

この等式を解析接続することで、ポッホハマー積分表示として一般の複素パラメータへ拡張できる。$\square$

## 次の記事

[ディガンマ関数](/articles/digamma-function.html)
