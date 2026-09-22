---
layout: article
title: "代数方程式の解のMellin変換（Mellin Transform of an Algebraic Function）"
seo_title: "代数方程式の解のMellin変換｜積分表示と導出"
description: "代数方程式 y^μ+xy^p-1=0 の正の実数解に対するMellin変換を定義し、ガンマ関数を含む表示へ導きます。"
category: "gamma-function"
category_label: "ガンマ関数"
---

$$
y^\mu+xy^p-1=0,
\qquad
\mu>p>0
$$

のうち、$x>0$ で $y(0)=1$ から続く正の実数解を考える。

<div class="math-box theorem-box">

<div class="math-box-title">定理：代数方程式の解のMellin変換（Mellin Transform of an Algebraic Function）</div>

$$
Y(z)
=
\int_0^\infty
y(x)^\mu x^{z-1}\,dx
$$

とおく。このとき、

$$
0<\operatorname{Re}z<\frac{\mu}{p}
$$

で

$$
Y(z)
=
\frac{
\Gamma(z)
\Gamma\left(
\frac{\mu-pz}{\mu}
\right)
}{
\Gamma\left(
\frac{\mu-pz}{\mu}+z+1
\right)
}
$$

が成り立つ。

</div>

## 証明

方程式を $x$ について解くと、

$$
x
=
y^{-p}-y^{\mu-p}
=
y^{-p}(1-y^\mu).
$$

$x$ が $0$ から $\infty$ へ増加すると、正の解 $y$ は $1$ から $0$ へ減少する。

微分すると、

$$
\frac{dx}{dy}
=
-py^{-p-1}
-(\mu-p)y^{\mu-p-1}.
$$

したがって、

$$
-dx
=
y^{-p-1}
\left[
p+(\mu-p)y^\mu
\right]dy.
$$

Mellin変換へ代入すると、

$$
\begin{aligned}
Y(z)
&=
\int_0^1
y^\mu
\left[
y^{-p}(1-y^\mu)
\right]^{z-1}
y^{-p-1}
\left[
p+(\mu-p)y^\mu
\right]dy.
\end{aligned}
$$

整理して、

$$
Y(z)
=
\int_0^1
y^{\mu-pz-1}
(1-y^\mu)^{z-1}
\left[
p+(\mu-p)y^\mu
\right]dy.
$$

ここで

$$
t=y^\mu,
\qquad
dy=\frac1\mu t^{1/\mu-1}dt
$$

とおき、

$$
a
=
\frac{\mu-pz}{\mu}
$$

とすると、

$$
Y(z)
=
\frac1\mu
\int_0^1
t^{a-1}(1-t)^{z-1}
\left[
p+(\mu-p)t
\right]dt.
$$

したがって、

$$
Y(z)
=
\frac1\mu
\left[
pB(a,z)
+
(\mu-p)B(a+1,z)
\right].
$$

ベータ関数の関係

$$
B(a+1,z)
=
\frac{a}{a+z}B(a,z)
$$

を用いると、

$$
Y(z)
=
\frac{B(a,z)}{a+z}.
$$

さらに、

$$
B(a,z)
=
\frac{\Gamma(a)\Gamma(z)}
{\Gamma(a+z)}
$$

だから、

$$
Y(z)
=
\frac{
\Gamma(a)\Gamma(z)
}{
\Gamma(a+z+1)
}.
$$

$a=(\mu-pz)/\mu$ を戻せば、

$$
Y(z)
=
\frac{
\Gamma(z)
\Gamma\left(
\frac{\mu-pz}{\mu}
\right)
}{
\Gamma\left(
\frac{\mu-pz}{\mu}+z+1
\right)
}.
$$

端点 $x=0$ と $x=\infty$ での収束条件を調べると、

$$
0<\operatorname{Re}z<\frac{\mu}{p}
$$

を得る。
<div class="proof-end">\(\square\)</div>

## 関連記事

- [代数方程式の解の回転対称性](/articles/mellin-algebraic-equation.html)
- [Mellin変換とMellin反転公式](/articles/mellin-transform-inversion.html)
