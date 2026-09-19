---
layout: article
title: "代数方程式の解の回転対称性"
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

<div class="math-box-title">定理：解の回転対称性</div>

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

よって $\widetilde y$ も解である。$\square$

## 次の記事

[代数方程式の解のMellin変換](/articles/mellin-algebraic-transform.html)
