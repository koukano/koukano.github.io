---
layout: article
title: "正則関数の平均値公式"
seo_title: "正則関数の平均値公式｜コーシーの積分公式から証明"
description: "正則関数の値が円周上の値の平均で表される平均値公式を、コーシーの積分公式から証明します。"
category: "complex-analysis"
category_label: "複素解析"
---

正則関数の一点での値は、その点を中心とする円周上の値の平均として表せる。本記事では、この平均値公式をコーシーの積分公式から証明する。

<div class="math-box theorem-box">

<div class="math-box-title">定理：正則関数の平均値公式</div>

$f$ を領域 $D$ 上の正則関数とし、$a\in D$ とする。半径 $r>0$ の閉円板

$$
\overline{B(a,r)}
=
\{z\in\mathbb{C}:|z-a|\leq r\}
$$

が $D$ に含まれているとする。このとき、

$$
f(a)
=
\frac{1}{2\pi}
\int_0^{2\pi}
f(a+re^{i\theta})\,d\theta
$$

が成り立つ。

</div>

## 証明

$f$ は $D$ 上正則であり、円周

$$
|\xi-a|=r
$$

とその内部は $D$ に含まれている。したがって、コーシーの積分公式より

$$
f(a)
=
\frac{1}{2\pi i}
\int_{|\xi-a|=r}
\frac{f(\xi)}{\xi-a}\,d\xi
$$

である。

円周を

$$
\xi=a+re^{i\theta},
\qquad
0\leq\theta\leq2\pi
$$

とパラメータ表示すると、

$$
d\xi
=
ire^{i\theta}\,d\theta
$$

であり、

$$
\xi-a
=
re^{i\theta}
$$

である。

これをコーシーの積分公式に代入すると、

$$
\begin{aligned}
f(a)
&=
\frac{1}{2\pi i}
\int_0^{2\pi}
\frac{f(a+re^{i\theta})}
{re^{i\theta}}
ire^{i\theta}\,d\theta\\
&=
\frac{1}{2\pi}
\int_0^{2\pi}
f(a+re^{i\theta})\,d\theta.
\end{aligned}
$$

したがって、

$$
f(a)
=
\frac{1}{2\pi}
\int_0^{2\pi}
f(a+re^{i\theta})\,d\theta
$$

が示された。$\square$

## 関連記事

- [リーマンの写像定理の証明](/articles/riemann-mapping-theorem-proof.html)
- [再生核によるリーマン写像の表示](/articles/riemann-mapping-orthogonal-polynomials.html)
