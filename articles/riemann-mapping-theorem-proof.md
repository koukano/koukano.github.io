---
layout: article
title: "リーマンの写像定理（Riemann Mapping Theorem）の証明"
seo_title: "リーマンの写像定理とは？定理の内容と証明"
description: "単連結な真部分領域と単位円板の正則同値を主張するリーマンの写像定理を、モンテルの定理やシュワルツの補題を用いて証明します。"
category: "complex-analysis"
category_label: "複素解析"
---

リーマンの写像定理は、複素平面上の単連結な真部分領域が単位円板と正則同値であることを主張する。本記事では、モンテルの定理、最大値の原理、シュワルツの補題などを用いた証明をまとめる。

> **注記**：以下では証明の流れを保ちながら、記号をサイト内で統一し、後続の議論から必要であることが明らかな単葉性の条件や、不等号などの明らかな誤植を論理が通る形に整えている。

## 1. リーマンの写像定理（Riemann Mapping Theorem）

単位円板を

$$
\mathbb{D}
=
\left\{
z\in\mathbb{C}
\mid
\lvert z\rvert<1
\right\}
$$

とする。

<div class="math-box theorem-box">

<div class="math-box-title">定理：リーマンの写像定理（Riemann Mapping Theorem）</div>

$D\subsetneq\mathbb{C}$ を単連結領域とする。このとき、$D$ から単位円板 $\mathbb{D}$ への正則な全単射写像

$$
\gamma:D\longrightarrow\mathbb{D}
$$

が存在する。さらに、$a\in D$ を固定し、

$$
\gamma(a)=0,
\qquad
\gamma'(a)>0
$$

という条件を課すと、$\gamma$ は一意に定まる。

</div>

## 2. 証明に用いる結果

証明では、次の結果を用いる。

<div class="math-box lemma-box">

<div class="math-box-title">補題：正則関数の領域保存定理（Open Mapping Theorem）</div>

定数でない正則関数は開集合を開集合へ写す。したがって、領域の像も領域になる。

</div>

<div class="math-box lemma-box">

<div class="math-box-title">補題：正則な対数と $n$ 乗根（Holomorphic Logarithms and $n$-th Roots）</div>

$D$ を単連結領域とし、$f$ を $D$ 上で零点を持たない正則関数とする。このとき、$D$ 上の正則な一価関数 $g,h$ で

$$
e^{g(z)}=f(z),
\qquad
h(z)^n=f(z)
$$

を満たすものが存在する。

</div>

<div class="math-box lemma-box">

<div class="math-box-title">補題：モンテルの定理（Montel's Theorem）</div>

領域 $D$ 上の正則関数族 $\mathcal{F}$ が $D$ の任意のコンパクト部分集合上で一様有界ならば、$\mathcal{F}$ は正規族である。

</div>

<div class="math-box lemma-box">

<div class="math-box-title">補題：最大値の原理（Maximum Modulus Principle）</div>

定数でない正則関数は、領域の内部で絶対値の最大値をとらない。

</div>

<div class="math-box lemma-box">

<div class="math-box-title">補題：シュワルツの補題（Schwarz's Lemma）</div>

$f$ を単位円板 $\mathbb{D}$ 上の正則関数とし、

$$
\lvert f(z)\rvert\leq 1,
\qquad
f(0)=0
$$

を満たすとする。このとき、

$$
\lvert f(z)\rvert\leq\lvert z\rvert,
\qquad
\lvert f'(0)\rvert\leq 1
$$

が成り立つ。

</div>

## 3. 極値問題として考える

$D$ 上の一点 $a$ を固定する。次の条件を満たす関数 $h$ の集合を $\mathcal{H}$ とする。

$$
\begin{aligned}
&\text{(i)}\quad h \text{ は }D\text{ 上単葉正則},\\
&\text{(ii)}\quad \lvert h(z)\rvert\leq 1 \qquad (z\in D),\\
&\text{(iii)}\quad h(a)=0,\qquad h'(a)>0.
\end{aligned}
$$

この関数族の中で $h'(a)$ を最大にする関数を求め、その関数が $D$ を $\mathbb{D}$ 上へ全単射に写すことを示す。

## 4. Step 1：$\mathcal{H}$ が空でないことを示す

$D\neq\mathbb{C}$ であるから、

$$
b\in\mathbb{C}\setminus D
$$

をとることができる。$z-b$ は単連結領域 $D$ 上で零点を持たない正則関数なので、$D$ 上で一価正則な平方根の分枝 $k$ が存在し、

