---
layout: article
title: "再生核と極値問題"
category: "special-functions"
category_label: "特殊関数"
---

クリストッフェル・ダルブーの公式から得られる再生核には、単に関数値を再生するだけでなく、ある点での多項式の値を最大化するという極値性がある。本記事では、この性質をコーシー・シュワルツの不等式から導く。

<div class="math-box theorem-box">

<div class="math-box-title">定理：再生核の極値性</div>

高々 $n$ 次でノルムが $1$ の実係数多項式 $\rho$ のうち、固定した点 $y\in(a,b)$ における $\lvert\rho(y)\rvert$ を最大にするものは、

$$
\rho(x)
=
\pm
\frac{K_n(x,y)}
{\sqrt{K_n(y,y)}}
$$

で与えられる。

</div>

## 1. 正規直交多項式で展開する

$\rho$ を

$$
\rho(x)
=
\sum_{k=0}^{n}
\alpha_k\phi_k(x)
$$

と展開する。正規直交性から、

$$
\lVert\rho\rVert^2
=
\sum_{k=0}^{n}
\alpha_k^2.
$$

$\lVert\rho\rVert=1$ なので、

$$
\sum_{k=0}^{n}
\alpha_k^2
=
1.
$$

点 $y$ での値は、

$$
\rho(y)
=
\sum_{k=0}^{n}
\alpha_k\phi_k(y)
$$

である。

## 2. コーシー・シュワルツの不等式

ベクトル

$$
A=
(\alpha_0,\alpha_1,\ldots,\alpha_n),
\qquad
B=
(\phi_0(y),\phi_1(y),\ldots,\phi_n(y))
$$

を考えると、

$$
\rho(y)
=
A\cdot B
$$

である。コーシー・シュワルツの不等式より、

$$
\lvert\rho(y)\rvert^2
\leq
\left(
\sum_{k=0}^{n}\alpha_k^2
\right)
\left(
\sum_{k=0}^{n}\phi_k(y)^2
\right).
$$

したがって、

$$
\lvert\rho(y)\rvert^2
\leq
K_n(y,y).
$$

## 3. 等号成立条件

等号が成立するのは、$A$ と $B$ が比例するときである。したがって、ある実数 $\lambda$ を用いて、

$$
\alpha_k
=
\lambda\phi_k(y)
$$

と書ける。このとき、

$$
\rho(x)
=
\lambda
\sum_{k=0}^{n}
\phi_k(y)\phi_k(x)
=
\lambda K_n(x,y).
$$

ノルム条件から、

$$
1
=
\lVert\rho\rVert^2
=
\lambda^2K_n(y,y)
$$

なので、

$$
\lambda
=
\pm
\frac{1}{\sqrt{K_n(y,y)}}.
$$

したがって、

$$
\rho(x)
=
\pm
\frac{K_n(x,y)}
{\sqrt{K_n(y,y)}}.
$$

## 4. リーマン写像とのつながり

さらに、この「ノルムを固定したときに一点での値を最大化する」という性質を複素領域へ拡張し、リーマン写像と再生核の関係を考える。

[リーマンの写像定理と直交多項式](/articles/riemann-mapping-orthogonal-polynomials.html)
