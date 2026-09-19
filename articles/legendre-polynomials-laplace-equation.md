---
layout: article
title: "ルジャンドル多項式とラプラス方程式"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

ルジャンドル多項式の母関数は、3次元空間の静電ポテンシャルと同じ形を持つ。このことから、ルジャンドル多項式が球座標におけるラプラス方程式の変数分離から自然に現れることが分かる。

## 1. 静電ポテンシャルと母関数

点

$$
e=(0,0,1)
$$

に単位電荷を置き、原点からの距離が $r$、極角が $\theta$ である点を考える。

点 $e$ との距離を $\rho$ とすると、

$$
\rho
=
\sqrt{
1-2r\cos\theta+r^2
}.
$$

したがってポテンシャルは、

$$
u(r,\theta)
=
\frac{1}{\rho}
=
\frac{1}
{\sqrt{1-2r\cos\theta+r^2}}.
$$

ルジャンドル多項式の母関数

$$
\frac{1}
{\sqrt{1-2xt+t^2}}
=
\sum_{n=0}^{\infty}
P_n(x)t^n
$$

と比較すると、

$$
u(r,\theta)
=
\sum_{n=0}^{\infty}
P_n(\cos\theta)r^n
$$

という展開が得られる。

## 2. 球座標におけるラプラス方程式

電荷の存在しない領域では、

$$
\Delta u=0
$$

が成り立つ。

球座標 $(r,\theta,\phi)$ では、

$$
\Delta u
=
\frac{\partial^2u}{\partial r^2}
+
\frac{2}{r}
\frac{\partial u}{\partial r}
+
\frac{1}{r^2\sin\theta}
\frac{\partial}{\partial\theta}
\left(
\sin\theta
\frac{\partial u}{\partial\theta}
\right)
+
\frac{1}{r^2\sin^2\theta}
\frac{\partial^2u}{\partial\phi^2}.
$$

軸対称な場合には $\phi$ に依存しないため、最後の項は消える。

## 3. 変数分離

$$
u(r,\theta)
=
R(r)\Theta(\theta)
$$

とおく。ラプラス方程式へ代入して変数を分離すると、

$$
r^2R''+2rR'-\lambda^2R=0
$$

および、

$$
\frac{1}{\sin\theta}
\frac{d}{d\theta}
\left(
\sin\theta
\frac{d\Theta}{d\theta}
\right)
+
\lambda^2\Theta
=
0
$$

という2つの常微分方程式を得る。

## 4. 分離定数

多項式解に対応する場合、

$$
\lambda^2
=
n(n+1)
$$

とおくことができる。半径方向の方程式は、

$$
R(r)
=
C_1r^n
+
C_2r^{-n-1}
$$

という形の解を持つ。

原点近傍で有界な解を考える場合には、

$$
C_2=0
$$

を選ぶ。

## 5. 角度方向とルジャンドル方程式

角度方向の方程式で、

$$
x=\cos\theta
$$

と変数変換する。すると、

$$
(1-x^2)
\frac{d^2\Theta}{dx^2}
-
2x
\frac{d\Theta}{dx}
+
n(n+1)\Theta
=
0
$$

を得る。

これはルジャンドル微分方程式そのものである。したがって、

$$
\Theta(\theta)
=
P_n(\cos\theta)
$$

が現れる。

<div class="math-box theorem-box">

<div class="math-box-title">ラプラス方程式とルジャンドル多項式</div>

球座標で軸対称なラプラス方程式を変数分離すると、角度方向の方程式としてルジャンドル微分方程式が現れる。そのため、ルジャンドル多項式は球対称・軸対称なポテンシャル問題に自然に現れる。

</div>
