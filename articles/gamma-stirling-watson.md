---
layout: article
title: "ワトソンの補題とスターリングの公式"
category: "gamma-function"
category_label: "ガンマ関数"
---

ガンマ関数の大きな引数に対する振る舞いを調べるためには漸近展開が重要になる。本記事では、漸近展開の定義、ラプラス型積分に対するワトソンの補題、スターリングの公式を整理する。

## 1. 漸近展開

関数 $f(z)$ に対して、

$$
f(z)
\sim
\sum_{k=0}^{\infty}
\frac{a_k}{z^k}
$$

と書くとは、任意の $N$ に対して、

$$
\lim_{z\to\infty}
z^N
\left[
f(z)
-
\sum_{k=0}^{N}
\frac{a_k}{z^k}
\right]
=
0
$$

が成り立つことをいう。

漸近級数は必ずしも通常の意味で収束する必要はなく、有限項で打ち切ったときの誤差が順に小さくなるという意味で使われる。

## 2. ワトソンの補題

$f(t)$ が $t=0$ の近傍で、

$$
f(t)
\sim
\sum_{k=0}^{\infty}
a_k t^{k/r-1}
$$

と展開できるとする。

ラプラス型積分

$$
I(x)
=
\int_0^\infty
e^{-xt}f(t)\,dt
$$

を考える。

<div class="math-box theorem-box">

<div class="math-box-title">ワトソンの補題</div>

$x\to\infty$ のとき、

$$
I(x)
\sim
\sum_{k=0}^{\infty}
a_k
\Gamma\left(\frac{k}{r}\right)
x^{-k/r}
$$

という形の漸近展開が得られる。

</div>

本質は、$x$ が大きいとき積分の主要な寄与が $t=0$ の近傍から来ることである。

## 3. ガンマ関数の積分を書き換える

オイラー積分で、

$$
t=e^x
$$

と変数変換すると、

$$
\Gamma(z)
=
\int_{-\infty}^{\infty}
\exp\left(
zx-e^x
\right)\,dx
$$

となる。

指数部

$$
f(x)=zx-e^x
$$

は、

$$
f'(x)=z-e^x
$$

より、

$$
x=\log z
$$

で極大となる。したがって、$z$ が大きいときにはこの点の近傍が積分の主要部分になる。

## 4. ガウス積分による第一近似

極大点の近傍で指数部を2次まで展開するとガウス積分が現れ、

$$
\Gamma(z+1)
\sim
\sqrt{2\pi z}
\left(
\frac{z}{e}
\right)^z
$$

を得る。

したがって、

<div class="math-box theorem-box">

<div class="math-box-title">スターリングの公式</div>

$$
\Gamma(z)
\sim
\sqrt{\frac{2\pi}{z}}
\left(
\frac{z}{e}
\right)^z
$$

が大きな $z$ に対する第一近似となる。

</div>

## 5. 高次の漸近展開

さらに高次の項まで考えると、

$$
\Gamma(z)
\sim
\sqrt{\frac{2\pi}{z}}
\left(
\frac{z}{e}
\right)^z
\sum_{k=0}^{\infty}
\frac{a_k}{z^k}
$$

という形になる。

最初の係数は、

$$
a_0=1,
\qquad
a_1=\frac{1}{12}
$$

である。

したがって、

$$
\Gamma(z)
\sim
\sqrt{\frac{2\pi}{z}}
\left(
\frac{z}{e}
\right)^z
\left(
1+\frac{1}{12z}+\cdots
\right).
$$

## 6. 注意

ここでは、×印で取り消されていた計算は使用していない。高次係数の導出については、取り消されていない部分から確認できる範囲のみを記載している。

## 次の記事

[ガンマ関数の乗法公式と倍角公式](/articles/gamma-multiplication-formula.html)
