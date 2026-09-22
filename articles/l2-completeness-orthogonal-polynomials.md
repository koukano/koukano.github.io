---
layout: article
title: "L²(w)における正規直交多項式の完備性（Completeness of Orthonormal Polynomials in L²(w)）"
seo_title: "L²(w)における正規直交多項式の完備性｜定義と証明"
description: "重み付きL²空間における正規直交多項式系の完備性を、コーシー列・ヒルベルト空間・閉性との関係から整理します。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

正規直交多項式が重み付き $L^2$ 空間で関数を十分に表現できるかという問題を考える。本記事では、完備性と閉性の関係を整理し、正規直交多項式系の完備性についてまとめる。

## 1. 完備性とヒルベルト空間

<div class="math-box definition-box">

<div class="math-box-title">定義：コーシー列（Cauchy Sequence）</div>

関数列 $\{f_n\}$ が、任意の $\varepsilon>0$ に対してある $N$ が存在し、

$$
\lVert f_n-f_m\rVert
<
\varepsilon
\qquad
(n,m>N)
$$

を満たすとき、$\{f_n\}$ をコーシー列という。

</div>

<div class="math-box definition-box">

<div class="math-box-title">定義：完備な内積空間（Complete Inner Product Space）</div>

すべてのコーシー列がその空間内の元へ収束するとき、その内積空間を完備という。完備な内積空間をヒルベルト空間という。

</div>

重み付き空間 $L^2(w)$ は、通常の同値関係を入れることでヒルベルト空間になる。

## 2. 閉性と完備性

ここでは、正規直交系 $\{\phi_n\}$ に対して、

$$
\langle f,\phi_n\rangle=0
\qquad
(n\geq0)
$$

がすべて成り立つならば $f=0$ となる性質を「閉じている」と表現している。

<div class="math-box theorem-box">

<div class="math-box-title">定理：閉性と完備性（Closedness and Completeness）</div>

ヒルベルト空間における正規直交系は、閉じていることと完備であることが同値である。

</div>

## 3. 閉性から完備性へ

$f\in L^2(w)$ に対して、

$$
\alpha_k
=
\langle f,\phi_k\rangle
$$

とし、

$$
g_n
=
f-
\sum_{k=0}^{n}
\alpha_k\phi_k
$$

とおく。

ベッセルの不等式から、

$$
\sum_{k=0}^{\infty}
\alpha_k^2
$$

は収束するため、$\{g_n\}$ はコーシー列になる。$L^2(w)$ の完備性から、ある $g\in L^2(w)$ が存在して、

$$
g_n\longrightarrow g
$$

となる。

一方、固定した $k$ に対して十分大きい $n$ では、

$$
\langle g_n,\phi_k\rangle=0.
$$

極限をとると、

$$
\langle g,\phi_k\rangle=0
$$

がすべての $k$ について成り立つ。正規直交系が閉じていれば $g=0$ なので、

$$
\left\lVert
f-
\sum_{k=0}^{n}
\alpha_k\phi_k
\right\rVert
\longrightarrow0.
$$

したがって正規直交系は完備である。

## 4. 完備性から閉性へ

逆に正規直交系が完備であり、

$$
\langle f,\phi_k\rangle=0
$$

がすべての $k$ について成り立つとする。パーセヴァルの等式から、

$$
\lVert f\rVert^2
=
\sum_{k=0}^{\infty}
\left|
\langle f,\phi_k\rangle
\right|^2
=
0
$$

なので、

$$
f=0.
$$

したがって正規直交系は閉じている。

## 5. 正規直交多項式系の完備性

さらに、有限区間上の重み付き $L^2(w)$ において、正規直交多項式系が完備であることをワイエルシュトラスの近似定理と結びつけている。

多項式すべてと直交する関数 $f$ を考える。すなわち、

$$
\int_a^b
w(x)f(x)x^n\,dx
=
0
$$

がすべての $n$ について成り立つとする。連続関数の場合、ワイエルシュトラスの近似定理を使って $f$ 自身を多項式で一様近似すると、上の直交条件から

$$
\int_a^b
w(x)f(x)^2\,dx
=
0
$$

を導くことができる。したがって、

$$
f=0
$$

となり、多項式系が閉じていることが分かる。閉性と完備性の同値性から、正規直交多項式系の完備性が得られる。

## 6. 直交多項式展開の意味

完備性が成り立つと、

$$
f
=
\sum_{k=0}^{\infty}
\langle f,\phi_k\rangle\phi_k
$$

を $L^2$ の意味で考えることができる。これは、有限次元の直交基底によるベクトル展開を関数空間へ拡張したものである。

## 次の記事

[リーマンの写像定理と直交多項式](/articles/riemann-mapping-orthogonal-polynomials.html)
