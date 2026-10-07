---
layout: article
title: "確定特異点を持つ線形系と固有値"
seo_title: "確定特異点を持つ線形系と固有値｜超幾何関数"
description: "行列による線形微分方程式、係数行列のべき級数、固有値・固有ベクトルと逆行列の条件を整理します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
---

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：確定特異点を持つ線形系（Linear System）</div>

ノートの第4-1節では、行列による方程式

$$
\frac{dX}{dz}=\frac1z A(z)X
$$

を考える。$X$ は $n$ 次元の列ベクトル、$A(z)$ は解析関数を成分とする $n\times n$ 行列で、

$$
A(z)=\sum_{k=0}^{\infty}A_kz^k
=A_0+A_1z+A_2z^2+\cdots
$$

と展開する。ノートでは、特異点が消えないように $A_0\neq0$ と仮定している。

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

## 続けて読む

[← 3つの確定特異点とフックスの関係式](/articles/hypergeometric-three-singularities.html)

[線形系の級数解と係数ベクトルの漸化式 →](/articles/hypergeometric-matrix-series-solutions.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)

出典ノート：『超幾何方程式.pdf』5〜6ページ。
