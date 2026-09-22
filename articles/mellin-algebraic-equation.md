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
y(t)^\mu+t,y(t)^p-1=0
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
y(t)^\mu+t,y(t)^p-1
=
0.
$$

よって $\widetilde y$ も解である。
<div class="proof-end">\(\square\)</div>

## 次の記事

[代数方程式の解のMellin変換](/articles/mellin-algebraic-transform.html)
