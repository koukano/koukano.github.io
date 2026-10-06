---
layout: article
title: "直交多項式による最良近似（Best Approximation by Orthogonal Polynomials）"
seo_title: "直交多項式による最良近似｜L²最小二乗近似"
description: "正規直交多項式を用いたL²の意味での最良近似を解説し、直交射影が最小二乗近似を与える理由を数式で示します。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

正規直交多項式を用いて関数を多項式で近似するとき、どの多項式が $L^2$ の意味で最良近似になるかを考える。本記事では、その中心となる結果をまとめる。

$f$ を

$$
\int_a^b
w(x)f(x)^2\,dx
<
\infty
$$

を満たす関数とし、内積を

$$
\langle f,g\rangle
=
\int_a^b
w(x)f(x)g(x)\,dx
$$

とする。

<div class="math-box theorem-box">

<div class="math-box-title">定理：最良近似多項式（Best Approximation Polynomial）</div>

$f$ に対して、

$$
p_n(x)
=
\sum_{k=0}^{n}
\alpha_k\phi_k(x),
\qquad
\alpha_k
=
\langle f,\phi_k\rangle
$$

とおく。このとき $p_n$ は、高々 $n$ 次の多項式の中で

$$
\lVert f-p_n\rVert
$$

を最小にする。

</div>

## 1. 誤差が直交すること

$$
g(x)
=
f(x)-p_n(x)
$$

とおく。$k\leq n$ に対して、

$$
\langle g,\phi_k\rangle
=
\langle f,\phi_k\rangle
-
\alpha_k
=
0
$$

である。したがって $g$ は、高々 $n$ 次のすべての多項式と直交する。

## 2. 任意の他の多項式と比較する

高々 $n$ 次の任意の多項式 $q_n$ を考える。このとき、

$$
f-(p_n+q_n)
=
g-q_n
$$

である。$g$ と $q_n$ は直交するので、ピタゴラスの関係から、

$$
\lVert g-q_n\rVert^2
=
\lVert g\rVert^2
+
\lVert q_n\rVert^2
\geq
\lVert g\rVert^2.
$$

したがって、

$$
\lVert f-(p_n+q_n)\rVert
\geq
\lVert f-p_n\rVert.
$$

等号が成立するのは $q_n=0$ のときであるから、$p_n$ が最良近似多項式である。

## 3. 近似誤差の符号変化

有限区間 $[a,b]$ 上の実連続関数 $f$ と最良近似多項式 $p_n$ を考える。重み $w$ は可積分で、$(a,b)$ 上ほとんど至る所で正とする。このとき、$f-p_n$ が恒等的に $0$ でなければ、区間 $(a,b)$ 内で少なくとも $n+1$ 回符号を変える。

実際、符号変化が $m\leq n$ 回だけなら、その符号変化の位置を零点とする $m$ 次多項式 $q$ を選び、必要なら全体の符号を変えることで $(f-p_n)q\geq0$ とできる。この積はある開区間で正になるため、$\langle f-p_n,q\rangle>0$ となる。一方、最良近似の誤差は高々 $n$ 次のすべての多項式と直交するので、同じ内積は $0$ でなければならない。これは矛盾である。

## 4. 幾何学的な見方

この定理は、$p_n$ が $f$ を

$$
\operatorname{span}
\{
\phi_0,\phi_1,\ldots,\phi_n
\}
$$

へ直交射影したものだと考えると理解しやすい。有限次元のベクトル空間でベクトルを部分空間へ直交射影すると最短距離が得られるのと同じ構造が、関数空間でも現れている。

## 具体例：放物線を1次以下の多項式で最良近似する

$[-1,1]$、$w=1$ で $f(x)=x^2$ を $p_1(x)=a+bx$ により近似する。誤差が $1,x$ と直交する条件は

$$
\int_{-1}^1(x^2-a-bx)\,dx=\frac23-2a=0,
\qquad
\int_{-1}^1x(x^2-a-bx)\,dx=-\frac23b=0.
$$

よって $p_1(x)=1/3$ であり、最小二乗誤差は $\int_{-1}^1(x^2-1/3)^2dx=8/45$ となる。対称性により傾きは $0$ になる。誤差は $x=\pm1/\sqrt3$ で符号を変え、$n+1=2$ 回という下限も実現している。

## 次の記事

[ラグランジュ補間](/articles/lagrange-interpolation.html)
