---
layout: article
title: "チェビシェフ多項式と余弦関数"
seo_title: "チェビシェフ多項式と余弦関数｜T_n(cosθ)=cos(nθ)"
description: "チェビシェフ多項式と余弦関数の関係を、微分方程式と変数変換 x=cosθ から導きます。"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

チェビシェフ多項式が満たす微分方程式は、変数を $x=\cos\phi$ と置くことで三角関数の微分方程式へ変換できる。このことから、チェビシェフ多項式と余弦関数の関係が現れる。

## 1. チェビシェフ微分方程式（Chebyshev Differential Equation）

チェビシェフ多項式に対応する微分方程式は、

$$
(1-x^2)y''-xy'+n^2y=0
$$

である。

## 2. 変数変換

$$
x=\cos\phi
$$

とおき、

$$
y(x)=Y(\phi)
$$

とする。このとき、

$$
\frac{dx}{d\phi}
=
-\sin\phi
$$

であり、

$$
\frac{d}{dx}
=
-\frac{1}{\sin\phi}
\frac{d}{d\phi}.
$$

したがって、

$$
y'
=
-\frac{1}{\sin\phi}Y'
$$

となる。さらに2階微分を計算してチェビシェフ微分方程式へ代入すると、

$$
Y''+n^2Y=0
$$

に帰着する。

## 3. 三角関数による表示

この方程式の解は、

$$
Y(\phi)
=
A\cos(n\phi)
+
B\sin(n\phi)
$$

という形になる。

$\phi=\cos^{-1}x$ であるから、

$$
y(x)
=
A\cos\left(n\cos^{-1}x\right)
+
B\sin\left(n\cos^{-1}x\right)
$$

となる。

多項式解を標準的な規格化 $T_n(1)=1$ で選ぶと、

$$
T_n(x)
=
\cos\left(n\cos^{-1}x\right)
$$

となる。したがって $[-1,1]$ 上では $|T_n(x)|\leq1$ である。具体例として $n=5$ を描くと次のようになる。

<figure class="article-figure">
  <img src="/images/figures/chebyshev-cosine.svg" alt="T5(x)=cos(5 arccos x)を区間マイナス1から1で正確に描いたグラフ">
  <figcaption>図1：$T_5(x)=\cos(5\arccos x)$ の正確なグラフ。一般に $T_n(x)=\cos(n\arccos x)$ であり、$[-1,1]$ 上で $|T_n(x)|\leq1$。<span class="figure-source">本文の公式に基づき作図。</span></figcaption>
</figure>


## 4. 微分方程式へ戻して確認する

$$
T_n(x)
=
\cos\left(n\cos^{-1}x\right)
$$

を微分し整理すると、

$$
(1-x^2)T_n''(x)
-
xT_n'(x)
+
n^2T_n(x)
=
0
$$

が得られる。したがって、この余弦表示はチェビシェフ微分方程式と一致する。

## 次の記事

[量子力学におけるエルミート多項式](/articles/hermite-polynomials-quantum-mechanics.html)
