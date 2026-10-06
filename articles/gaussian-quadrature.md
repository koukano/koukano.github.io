---
layout: article
title: "ガウスの求積公式（Gaussian Quadrature Formula）とクリストッフェル数"
seo_title: "ガウスの求積公式とは？直交多項式の零点と数値積分"
description: "直交多項式の零点を標本点に用いるガウスの求積公式を導き、クリストッフェル数の意味と正値性を説明します。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

直交多項式の零点は、数値積分の標本点として特別な性質を持つ。本記事では、ラグランジュ補間と直交性を用いてガウスの求積公式を導き、重みとして現れるクリストッフェル数が正であることを示す。

重み $w$ に関する正規直交多項式を $\phi_n(x)=k_nx^n+\cdots$、$k_n>0$ とする。特に $\int_a^b w(x)\phi_n(x)^2\,dx=1$ である。$\phi_n$ の相異なる零点を

$$
x_1,\ldots,x_n
$$

とする。

## 1. ラグランジュ補間との関係

$\phi_n$ の零点を標本点とするラグランジュ基本多項式は、

$$
\rho_j(x)
=
\frac{\phi_n(x)}
{(x-x_j)\phi_n'(x_j)}
$$

と書ける。

そこで、

$$
\lambda_{j,n}
=
\int_a^b
w(x)
\frac{\phi_n(x)}
{(x-x_j)\phi_n'(x_j)}
\,dx
$$

と定める。この $\lambda_{j,n}$ をクリストッフェル数という。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ガウスの求積公式（Gaussian Quadrature Formula）</div>

$f$ が高々 $2n-1$ 次の多項式ならば、

$$
\int_a^b
w(x)f(x)\,dx
=
\sum_{j=1}^{n}
\lambda_{j,n}f(x_j)
$$

が成り立つ。

</div>

## 2. 証明

$f$ のラグランジュ補間多項式を

$$
F(x)
=
\sum_{j=1}^{n}
f(x_j)
\frac{\phi_n(x)}
{(x-x_j)\phi_n'(x_j)}
$$

とする。$F-f$ は各 $x_j$ で $0$ になるので、

$$
F(x)-f(x)
=
r(x)\phi_n(x)
$$

と書ける。$f$ の次数が高々 $2n-1$ であるため、$r$ の次数は高々 $n-1$ である。

両辺に $w(x)$ を掛けて積分すると、

$$
\int_a^b
w(x)f(x)\,dx
=
\sum_{j=1}^{n}
f(x_j)\lambda_{j,n}
-
\int_a^b
w(x)r(x)\phi_n(x)\,dx.
$$

最後の積分は、

$$
\langle r,\phi_n\rangle=0
$$

なので消える。したがって求積公式が得られる。

## 3. クリストッフェル数の表示

クリストッフェル・ダルブーの公式に $y=x_j$ を代入すると、

$$
K_{n-1}(x,x_j)
=
-\frac{k_n}{k_{n+1}}
\frac{
\phi_n(x)\phi_{n+1}(x_j)
}{
x-x_j
}
$$

となる。これを用いると、

$$
\lambda_{j,n}
=
-
\frac{k_{n+1}}{k_n}
\frac{1}
{\phi_n'(x_j)\phi_{n+1}(x_j)}
$$

と書ける。

直交多項式の零点の交互性から、

$$
\phi_n'(x_j)\phi_{n+1}(x_j)<0
$$

であるため、

$$
\lambda_{j,n}>0.
$$

したがってガウスの求積公式では、すべての重みが正になる。

## 4. 剰余項

剰余項では $[a,b]$ を有限区間とし、$w$ は可積分かつほとんど至る所で正、$f$ は実数値の $C^{2n}[a,b]$ 関数とする。エルミート補間の剰余項を積分し、$\int_a^b w(x)\phi_n(x)^2\,dx=1$ を用いると、ある $\xi\in(a,b)$ に対して、

$$
R
=
\frac{f^{(2n)}(\xi)}
{k_n^2(2n)!}
$$

という積分の剰余項を用いると、

$$
\int_a^b
w(x)f(x)\,dx
=
\sum_{j=1}^{n}
\lambda_{j,n}f(x_j)
+
R
$$

という形になり、さらに

$$
\lvert R\rvert
\leq
\frac{
\sup_{x\in(a,b)}
\lvert f^{(2n)}(x)\rvert
}{
k_n^2(2n)!
}
$$

という評価が得られる。

## 5. 何が特別なのか

$n$ 個の標本点だけを使うにもかかわらず、高々 $2n-1$ 次の多項式に対して積分値を正確に再現できる点がガウス求積の特徴である。その標本点が正規直交多項式 $\phi_n$ の零点であることが、直交性と数値積分を結びつけている。

## 具体例：2点のガウス求積と誤差

$[-1,1]$ 上で $w=1$、$n=2$ とする。節点は $P_2$ の零点 $\pm1/\sqrt3$、重みはどちらも $1$ なので、

$$
\int_{-1}^1 f(x)\,dx=f\left(-\frac1{\sqrt3}\right)+f\left(\frac1{\sqrt3}\right)
\qquad(\deg f\leq3).
$$

$f(x)=x^2$ では右辺は $1/3+1/3=2/3$ で、積分値と一致する。4次の $f(x)=x^4$ では積分値が $2/5$、求積値が $2/9$ となり、誤差は $8/45$ である。

正規直交多項式 $\phi_2=\sqrt{5/2}(3x^2-1)/2$ の最高次係数は $k_2^2=45/8$ だから、剰余公式も $R=24/(24k_2^2)=8/45$ と同じ誤差を与える。

## 次の記事

[高次数の直交多項式と零点の分布](/articles/zeros-distribution-orthogonal-polynomials.html)
