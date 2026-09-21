---
layout: article
title: "量子力学におけるエルミート多項式"
seo_title: "量子力学におけるエルミート多項式｜調和振動子との関係"
description: "エルミート多項式が量子力学の調和振動子型微分方程式に現れる理由を、微分方程式の変換から解説します。"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

エルミート多項式は、調和振動子型の微分方程式と直接結びついている。本記事では、エルミート多項式の微分方程式から指数関数を掛けた関数を作り、量子力学で現れる微分方程式との対応を確認する。

## 1. エルミート微分方程式

重み $e^{-x^2/2}$ に対応するエルミート多項式は、

$$
H_n''(x)
-
xH_n'(x)
+
nH_n(x)
=
0
$$

を満たす。

## 2. 指数関数を掛けた関数

次の関数を考える。

$$
U_n(x)
=
e^{-x^2/4}H_n(x).
$$

$W(x)=e^{-x^2/4}$ とおけば、

$$
U_n=WH_n
$$

である。微分すると、

$$
U_n'
=
W'H_n+WH_n',
$$

$$
U_n''
=
W''H_n+2W'H_n'+WH_n''.
$$

エルミート微分方程式

$$
H_n''
=
xH_n'-nH_n
$$

を代入する。$H_n'$ の項が消えるためには、

$$
2W'+xW=0
$$

を満たせばよく、その解が

$$
W(x)=Ce^{-x^2/4}
$$

である。

したがって、

<div class="math-box theorem-box">

<div class="math-box-title">エルミート関数の微分方程式</div>

$$
U_n(x)
=
e^{-x^2/4}H_n(x)
$$

は、

$$
U_n''(x)
+
\left(
n+\frac12-\frac{x^2}{4}
\right)
U_n(x)
=
0
$$

を満たす。

</div>

具体例として $n=3$ の正規化された固有関数を描くと、零点を持ちながら振動し、無限遠で指数的に減衰することが分かる。

<figure class="article-figure">
  <img src="/images/figures/hermite-oscillator.svg" alt="n=3の正規化された調和振動子固有関数V3の正確なグラフ">
  <figcaption>図1：$n=3$ の正規化された $V_3(x)=C_3e^{-x^2/2}H_3(\sqrt2x)$。3個の零点を持ち、$|x|\to\infty$ で指数的に $0$ へ減衰する。</figcaption>
</figure>

## 3. 調和振動子型の方程式

次の微分方程式を考える。

$$
V''(x)
+
(E-x^2)V(x)
=
0.
$$

変数の尺度を調整して上のエルミート関数の方程式と比較すると、許される値として

$$
E_n
=
2n+1
$$

が現れる。また、対応する解は、

$$
V_n(x)
=
C_n
e^{-x^2/2}
H_n(\sqrt{2}x)
$$

という形になる。

## 4. 二乗可積分性

物理的な状態として用いるためには、

$$
\int_{-\infty}^{\infty}
V_n(x)^2\,dx
<
\infty
$$

が必要になる。

上の $V_n$ では指数因子 $e^{-x^2/2}$ が付いているため、$V_n^2$ には $e^{-x^2}$ が現れる。$H_n(\sqrt2 x)$ は多項式であるため、指数関数の減衰によって積分は収束する。

定数 $C_n$ を適切に選べば、

$$
\int_{-\infty}^{\infty}
V_n(x)^2\,dx
=
1
$$

と規格化できる。

## 5. 確率密度

規格化された $V_n$ に対して、$V_n(x)^2$ を確率密度と考えると、

$$
P(a\leq x\leq b)
=
\int_a^b
V_n(x)^2\,dx.
$$

と書ける。

<figure class="article-figure">
  <img src="/images/figures/hermite-probability-density.svg" alt="n=3の確率密度V3の二乗を正確に描き区間マイナス1から1を塗ったグラフ">
  <figcaption>図2：$n=3$ の確率密度 $|V_3(x)|^2$。青く塗った部分は具体例として $P(-1\leq x\leq1)=\int_{-1}^{1}|V_3(x)|^2\,dx$ を表す。</figcaption>
</figure>

エルミート多項式は、このように調和振動子の固有状態を表す関数の多項式部分として現れる。

## 次の記事

[エルミート多項式とラゲール多項式の完備性](/articles/hermite-laguerre-completeness.html)
