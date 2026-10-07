---
layout: article
title: "線形系の級数解と係数ベクトルの漸化式"
seo_title: "線形系の級数解と係数ベクトルの漸化式｜超幾何関数"
description: "X=z^μΣz^kX_k を代入して係数を比較し、固有値を用いて係数ベクトルを順に決める方法を整理します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
---

[線形系の定義](/articles/hypergeometric-linear-systems.html)にある $dX/dz=A(z)X/z$、$A(z)=\sum_{k=0}^{\infty}A_kz^k$ を考える。解を

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

同様に、各 $k\geq1$ についてこの条件が成り立つ場合、$X_k$ を順に求めることができる。ノートでは、この係数決定に続いて級数の収束領域を検討している。

## 続けて読む

[← 確定特異点を持つ線形系と固有値](/articles/hypergeometric-linear-systems.html)

[線形系の無限遠点と3つの特異点の変換 →](/articles/hypergeometric-matrix-singularities.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)

出典ノート：『超幾何方程式.pdf』5〜6ページ。