$$
k(z)^2=z-b
$$

を満たす。

もし $k(z_1)=-k(z_2)$ ならば、

$$
z_1-b=k(z_1)^2=k(z_2)^2=z_2-b
$$

より $z_1=z_2$ である。しかしそのとき $k(z_1)=-k(z_1)$ となり $k(z_1)=0$ であるから $z_1=b\notin D$ となって矛盾する。したがって、

$$
k(z_1)\neq -k(z_2)
\qquad
(z_1,z_2\in D)
$$

である。

正則関数の領域保存定理より $k(D)$ は領域であるから、$k(a)$ を中心とするある円板

$$
B(k(a),r)
$$

が $k(D)$ に含まれる。一方、$-B(k(a),r)$ と $k(D)$ は交わらないので、

$$
\lvert k(z)+k(a)\rvert\geq r
\qquad
(z\in D)
$$

が成り立つ。特に $z=a$ とすると、

$$
2\lvert k(a)\rvert\geq r>0.
$$

また、

$$
k(z)^2=z-b
$$

を微分すると、

$$
2k(z)k'(z)=1
$$

であるから、$k'(z)\neq0$ である。

ここで、

$$
g(z)
=
\frac{r}{4}
\frac{\lvert k'(a)\rvert}{\lvert k(a)\rvert^2}
\frac{k(a)}{k'(a)}
\frac{k(z)-k(a)}{k(z)+k(a)}
$$

とおく。分母は $0$ にならないので $g$ は $D$ 上正則である。また、$k$ は単葉であり、$g$ は $k$ と一次分数変換の合成であるから単葉である。

さらに、

$$
\left|
\frac{k(z)-k(a)}
{k(z)+k(a)}
\right|
=
\lvert k(a)\rvert
\left|
\frac{1}{k(a)}
-
\frac{2}{k(z)+k(a)}
\right|
$$

であるから、

$$
\left|
\frac{k(z)-k(a)}
{k(z)+k(a)}
\right|
\leq
\lvert k(a)\rvert
\left(
\frac{1}{\lvert k(a)\rvert}
+
\frac{2}{r}
\right)
\leq
\frac{4}{r}\lvert k(a)\rvert.
$$

したがって、

$$
\lvert g(z)\rvert\leq1.
$$

また、

$$
g(a)=0
$$

であり、微分すると、

$$
g'(a)
=
\frac{r}{8}
\frac{\lvert k'(a)\rvert}{\lvert k(a)\rvert^2}
>0.
$$

よって、

$$
g\in\mathcal{H}
$$

であり、$\mathcal{H}\neq\varnothing$ が示された。

## 5. Step 2：$h'(a)$ を最大にする関数が存在する

次に、

$$
d
=
\sup_{h\in\mathcal{H}}h'(a)
$$

とおく。$a$ を中心とする十分小さい閉円板が $D$ に含まれるように $\rho>0$ をとると、任意の $h\in\mathcal{H}$ に対して $\lvert h\rvert\leq1$ であるから、コーシーの評価式より

$$
\lvert h'(a)\rvert\leq\frac{1}{\rho}.
$$

したがって、

$$
0<d<\infty.
$$

上限の定義から、$\mathcal{H}$ の関数列 $\{h_n\}$ で

$$
h_n'(a)\longrightarrow d
$$

を満たすものをとることができる。$\mathcal{H}$ は局所有界な正則関数族であるから、モンテルの定理より正規族である。したがって部分列をとることで、$h_n$ は $D$ 上で広義一様収束するとしてよい。その極限を $f$ とする。

正則関数列の局所一様収束から $f$ は正則であり、

$$
f(a)=0,
\qquad
f'(a)=d>0
$$

を満たす。また、$\lvert h_n(z)\rvert\leq1$ より、

$$
\lvert f(z)\rvert\leq1.
$$

さらに、単葉正則関数列の局所一様極限は、定数関数であるか単葉関数である。ここでは $f'(a)=d>0$ であるため $f$ は定数ではなく、したがって単葉である。よって、

$$
f\in\mathcal{H},
\qquad
f'(a)=d.
$$

## 6. Step 3：$f(D)=\mathbb{D}$ を示す

$f'(a)=d>0$ であるから $f$ は定数ではない。最大値の原理より、

$$
\lvert f(z)\rvert<1
\qquad
(z\in D)
$$

であり、

$$
f(D)\subset\mathbb{D}.
$$

ここで $f(D)=\mathbb{D}$ でないと仮定する。このとき、

$$
c\in\mathbb{D}\setminus f(D)
$$

をとることができる。$f(a)=0$ であるため $c\neq0$ である。

単位円板の自己同型

$$
\ell(z)
=
\frac{z-c}
{1-\overline{c}z}
$$

を考え、

$$
m=\ell\circ f
$$

とおく。$c\notin f(D)$ であるから $m$ は $D$ 上で零点を持たない。$D$ は単連結なので、$m$ の正則な平方根の分枝 $F$ が存在し、

$$
F(z)^2=m(z)
$$

を満たす。

$\ell$ は $\mathbb{D}$ を $\mathbb{D}$ へ写すため、

$$
\lvert F(z)\rvert<1.
$$

また、

$$
m(a)=\ell(0)=-c
$$

であるから、

$$
\lvert F(a)\rvert^2=\lvert c\rvert.
$$

$F^2=m$ を微分すると、

$$
2F(z)F'(z)=m'(z)
$$

であり、

$$
F'(a)
=
\frac{m'(a)}
{2F(a)}.
$$

さらに、

$$
\ell'(0)=1-\lvert c\rvert^2
$$

であるから、

$$
\lvert F'(a)\rvert
=
\frac{1-\lvert c\rvert^2}
{2\sqrt{\lvert c\rvert}}
d.
$$

ここで、$\mathbb{D}$ の自己同型

$$
n(z)
=
\frac{\lvert F'(a)\rvert}{F'(a)}
\frac{z-F(a)}
{1-\overline{F(a)}z}
$$

を考え、

$$
G=n\circ F
$$

とおく。$G$ は $D$ 上単葉正則で、

$$
\lvert G(z)\rvert<1,
\qquad
G(a)=0
$$

を満たす。また、

$$
G'(a)
=
\frac{\lvert F'(a)\rvert}
{1-\lvert F(a)\rvert^2}
$$

であるため、

$$
G'(a)
=
\frac{1+\lvert c\rvert}
{2\sqrt{\lvert c\rvert}}
d.
$$

相加相乗平均の不等式より、$0<\lvert c\rvert<1$ に対して

$$
\frac{1+\lvert c\rvert}
{2\sqrt{\lvert c\rvert}}
>1
$$

であるから、

$$
G'(a)>d.
$$

しかし $G\in\mathcal{H}$ なので、これは

$$
d=\sup_{h\in\mathcal{H}}h'(a)
$$

に矛盾する。したがって、

$$
f(D)=\mathbb{D}.
$$

よって $f$ は $D$ から $\mathbb{D}$ への正則な全単射写像である。

## 7. Step 4：正規化した写像の一意性

最後に一意性を示す。$h_0\in\mathcal{H}$ が

$$
h_0(D)=\mathbb{D}
$$

を満たすとする。任意の $h\in\mathcal{H}$ に対して、

$$
\varphi
=
h\circ h_0^{-1}
$$

とおくと、$\varphi$ は $\mathbb{D}$ 上正則で、

$$
\varphi(0)=0.
$$

シュワルツの補題から、

$$
\lvert\varphi'(0)\rvert\leq1.
$$

連鎖律より、

$$
h'(a)
=
\varphi'(0)h_0'(a)
$$

であり、$h'(a),h_0'(a)>0$ なので、

$$
h'(a)\leq h_0'(a).
$$

$h$ は任意であるから、

$$
d\leq h_0'(a).
$$

一方、$h_0\in\mathcal{H}$ なので $h_0'(a)\leq d$ であり、

$$
h_0'(a)=d.
$$

ここで、$D$ を $\mathbb{D}$ へ正則全単射に写す二つの関数 $f_1,f_2$ があり、

$$
f_1(a)=f_2(a)=0,
\qquad
f_1'(a)>0,
\qquad
f_2'(a)>0
$$

を満たすとする。上の議論から、

$$
f_1'(a)=f_2'(a)=d.
$$

そこで、

$$
\varphi
=
f_1\circ f_2^{-1}
$$

とおくと、$\varphi$ は単位円板の正則自己同型で、

$$
\varphi(0)=0,
\qquad
\varphi'(0)=1
$$

を満たす。シュワルツの補題の等号成立条件から、

$$
\varphi(z)=z
$$

である。したがって、

$$
f_1=f_2.
$$

以上により、$D$ から $\mathbb{D}$ への正則な全単射写像が存在し、

$$
\gamma(a)=0,
\qquad
\gamma'(a)>0
$$

という正規化条件のもとで一意に定まることが示された。
