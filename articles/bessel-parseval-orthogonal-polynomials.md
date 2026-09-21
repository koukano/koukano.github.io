---
layout: article
title: "ベッセルの不等式とパーセヴァルの等式"
seo_title: "ベッセルの不等式とパーセヴァルの等式｜直交多項式とL²空間"
description: "重み付きL²空間におけるベッセルの不等式とパーセヴァルの等式を、正規直交多項式による展開との関係を含めて数式とともに整理します。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

正規直交多項式を有限次元の多項式空間から $L^2$ 空間へ拡張して考える。本記事では、その準備としてベッセルの不等式とパーセヴァルの等式を整理する。

## 1. 重み付き $L^2$ 空間

$$
\int_a^b
w(x)f(x)^2\,dx
<
\infty
$$

を満たす実関数からなる空間を $L^2(w)$ とする。内積を

$$
\langle f,g\rangle
=
\int_a^b
w(x)f(x)g(x)\,dx
$$

とし、ノルムを

$$
\lVert f\rVert
=
\sqrt{\langle f,f\rangle}
$$

とする。

正規直交多項式系を $\{\phi_n\}$ とし、

$$
\alpha_k
=
\langle f,\phi_k\rangle
$$

とおく。

## 2. 部分和

$f$ の直交展開の第 $n$ 部分和を

$$
p_n(x)
=
\sum_{k=0}^{n}
\alpha_k\phi_k(x)
$$

とする。直交性を使うと、

$$
\left\lVert
f-
\sum_{k=0}^{n}
\alpha_k\phi_k
\right\rVert^2
=
\lVert f\rVert^2
-
\sum_{k=0}^{n}
\alpha_k^2.
$$

左辺は非負なので、

<div class="math-box theorem-box">

<div class="math-box-title">ベッセルの不等式</div>

$$
\sum_{k=0}^{n}
\alpha_k^2
\leq
\lVert f\rVert^2
$$

がすべての $n$ について成り立つ。したがって、

$$
\sum_{k=0}^{\infty}
\alpha_k^2
\leq
\lVert f\rVert^2.
$$

</div>

この不等式は、直交展開の係数の二乗和が元の関数のノルムを超えないことを示している。

## 3. パーセヴァルの等式

正規直交系が十分に豊かで、部分和が $f$ に $L^2$ の意味で収束するとき、

$$
\left\lVert
f-
\sum_{k=0}^{n}
\alpha_k\phi_k
\right\rVert
\longrightarrow0.
$$

したがって、

$$
\lVert f\rVert^2
=
\sum_{k=0}^{\infty}
\alpha_k^2
$$

を得る。

<div class="math-box definition-box">

<div class="math-box-title">パーセヴァルの等式</div>

$$
\lVert f\rVert^2
=
\sum_{k=0}^{\infty}
\left|
\langle f,\phi_k\rangle
\right|^2
$$

がすべての $f\in L^2(w)$ に対して成り立つとき、正規直交系は完備であるという。

</div>

## 4. 有限次元のピタゴラスの定理との対応

ベッセルの不等式は、有限次元のユークリッド空間における直交射影の関係と同じ構造を持つ。完全な正規直交基底が存在すれば、ベクトルの長さは各座標成分の二乗和に一致する。パーセヴァルの等式は、その無限次元版と見ることができる。

## 次の記事

[$L^2(w)$ における正規直交多項式の完備性](/articles/l2-completeness-orthogonal-polynomials.html)
