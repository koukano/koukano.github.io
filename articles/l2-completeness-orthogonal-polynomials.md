---
layout: article
title: "L²(w)における正規直交多項式の完備性（Completeness of Orthonormal Polynomials in L²(w)）"
seo_title: "L²(w)における正規直交多項式の完備性｜定義と証明"
description: "重み付きL²空間における正規直交多項式系の完備性を、コーシー列・ヒルベルト空間・閉性との関係から整理します。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
  - 'NIST, <a href="https://dlmf.nist.gov/18.2#viii">Digital Library of Mathematical Functions: General Orthogonal Polynomials: Quadrature and Completeness</a>.'
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

ここでは実関数の重み付き空間 $L^2(w)$ を考え、重み付き測度 $w(x)\,dx$ に関してほとんど至る所で等しい関数を同一視する。この同値関係を入れると $L^2(w)$ はヒルベルト空間になる。以下の $f=0$ も、この空間の元として零であることを意味する。

## 2. 閉性と完備性

正規直交系の「完備性」とは、その有限線形結合がヒルベルト空間全体で稠密であることをいう。これは、空間そのものの「すべてのコーシー列が収束する」という完備性とは区別する。

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

有限区間 $[a,b]$ 上で $w$ が可積分かつほとんど至る所で正であるとする。このとき、正規直交多項式系は $L^2(w)$ で完備である。

多項式すべてと直交する関数 $f$ を考える。すなわち、

$$
\int_a^b
w(x)f(x)x^n\,dx
=
0
$$

がすべての $n$ について成り立つとする。一般の $f\in L^2(w)$ は連続とは限らないため、$f$ 自身にワイエルシュトラスの一様近似定理を直接適用することはできない。

そこで、有限測度 $w(x)\,dx$ に関する $L^2$ 空間では連続関数が稠密であることを用いる。任意の $\varepsilon>0$ に対して、実連続関数 $h$ を

$$
\|f-h\|_{L^2(w)}<\frac{\varepsilon}{2}
$$

となるように選ぶ。$W=\int_a^b w(x)\,dx>0$ とおく。ワイエルシュトラスの近似定理により、実多項式 $p$ で

$$
\sup_{x\in[a,b]}|h(x)-p(x)|<\frac{\varepsilon}{2\sqrt W}
$$

を満たすものがある。したがって、

$$
\|h-p\|_{L^2(w)}\leq\sqrt W\,\sup_{[a,b]}|h-p|<\frac{\varepsilon}{2},
\qquad
\|f-p\|_{L^2(w)}<\varepsilon.
$$

すなわち、多項式は $L^2(w)$ で稠密である。さらに $f$ がすべての多項式と直交するならば、コーシー・シュワルツの不等式により

$$
\|f\|^2=\langle f,f-p\rangle
\leq\|f\|\,\|f-p\|\leq\|f\|\varepsilon.
$$

$\varepsilon$ は任意なので $\|f\|=0$、つまり $f=0$ がほとんど至る所で成り立つ。閉性と完備性の同値性から、正規直交多項式系の完備性が得られる。

## 6. 直交多項式展開の意味

完備性が成り立つと、

$$
f
=
\sum_{k=0}^{\infty}
\langle f,\phi_k\rangle\phi_k
$$

を $L^2$ の意味で考えることができる。これは、有限次元の直交基底によるベクトル展開を関数空間へ拡張したものである。

## 具体例：不連続な関数も平均二乗で近似できる

$[-1,1]$、$w=1$ で、$x<0$ なら $f(x)=-1$、$x>0$ なら $f(x)=1$ とし、$f(0)=0$ と定める。この関数は不連続だが $\|f\|^2=2$ なので $L^2$ に属する。ルジャンドル展開の1次・3次までの部分和は、係数を積分して求めると

$$
p_1(x)=\frac32P_1(x)=\frac32x,
\qquad p_3(x)=\frac32P_1(x)-\frac78P_3(x).
$$

直交性と $\|P_n\|^2=2/(2n+1)$ より、

$$
\|f-p_1\|^2=2-\frac32=\frac12,
\qquad
\|f-p_3\|^2=2-\frac32-\frac7{32}=\frac9{32}.
$$

完備性は、次数を増やすとこの $L^2$ 誤差が $0$ に近づくことを保証する。一方、不連続点を含む区間全体での一様収束を主張するものではない。

## 次の記事

[リーマンの写像定理と直交多項式](/articles/riemann-mapping-orthogonal-polynomials.html)
