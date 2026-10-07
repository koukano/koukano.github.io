---
layout: article
title: "ガンマ関数の対数微分：ディガンマ関数（Digamma Function）"
seo_title: "ディガンマ関数とは？ガンマ関数の対数微分"
description: "ディガンマ関数 ψ(z)=Γ'(z)/Γ(z) の定義と基本的な表示を、ガンマ関数のワイエルシュトラス積表示から導きます。"
category: "gamma-function"
category_label: "ガンマ関数"
---

ガンマ関数の対数微分

$$
\psi(z)
=
\frac{d}{dz}\log\Gamma(z)
=
\frac{\Gamma'(z)}{\Gamma(z)}
$$

を考える。この関数は、ガンマ関数の変化率を調べる際に自然に現れる。

## 1. ワイエルシュトラス表示から導く

ワイエルシュトラスの積表示

$$
\frac{1}{\Gamma(z)}
=
ze^{\gamma z}
\prod_{n=1}^{\infty}
\left(
1+\frac{z}{n}
\right)e^{-z/n}
$$

の対数をとると、

$$
-\log\Gamma(z)
=
\log z
+
\gamma z
+
\sum_{n=1}^{\infty}
\left[
\log\left(1+\frac{z}{n}\right)
-
\frac{z}{n}
\right].
$$

両辺を $z$ で微分すると、

$$
-\psi(z)
=
\frac1z
+
\gamma
+
\sum_{n=1}^{\infty}
\left(
\frac{1}{n+z}
-
\frac1n
\right).
$$

したがって、

<div class="math-box theorem-box">

<div class="math-box-title">ディガンマ関数の級数表示（Series Representation of the Digamma Function）</div>

$z\notin\lbrace 0,-1,-2,\ldots\rbrace $ に対して、

$$
\psi(z)
=
-\gamma
+
\sum_{n=0}^{\infty}
\left(
\frac{1}{n+1}
-
\frac{1}{n+z}
\right).
$$

</div>

## 2. 極との関係

級数表示を見ると、

$$
z=0,-1,-2,\ldots
$$

で分母が $0$ になる項が現れる。これは、ガンマ関数が非正整数に極を持つことと対応している。

## 具体例：整数での値と調和数

級数表示で $z=1$ とすると、各括弧内が $0$ なので $\psi(1)=-\gamma$ である。$z=3$ では和が望遠鏡状に消えて、

$$
\begin{aligned}
\psi(3)
&=-\gamma+\lim_{N\to\infty}\sum_{n=0}^N
\left(\frac1{n+1}-\frac1{n+3}\right)\\
&=-\gamma+1+\frac12=\frac32-\gamma.
\end{aligned}
$$

一般に正整数 $m$ では $\psi(m)=H_{m-1}-\gamma$ となる。対数微分の値が、有限個の逆数の和で表される例である。

## 次の記事

[ガンマ関数と一般化二項定理](/articles/gamma-generalized-binomial-theorem.html)
