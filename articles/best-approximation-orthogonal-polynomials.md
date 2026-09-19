---
layout: article
title: "直交多項式による最良近似"
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

<div class="math-box-title">定理：最良近似多項式</div>

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

連続関数 $f$ と最良近似多項式 $p_n$ に対して、$f-p_n$ の符号変化についても考える。$f-p_n$ が恒等的に $0$ でない場合には区間 $(a,b)$ 内で少なくとも $n-1$ 回符号を変えるという性質を扱っている。

この議論では、符号変化する点を用いて低次数の多項式を作り、その多項式と $f-p_n$ の内積を考える。最良近似の条件からは内積が $0$ になる一方、符号の取り方からは積分が一定符号を持つため、符号変化が少なすぎるという仮定に矛盾が生じる。

## 4. 幾何学的な見方

この定理は、$p_n$ が $f$ を

$$
\operatorname{span}
\{
\phi_0,\phi_1,\ldots,\phi_n
\}
$$

へ直交射影したものだと考えると理解しやすい。有限次元のベクトル空間でベクトルを部分空間へ直交射影すると最短距離が得られるのと同じ構造が、関数空間でも現れている。

## 次の記事

[ラグランジュ補間](/articles/lagrange-interpolation.html)
