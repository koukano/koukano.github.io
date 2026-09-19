---
layout: article
title: "スターリングの公式"
category: "gamma-function"
category_label: "ガンマ関数"
---

ガンマ関数の大きな引数に対する第一近似を与えるのがスターリングの公式である。本記事では、実数 $x\to+\infty$ の場合をラプラス法で証明する。

<div class="math-box theorem-box">

<div class="math-box-title">定理：スターリングの公式</div>

$x\to+\infty$ のとき、

$$
\Gamma(x)
\sim
\sqrt{\frac{2\pi}{x}}
\left(\frac{x}{e}\right)^x
$$

が成り立つ。

同値な形として、

$$
\Gamma(x+1)
\sim
\sqrt{2\pi x}
\left(\frac{x}{e}\right)^x
$$

とも書ける。

</div>

## 証明

オイラー積分から、

$$
\Gamma(x+1)
=
\int_0^\infty e^{-t}t^x\,dt.
$$

ここで

$$
t=xu
$$

と変数変換すると、

$$
\Gamma(x+1)
=
x^{x+1}
\int_0^\infty
e^{-xu}u^x\,du.
$$

指数関数の形にまとめると、

$$
\Gamma(x+1)
=
x^{x+1}
\int_0^\infty
\exp\left[
x(\log u-u)
\right]
\,du.
$$

$$
\phi(u)
=
\log u-u
$$

とおく。

この関数は

$$
\phi'(u)
=
\frac1u-1
$$

より $u=1$ で最大値をとる。また、

$$
\phi(1)=-1,
\qquad
\phi''(1)=-1.
$$

$u=1+s$ とおき、$s=0$ の近くでテイラー展開すると、

$
\phi(1+s)
=
-1
-
\frac{s^2}{2}
+
O(s^3).
$

ノートでは、このラプラス法の考え方を「指数部が最大になる点の近くに積分の寄与が集中する」という図で捉えている。

<figure class="article-figure">
  <img src="/images/figures/stirling-laplace-method.svg" alt="phi(u)がu=1で最大となりexp(x phi(u))がu=1付近に集中する図">
  <figcaption>図1：ラプラス法の直感。$\phi(u)=\log u-u$ は $u=1$ で最大となり、$x$ が大きいほど $e^{x\phi(u)}$ はその近くに集中する。</figcaption>
</figure>

$x$ が大きいとき、積分への主要な寄与は $s=0$、すなわち $u=1$ の近くから来る。

したがってラプラス法により、

$$
\int_0^\infty
e^{x\phi(u)}\,du
\sim
e^{-x}
\sqrt{\frac{2\pi}{x}}.
$$

これを元の式へ代入すると、

$$
\begin{aligned}
\Gamma(x+1)
&\sim
x^{x+1}
e^{-x}
\sqrt{\frac{2\pi}{x}}\\
&=
\sqrt{2\pi x}
\left(\frac{x}{e}\right)^x.
\end{aligned}
$$

関数方程式

$$
\Gamma(x+1)=x\Gamma(x)
$$

で両辺を $x$ で割れば、

$$
\Gamma(x)
\sim
\sqrt{\frac{2\pi}{x}}
\left(\frac{x}{e}\right)^x
$$

を得る。$\square$

## 補足

複素数 $z$ に対しても、負の実軸から離れた扇形

$$
|\arg z|\leq\pi-\delta
\qquad
(\delta>0)
$$

では対応するスターリング展開が成り立つ。ただし複素数の場合は $z^z$ の分枝を固定する必要がある。

## 次の記事

[ガウスの乗法公式](/articles/gamma-multiplication-formula.html)
