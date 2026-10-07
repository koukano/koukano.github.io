---
layout: article
title: "2成分の線形系から2階微分方程式を導く"
seo_title: "2成分の線形系から2階微分方程式を導く｜超幾何関数"
description: "2×2の係数行列を持つ線形系から一方の未知関数を消去し、2階方程式の係数を求めます。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
---

線形系から2階微分方程式を導いてみよう。$X=(y,u)^{\mathsf T}$、係数行列を

$$
A(z)=\begin{pmatrix}a(z)&b(z)\\c(z)&d(z)\end{pmatrix}
$$

と書くと、

$$
zy'=ay+bu,
\qquad
zu'=cy+du.
$$

第1式から $u$ を消去する。$b(z)\neq0$ として

$$
u=\frac{zy'-ay}{b}
$$

とおき、微分して

$$
u'=\frac{bz\,y''+(b-ab-zb')y'+(ab'-a'b)y}{b^2}
$$

を得る。これを第2式に代入すると、

$$
\begin{aligned}
&bz^2y''+z(b-ab-zb'-bd)y'\\
&\qquad +(zab'-za'b-b^2c+abd)y=0.
\end{aligned}
$$

<div class="math-box proposition-box" markdown="1">

<div class="math-box-title">命題：2成分の線形系から得られる2階方程式</div>

したがって、次の形に整理できる。

$$
y''+\frac{\mathcal P(z)}z y'
+\frac{\mathcal Q(z)}{z^2}y=0,
$$

ただし、係数をまとめる記号を $\mathcal P,\mathcal Q$ として、

$$
\mathcal P(z)=\frac{b-ab-zb'-bd}{b},
\qquad
\mathcal Q(z)=\frac{zab'-za'b-b^2c+abd}{b}.
$$

である。

</div>

## 続けて読む

[← 線形系の無限遠点と3つの特異点の変換](/articles/hypergeometric-matrix-singularities.html)

[部分分数と無限遠の条件：係数の相殺に注意 →](/articles/hypergeometric-partial-fractions.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)
