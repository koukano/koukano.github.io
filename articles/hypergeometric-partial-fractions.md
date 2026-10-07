---
layout: article
title: "部分分数と無限遠の条件：係数の相殺に注意"
seo_title: "部分分数と無限遠の条件：係数の相殺に注意｜超幾何関数"
description: "部分分数で書かれた2階方程式を無限遠で調べ、係数の組合せの解析性と個別の定数性を区別します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
  - "NIST, <a href=\"https://dlmf.nist.gov/2.7#i\">Digital Library of Mathematical Functions: Regular Singularities: Fuchs–Frobenius Theory</a>."
---

ノートでは、部分分数による2階方程式の形を

$$
y''+\left(\frac{P_0(z)}z+\frac{P_1(z)}{z-1}\right)y'
+\left(\frac{Q_0(z)}{z^2}
+\frac{Q_1(z)}{(z-1)^2}
+\frac{Q_2(z)}{z(z-1)}\right)y=0
$$

と書き、$P_0,P_1,Q_0,Q_1,Q_2$ を整関数としている。

$z=1/t$、$Y(t)=y(1/t)$ とすると、ノートの書き直された計算では、

$$
\frac{dy}{dz}=-t^2\frac{dY}{dt},
\qquad
\frac{d^2y}{dz^2}=t^4\frac{d^2Y}{dt^2}
+2t^3\frac{dY}{dt}
$$

を用いている。変換後の方程式は

$$
\begin{aligned}
Y''&+\frac1t\left(2-P_0(1/t)
-\frac{P_1(1/t)}{1-t}\right)Y'\\
&+\frac1{t^2}\left(Q_0(1/t)
+\frac{Q_1(1/t)}{(1-t)^2}
+\frac{Q_2(1/t)}{1-t}\right)Y=0.
\end{aligned}
$$

<div class="math-box proposition-box" markdown="1">

<div class="math-box-title">命題：無限遠で解析的となる係数の組合せ</div>

ノートでは、無限遠が確定特異点であるために、次の2つの組合せが $t=0$ で解析的となる条件を調べている。

$$
2-P_0(1/t)-\frac{P_1(1/t)}{1-t},
$$

$$
Q_0(1/t)+\frac{Q_1(1/t)}{(1-t)^2}
+\frac{Q_2(1/t)}{1-t}.
$$

</div>

## 個々の係数の定数性とは区別する

原ノート末尾の「各係数が定数になる」という結論は、上の組合せの解析性から個別の定数性を導いている。この推論には、係数同士の相殺を除外する条件が不足している。


<div class="math-box proposition-box" markdown="1">

<div class="math-box-title">命題：組合せの解析性だけでは個別の定数性は従わない</div>

$P_0(z)=z+1$、$P_1(z)=3-z$ とおくと、どちらも非定数の整関数であるが、

$$
\frac{P_0(z)}z+\frac{P_1(z)}{z-1}
=\frac1z+\frac2{z-1}.
$$

無限遠の判定に用いる組合せも

$$
2-P_0(1/t)-\frac{P_1(1/t)}{1-t}
=-\frac{1+t}{1-t}
$$

となり、$t=0$ で解析的である。したがって、この条件から $P_0,P_1$ がそれぞれ定数だとは結論できない。

</div>

この計算は原ノート末尾の推論を検証するための補足である。確定特異点の判定は NIST DLMF §2.7(i) と照合した。定数を選んで同じ係数を表すことはできても、任意の分解に現れる各関数が定数であることとは区別する。

## 続けて読む

[← 2成分の線形系から2階微分方程式を導く](/articles/hypergeometric-system-elimination.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)

出典ノート：『超幾何方程式.pdf』9〜10（バツの範囲を除外）ページ。
