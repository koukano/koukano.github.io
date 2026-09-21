---
layout: article
title: "直交多項式の3項間漸化式"
seo_title: "直交多項式の3項間漸化式｜公式と証明"
description: "正規直交多項式が満たす3項間漸化式を、係数の導出と直交性を用いた証明とともに整理します。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

直交多項式には、隣り合う3つの次数の多項式を結びつける3項間漸化式が存在する。本記事では、その導出を確認する。表記はサイト内で統一している。

$n$ 次の正規直交多項式を

$$
\phi_n(x)=k_nx^n+\cdots,
\qquad
k_n>0
$$

とする。

<div class="math-box theorem-box">

<div class="math-box-title">定理：3項間漸化式</div>

正規直交多項式 $\phi_n$ は

$$
\phi_{n+1}(x)
-
(A_nx+B_n)\phi_n(x)
+
C_n\phi_{n-1}(x)
=
0
$$

という3項間漸化式を満たす。ここで、

$$
A_n=\frac{k_{n+1}}{k_n},
\qquad
C_n=\frac{A_n}{A_{n-1}},
\qquad
C_0=0
$$

である。

</div>

## 1. 最高次の項を消す

まず、

$$
A_n=\frac{k_{n+1}}{k_n}
$$

とおく。このとき、

$$
\phi_{n+1}(x)-A_nx\phi_n(x)
$$

では $x^{n+1}$ の項が打ち消される。実際、

$$
\phi_{n+1}(x)=k_{n+1}x^{n+1}+\cdots
$$

であり、

$$
A_nx\phi_n(x)
=
\frac{k_{n+1}}{k_n}x
\left(
k_nx^n+\cdots
\right)
=
k_{n+1}x^{n+1}+\cdots
$$

だからである。したがって、

$$
\phi_{n+1}(x)-A_nx\phi_n(x)
$$

は高々 $n$ 次の多項式になる。

正規直交多項式 $\phi_0,\phi_1,\ldots,\phi_n$ を用いると、

$$
\phi_{n+1}(x)-A_nx\phi_n(x)
=
\sum_{k=0}^{n}\beta_k\phi_k(x)
$$

と展開できる。

## 2. 低い次数の係数が消えることを示す

両辺と $\phi_j$ の内積をとると、

$$
\beta_j
=
\left\langle
\phi_{n+1}-A_nx\phi_n,
\phi_j
\right\rangle.
$$

$j\leq n$ では直交性より

$$
\langle\phi_{n+1},\phi_j\rangle=0
$$

なので、

$$
\beta_j
=
-A_n\langle x\phi_n,\phi_j\rangle.
$$

内積の対称性を用いると、

$$
\langle x\phi_n,\phi_j\rangle
=
\langle\phi_n,x\phi_j\rangle.
$$

$j\leq n-2$ のとき $x\phi_j$ の次数は高々 $n-1$ であるため、$\phi_n$ と直交する。したがって、

$$
\beta_0=\beta_1=\cdots=\beta_{n-2}=0.
$$

よって、

$$
\phi_{n+1}(x)-A_nx\phi_n(x)
=
\beta_n\phi_n(x)
+
\beta_{n-1}\phi_{n-1}(x).
$$

ここで、

$$
\beta_n=B_n,
\qquad
\beta_{n-1}=-C_n
$$

とおけば、

$$
\phi_{n+1}(x)
-
(A_nx+B_n)\phi_n(x)
+
C_n\phi_{n-1}(x)
=
0
$$

を得る。

## 3. $C_n$ を求める

上の展開から、

$$
C_n
=
A_n
\langle x\phi_n,\phi_{n-1}\rangle
=
A_n
\langle\phi_n,x\phi_{n-1}\rangle.
$$

一方、

$$
x\phi_{n-1}(x)
=
k_{n-1}x^n+\cdots
$$

であり、

$$
\phi_n(x)=k_nx^n+\cdots
$$

なので、

$$
x\phi_{n-1}(x)
=
\frac{k_{n-1}}{k_n}
\left[
\phi_n(x)
+
\sum_{j=0}^{n-1}\gamma_j\phi_j(x)
\right].
$$

$A_{n-1}=k_n/k_{n-1}$ であるから、

$$
x\phi_{n-1}(x)
=
\frac{1}{A_{n-1}}
\left[
\phi_n(x)
+
\sum_{j=0}^{n-1}\gamma_j\phi_j(x)
\right].
$$

これを内積に代入すると、直交性より低次の項はすべて消え、

$$
C_n
=
\frac{A_n}{A_{n-1}}.
$$

したがって3項間漸化式は完全に定まる。

## 4. この式の意味

3項間漸化式は、直交多項式が単なるばらばらの多項式列ではなく、隣り合う次数の間に強い構造を持つことを示している。この漸化式は、次の記事で扱うクリストッフェル・ダルブーの公式を導くための基本となる。

## 次の記事

[クリストッフェル・ダルブーの公式](/articles/christoffel-darboux-formula.html)
