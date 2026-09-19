---
layout: article
title: "ヤコビ多項式の零点と静電気学的解釈"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

ヤコビ多項式の零点は、区間 $(-1,1)$ に置かれた点電荷の平衡位置として解釈することができる。本記事では、零点を未知の電荷位置と考え、平衡条件からヤコビ微分方程式が現れることを確認する。

## 1. 点電荷の配置

区間 $(-1,1)$ に $n$ 個の単位電荷を

$$
x_1,x_2,\ldots,x_n
$$

と配置する。また、端点 $x=1$ と $x=-1$ に固定電荷を置き、それぞれの強さを $p,q$ とする。

配置に対応する量として、

$$
T
=
\prod_{k=1}^{n}
(1-x_k)^p
(1+x_k)^q
\prod_{1\leq j<k\leq n}
|x_j-x_k|
$$

を考える。平衡状態では、この量から得られるポテンシャルに対して各 $x_k$ で停留条件が成り立つ。

## 2. 平衡条件

$\log T$ を $x_k$ で微分すると、

$$
\frac{p}{x_k-1}
+
\frac{q}{x_k+1}
+
\sum_{j\neq k}
\frac{1}{x_k-x_j}
=
0
$$

という形の条件を得る。

## 3. 零点を持つ多項式

零点 $x_1,\ldots,x_n$ を持つ多項式

$$
f(x)
=
\prod_{j=1}^{n}
(x-x_j)
$$

を考える。

$x_k$ を1つ固定し、

$$
f(x)
=
(x-x_k)g(x)
$$

と書くと、

$$
f'(x_k)=g(x_k),
\qquad
f''(x_k)=2g'(x_k)
$$

である。したがって、

$$
\frac12
\frac{f''(x_k)}
{f'(x_k)}
=
\frac{g'(x_k)}
{g(x_k)}
=
\sum_{j\neq k}
\frac{1}{x_k-x_j}.
$$

この式を平衡条件へ代入する。

## 4. 微分方程式

各零点 $x_k$ で、

$$
(1-x_k^2)f''(x_k)
+
\left[
2(q-p)-2(p+q)x_k
\right]f'(x_k)
=
0
$$

が成り立つ。

左辺は $n$ 次以下の多項式であり、$x_1,\ldots,x_n$ のすべてを零点に持つため、ある定数 $C$ を用いて、

$$
(1-x^2)f''(x)
+
\left[
2(q-p)-2(p+q)x
\right]f'(x)
-
Cf(x)
=
0
$$

と書ける。

最高次の項を比較すると、

$$
C
=
-n(n-1+2p+2q)
$$

を得る。したがって、

$$
(1-x^2)f''
+
\left[
2(q-p)-2(p+q)x
\right]f'
+
n(n-1+2p+2q)f
=
0.
$$

## 5. ヤコビ微分方程式との比較

ヤコビ多項式の微分方程式

$$
(1-x^2)y''
+
\left[
\beta-\alpha-(\alpha+\beta+2)x
\right]y'
+
n(n+\alpha+\beta+1)y
=
0
$$

と比較すると、

$$
\alpha=2p-1,
\qquad
\beta=2q-1
$$

に対応する。

したがって、

$$
f(x)
=
C_0
P_n^{(2p-1,\,2q-1)}(x)
$$

という形になる。

<div class="math-box theorem-box">

<div class="math-box-title">零点の静電気学的解釈</div>

ヤコビ多項式 $P_n^{(2p-1,\,2q-1)}$ の零点は、区間 $(-1,1)$ に置かれた $n$ 個の単位電荷が、端点の固定電荷 $p,q$ と互いの反発のもとで平衡になる位置として解釈できる。

</div>

## 次の記事

[チェビシェフ多項式と余弦関数](/articles/chebyshev-cosine-representation.html)
