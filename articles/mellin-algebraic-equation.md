---
layout: article
title: "代数方程式の解の回転対称性（Rotational Symmetry of the Solutions of an Algebraic Equation）"
seo_title: "代数方程式の解の回転対称性｜複素数解の構造"
description: "代数方程式 y^μ+xy^p-1=0 の解が持つ回転対称性を、μ乗根と複素数解の関係から整理します。"
category: "gamma-function"
category_label: "ガンマ関数"
---

$$
y^\mu+xy^p-1=0,
\qquad
\mu>p>0
$$

を考える。ここでは $\mu,p$ を正整数とし、

$$
\varepsilon=e^{2\pi i/\mu}
$$

とおく。

<div class="math-box theorem-box">

<div class="math-box-title">定理：解の回転対称性（Rotational Symmetry of the Solutions）</div>

$y(x)$ が

$$
y^\mu+xy^p-1=0
$$

を満たすならば、任意の整数 $k$ に対して

$$
\widetilde y(x)
=
\varepsilon^k
y(\varepsilon^{pk}x)
$$

も同じ方程式を満たす。

</div>

## 証明

$$
t=\varepsilon^{pk}x
$$

とおく。

$y(t)$ は

$$
y(t)^\mu+ty(t)^p-1=0
$$

を満たす。

一方、

$$
\widetilde y(x)
=
\varepsilon^k y(t)
$$

なので、

$$
\begin{aligned}
\widetilde y(x)^\mu
+x\widetilde y(x)^p-1
&=
\varepsilon^{k\mu}y(t)^\mu
+x\varepsilon^{kp}y(t)^p-1.
\end{aligned}
$$

$\varepsilon^\mu=1$ かつ
$t=\varepsilon^{pk}x$ だから、

$$
\varepsilon^{k\mu}=1,
\qquad
x\varepsilon^{kp}=t.
$$

したがって、

$$
\widetilde y(x)^\mu
+x\widetilde y(x)^p-1
=
y(t)^\mu+ty(t)^p-1
=
0.
$$

よって $\widetilde y$ も解である。
<div class="proof-end">\(\square\)</div>

## 具体例：2次方程式の2つの解を結びつける

$\mu=2,p=1$ とすると方程式は $y^2+xy-1=0$ である。実数 $x$ に対して

$$
y_+(x)=\frac{-x+\sqrt{x^2+4}}2,
\qquad y_-(x)=\frac{-x-\sqrt{x^2+4}}2.
$$

ここでは $\varepsilon=-1$ なので、定理の $k=1$ の変換は $-y_+(-x)$ である。実際に代入すると

$$
-y_+(-x)=-\frac{x+\sqrt{x^2+4}}2=y_-(x).
$$

この対称性は、同じ $x$ で単に解の符号を変える操作ではなく、引数も $-x$ に変える操作である。

## 次の記事

[代数方程式の解のMellin変換](/articles/mellin-algebraic-transform.html)
