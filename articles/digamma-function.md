---
layout: article
title: "ガンマ関数の対数微分：ディガンマ関数"
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

<div class="math-box-title">ディガンマ関数の級数表示</div>

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

## 次の記事

[ガンマ関数と一般化二項定理](/articles/gamma-generalized-binomial-theorem.html)
