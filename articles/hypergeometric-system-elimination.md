---
layout: article
title: "線形系から2階方程式へ：未知関数の消去と無限遠の条件"
seo_title: "線形系から2階方程式へ：未知関数の消去と無限遠の条件｜超幾何関数"
description: "2成分の線形系から未知関数を消去し、2階方程式を導きます。部分分数と無限遠の解析性、係数の相殺も解説します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
  - "NIST, <a href=\"https://dlmf.nist.gov/2.7#i\">Digital Library of Mathematical Functions: Regular Singularities: Fuchs–Frobenius Theory</a>."
---

2成分の線形系から一方の未知関数を消去して、2階微分方程式を導こう。続いて部分分数による表示と無限遠の条件を調べる。

## この記事の目次

- [2成分の線形系から2階微分方程式を導く](#system-elimination)
- [部分分数と無限遠の条件：係数の相殺に注意](#partial-fractions)

<h2 id="system-elimination">2成分の線形系から2階微分方程式を導く</h2>

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

<h2 id="partial-fractions">部分分数と無限遠の条件：係数の相殺に注意</h2>

部分分数による2階方程式の形を

$$
y''+\left(\frac{P_0(z)}z+\frac{P_1(z)}{z-1}\right)y'
+\left(\frac{Q_0(z)}{z^2}
+\frac{Q_1(z)}{(z-1)^2}
+\frac{Q_2(z)}{z(z-1)}\right)y=0
$$

と書き、$P_0,P_1,Q_0,Q_1,Q_2$ を整関数としている。

$z=1/t$、$Y(t)=y(1/t)$ とすると、

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

無限遠が確定特異点であるためには、次の2つの組合せが $t=0$ で解析的となることが必要である。

$$
2-P_0(1/t)-\frac{P_1(1/t)}{1-t},
$$

$$
Q_0(1/t)+\frac{Q_1(1/t)}{(1-t)^2}
+\frac{Q_2(1/t)}{1-t}.
$$

</div>

### 個々の係数の定数性とは区別する

上の組合せが解析的であることから、各係数がそれぞれ定数になると結論してよいだろうか。係数同士の相殺が起こり得るため、この条件だけでは個別の定数性は導けない。

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

定数を選んで同じ係数を表すことはできても、任意の分解に現れる各関数が定数であることとは区別する。

## 続けて読む

[← 確定特異点を持つ線形系：固有値・級数解・特異点の変換](/articles/hypergeometric-linear-systems.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)
