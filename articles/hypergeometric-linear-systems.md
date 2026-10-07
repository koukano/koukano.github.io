---
layout: article
title: "確定特異点を持つ線形系：固有値・級数解・特異点の変換"
seo_title: "確定特異点を持つ線形系：固有値・級数解・特異点の変換｜超幾何関数"
description: "行列による線形微分方程式の定義から、固有値を使う級数解の係数決定と特異点の変換までを解説します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
---

行列で表される線形微分方程式を考え、固有値から級数解の係数を順に求めよう。その後、無限遠点と特異点の変換を調べる。

## この記事の目次

- [確定特異点を持つ線形系と固有値](#linear-systems)
- [線形系の級数解と係数ベクトルの漸化式](#matrix-series-solutions)
- [線形系の無限遠点と3つの特異点の変換](#matrix-singularities)

<h2 id="linear-systems">確定特異点を持つ線形系と固有値</h2>

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：確定特異点を持つ線形系（Linear System）</div>

行列による方程式

$$
\frac{dX}{dz}=\frac1z A(z)X
$$

を考える。$X$ は $n$ 次元の列ベクトル、$A(z)$ は解析関数を成分とする $n\times n$ 行列で、

$$
A(z)=\sum_{k=0}^{\infty}A_kz^k
=A_0+A_1z+A_2z^2+\cdots
$$

と展開する。特異点が消えないように $A_0\neq0$ と仮定している。

</div>

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：固有値と固有ベクトル（Eigenvalues and Eigenvectors）</div>

$A_0\in M_n(\mathbb C)$ に対し、非零ベクトル $X_0$ と数 $\mu$ が

$$
A_0X_0=\mu X_0,\qquad X_0\neq0
$$

を満たすとき、$\mu$ を固有値、$X_0$ を対応する固有ベクトルという。

</div>

<div class="math-box lemma-box" markdown="1">

<div class="math-box-title">補題：逆行列が存在する条件</div>

$\mu+k$ が $A_0$ の固有値でなければ、$((\mu+k)I-A_0)$ は逆行列を持つ。

</div>

<h2 id="matrix-series-solutions">線形系の級数解と係数ベクトルの漸化式</h2>

[線形系の定義](/articles/hypergeometric-linear-systems.html#linear-systems)にある $dX/dz=A(z)X/z$、$A(z)=\sum_{k=0}^{\infty}A_kz^k$ を考える。解を

$$
X=z^{\mu}\sum_{k=0}^{\infty}z^kX_k
$$

の形に求める。左辺と右辺を展開すると、

$$
\begin{aligned}
\frac{dX}{dz}
&=z^{\mu-1}\sum_{k=0}^{\infty}(k+\mu)z^kX_k,\\
\frac1zA(z)X
&=z^{\mu-1}\sum_{k=0}^{\infty}z^k
\sum_{\ell=0}^{k}A_{\ell}X_{k-\ell}.
\end{aligned}
$$

<div class="math-box proposition-box" markdown="1">

<div class="math-box-title">命題：ベクトルの級数解の係数比較</div>

係数を比較すれば、単位行列を $I$ として、

$$
\begin{aligned}
(\mu I-A_0)X_0&=0,\\
((\mu+k)I-A_0)X_k
&=\sum_{\ell=1}^{k}A_{\ell}X_{k-\ell},
\qquad k\geq1.
\end{aligned}
$$

</div>

ここで、$\mu$ を $A_0$ の固有値とすると、最初の式を満たす非零ベクトル $X_0$ が存在する。固有値・固有ベクトルは

$$
A_0X_0=\mu X_0,\qquad X_0\neq0
$$

という関係で定義される。

$\mu+k$ が $A_0$ の固有値でなければ、$((\mu+k)I-A_0)$ は逆行列を持つ。例えば、

$$
X_1=((\mu+1)I-A_0)^{-1}A_1X_0.
$$

同様に、各 $k\geq1$ についてこの条件が成り立つ場合、$X_k$ を順に求めることができる。

<h2 id="matrix-singularities">線形系の無限遠点と3つの特異点の変換</h2>

<div class="math-box proposition-box" markdown="1">

<div class="math-box-title">命題：線形系の無限遠点の変換</div>

線形系 $dX/dz=A(z)X/z$ で $z=1/t$ と変換すると、

$$
\frac{dX}{dt}=-\frac1t A(1/t)X.
$$

$z=0$ のほかに $z=\infty$ も確定特異点となる場合を調べよう。ここでは、$A$ が定数行列となる形を考える。

</div>

### 3つの有限特異点を移す

さらに、有限の3点 $0,1,a$ を扱う場合には、

$$
\frac{dX}{dz}=\frac{A(z)}{z(z-1)(z-a)}X
$$

と書く。無限遠が確定特異点でない場合には、

$$
A(z)=A_0+A_1z
$$

という1次の形を得ている。また、

$$
z=\frac{at}{t+(a-1)}
$$

という変換を用いて、特異点を $t=0,1,\infty$ に移す。

## 続けて読む

[← 確定特異点とフロベニウス法：特性指数・対数解・フックスの関係式](/articles/hypergeometric-frobenius-solutions.html)

[線形系から2階方程式へ：未知関数の消去と無限遠の条件 →](/articles/hypergeometric-system-elimination.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)
