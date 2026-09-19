---
layout: article
title: "ベータ関数のポッホハマー積分表示"
category: "gamma-function"
category_label: "ガンマ関数"
---

ベータ積分は最初、$\operatorname{Re}x>0$、$\operatorname{Re}y>0$ で定義される。分岐点 $0$ と $1$ のまわりを回るポッホハマー型積分路を使うと、複素積分による解析接続が得られる。

積分路 $C$ の向きと分枝は、区間 $(0,1)$ 上で

$
t^{x-1}(1-t)^{y-1}>0
$

となる主値から出発し、$0$ と $1$ の周回による位相因子がそれぞれ $e^{2\pi i x}$、$e^{2\pi i y}$ となるように固定する。

<figure class="article-figure">
  <img src="/images/figures/pochhammer-contour.svg" alt="分岐点0と1のまわりを回るポッホハマー積分路の模式図">
  <figcaption>図1：ノートに描かれているポッホハマー積分路を整理した模式図。分岐点 $0$ と $1$ を周回し、区間 $(0,1)$ を異なる分枝で往復する。</figcaption>
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

積分路を、$0$ と $1$ の小円、およびそれらを結ぶ区間 $(0,1)$ の往復に分ける。

最初に $(0,1)$ を進むときには、被積分関数は

$$
t^{x-1}(1-t)^{y-1}
$$

そのものである。

$1$ を一周すると $(1-t)^{y-1}$ に位相因子

$$
e^{2\pi i y}
$$

が付く。その状態で区間を逆向きに戻るため、その寄与は符号も反転する。

さらに $0$ を一周すると $t^{x-1}$ に

$$
e^{2\pi i x}
$$

が付く。

4本の区間部分の寄与を同じ向きの積分

$$
\int_0^1
t^{x-1}(1-t)^{y-1}\,dt
=
B(x,y)
$$

にそろえて足し合わせると、係数は

$$
1-e^{2\pi i y}
-e^{2\pi i x}
+e^{2\pi i(x+y)}
$$

となる。

これは

$$
(1-e^{2\pi i x})
(1-e^{2\pi i y})
$$

に等しい。

小円の半径を $0$ にすると、最初の収束領域
$\operatorname{Re}x>0$、$\operatorname{Re}y>0$ では小円部分の寄与は消える。したがって、

$$
\int_C
t^{x-1}(1-t)^{y-1}\,dt
=
(1-e^{2\pi i x})
(1-e^{2\pi i y})
B(x,y).
$$

右辺との恒等式によって、その後は解析接続として理解できる。$\square$

## 次の記事

[ディガンマ関数](/articles/digamma-function.html)
