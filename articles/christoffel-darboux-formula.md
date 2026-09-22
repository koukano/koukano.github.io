---
layout: article
title: "クリストッフェル・ダルブーの公式（Christoffel–Darboux Formula）"
seo_title: "クリストッフェル・ダルブーの公式｜直交多項式と再生核"
description: "直交多項式の有限和を2つの連続する多項式で表すクリストッフェル・ダルブーの公式を、再生核との関係とともに導きます。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

正規直交多項式から作られる有限和

$$
K_n(x,y)
=
\sum_{k=0}^{n}
\phi_k(x)\phi_k(y)
$$

は、再生核として重要な役割を持つ。本記事では、この和を2つの連続する直交多項式だけで表すクリストッフェル・ダルブーの公式を導く。

<div class="math-box theorem-box">

<div class="math-box-title">定理：クリストッフェル・ダルブーの公式（Christoffel–Darboux Formula）</div>

$n$ 次までの正規直交多項式から

$$
K_n(x,y)
=
\sum_{k=0}^{n}
\phi_k(x)\phi_k(y)
$$

と定める。このとき、

$$
K_n(x,y)
=
\frac{k_n}{k_{n+1}}
\frac{
\phi_n(y)\phi_{n+1}(x)
-
\phi_n(x)\phi_{n+1}(y)
}{
x-y
}
$$

が成り立つ。

</div>

## 1. 3項間漸化式を用いる

前の記事で得た3項間漸化式

$$
\phi_{n+1}(x)
=
(A_nx+B_n)\phi_n(x)
-
C_n\phi_{n-1}(x)
$$

を $x$ と $y$ の両方について書く。

$$
\phi_{n+1}(x)
=
(A_nx+B_n)\phi_n(x)
-
C_n\phi_{n-1}(x),
$$

$$
\phi_{n+1}(y)
=
(A_ny+B_n)\phi_n(y)
-
C_n\phi_{n-1}(y).
$$

これらを

$$
\phi_n(y)\phi_{n+1}(x)
-
\phi_n(x)\phi_{n+1}(y)
$$

に代入すると、$B_n$ を含む項は打ち消し合い、

$$
A_n(x-y)\phi_n(x)\phi_n(y)
+
C_n
\left[
\phi_n(x)\phi_{n-1}(y)
-
\phi_n(y)\phi_{n-1}(x)
\right]
$$

が残る。

したがって、

$$
\frac{k_n}{k_{n+1}}
\frac{
\phi_n(y)\phi_{n+1}(x)
-
\phi_n(x)\phi_{n+1}(y)
}{
x-y
}
$$

は、

$$
\phi_n(x)\phi_n(y)
+
\frac{k_{n-1}}{k_n}
\frac{
\phi_{n-1}(y)\phi_n(x)
-
\phi_{n-1}(x)\phi_n(y)
}{
x-y
}
$$

と書ける。

同じ操作を順次繰り返すと、

$$
K_n(x,y)
=
\sum_{k=0}^{n}
\phi_k(x)\phi_k(y)
$$

を得る。

## 2. $y\to x$ の極限

クリストッフェル・ダルブーの公式で $y\to x$ とすると、

$$
K_n(x,x)
=
\frac{k_n}{k_{n+1}}
\left[
\phi_n(x)\phi_{n+1}'(x)
-
\phi_n'(x)\phi_{n+1}(x)
\right].
$$

一方、定義から、

$$
K_n(x,x)
=
\sum_{k=0}^{n}
\phi_k(x)^2
\geq0.
$$

したがって、

$$
\frac{k_n}{k_{n+1}}
\left[
\phi_n(x)\phi_{n+1}'(x)
-
\phi_n'(x)\phi_{n+1}(x)
\right]
\geq0
$$

という関係も得られる。

## 3. 再生核としての性質

$p$ を高々 $n$ 次の多項式とする。正規直交多項式を用いて

$$
p(x)
=
\sum_{k=0}^{n}
c_k\phi_k(x)
$$

と書くと、

$$
\langle p,K_n(\cdot,y)\rangle
=
\sum_{k=0}^{n}
c_k\phi_k(y)
=
p(y)
$$

が成り立つ。つまり $K_n$ は、内積によって点 $y$ での値を再現する。

この再生性は、次の記事で扱う極値問題にもつながる。

## 次の記事

[再生核と極値問題](/articles/reproducing-kernel-extremal-property.html)
