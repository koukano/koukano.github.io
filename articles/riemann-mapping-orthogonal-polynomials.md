---
layout: article
title: "再生核によるリーマン写像の表示"
seo_title: "再生核によるリーマン写像の表示｜直交多項式との関係"
description: "境界上の正規直交多項式から作る再生核を用いて、リーマン写像を復元する表示とその条件を解説します。"
category: "orthogonal-polynomials"
category_label: "直交多項式"
---

境界上の正規直交多項式から作られる再生核は、適切な仮定のもとでリーマン写像を復元できる。本記事では、この定理だけを扱い、PDFで用いている極値問題の考え方に沿って証明する。

## 1. 設定

$D\subset\mathbb{C}$ を有界な単連結領域とし、$C=\partial D$ を十分正則な単純閉曲線とする。$a\in D$ を固定し、

$$
\gamma:D\longrightarrow\mathbb{D}
$$

を

$$
\gamma(a)=0,
\qquad
\gamma'(a)>0
$$

で正規化されたリーマン写像とする。

境界 $C$ 上の弧長測度 $ds$ に関する内積を

$$
\langle f,g\rangle
=
\int_C
f(z)\overline{g(z)}\,ds
$$

とし、正規直交多項式系を

$$
\phi_0,\phi_1,\phi_2,\ldots
$$

とする。

有限次の再生核を

$$
K_n(a,z)
=
\sum_{k=0}^{n}
\overline{\phi_k(a)}\phi_k(z)
$$

と定める。

以下では、境界の正則性と多項式の完備性により

$$
K_n(a,z)\longrightarrow K(a,z)
$$

が $D$ のコンパクト部分集合上一様に成り立つものとする。

<div class="math-box theorem-box">

<div class="math-box-title">定理：再生核によるリーマン写像の表示</div>

上の仮定のもとで、

$$
\gamma(z)
=
\lim_{n\to\infty}
\frac{2\pi}{K_n(a,a)}
\int_a^z
K_n(a,\xi)^2\,d\xi
$$

が成り立つ。

</div>

## 2. 再生核の極値性

高々 $n$ 次の多項式 $p$ について、

$$
p(a)
=
\langle p,K_n(a,\cdot)\rangle
$$

が成り立つ。

したがってコーシー・シュワルツの不等式から、

$$
|p(a)|^2
\leq
\|p\|^2 K_n(a,a).
$$

特に $\|p\|=1$ のとき、

$$
|p(a)|^2
\leq
K_n(a,a).
$$

等号は

$$
p(z)
=
\varepsilon
\frac{K_n(a,z)}
{\sqrt{K_n(a,a)}},
\qquad
|\varepsilon|=1
$$

のときに達成される。

つまり、正規化された再生核は、ノルムが $1$ の多項式の中で点 $a$ における絶対値を最大にする。

## 3. 単位円板へ移す

$g=\gamma^{-1}$ とする。$g$ は単位円板上で正則かつ単葉で、

$$
g(0)=a,
\qquad
g'(0)=\frac{1}{\gamma'(a)}
$$

を満たす。

$D$ 上の正則関数 $G$ に対して、

$$
F(\zeta)
=
G(g(\zeta))
\sqrt{g'(\zeta)}
$$

とおく。$g'$ は単位円板上で零点を持たないので、平方根の正則な分枝を選ぶことができる。

境界上で $\zeta=e^{i\theta}$ とすると、

$$
ds
=
|g'(e^{i\theta})|\,d\theta
$$

であるから、

$$
\int_C |G(z)|^2\,ds
=
\int_0^{2\pi}
|F(e^{i\theta})|^2\,d\theta.
$$

したがって、$G$ の境界 $L^2$ ノルムが $1$ ならば、

$$
\int_0^{2\pi}
|F(e^{i\theta})|^2\,d\theta
=
1.
$$

## 4. 点 $a$ における最大値

$F$ を

$$
F(\zeta)
=
\sum_{j=0}^{\infty}
c_j\zeta^j
$$

と展開する。

パーセヴァルの等式から、

$$
2\pi
\sum_{j=0}^{\infty}|c_j|^2
=
1.
$$

したがって、

$$
|F(0)|^2
=
|c_0|^2
\leq
\frac{1}{2\pi}.
$$

等号は

$$
c_1=c_2=\cdots=0
$$

すなわち $F$ が定数のときに限って成り立つ。

一方、

$$
F(0)
=
G(a)\sqrt{g'(0)}
$$

なので、

$$
|G(a)|^2
=
\frac{|F(0)|^2}{|g'(0)|}
\leq
\frac{\gamma'(a)}{2\pi}.
$$

よって、境界ノルムが $1$ の正則関数の中で点 $a$ における値の最大値は

$$
\sqrt{\frac{\gamma'(a)}{2\pi}}
$$

である。

再生核の極値性と $K_n\to K$ を用いると、

$$
K(a,a)
=
\frac{\gamma'(a)}{2\pi}.
$$

## 5. 極限再生核を求める

極値を達成する正規化された極限再生核

$$
G(z)
=
\frac{K(a,z)}
{\sqrt{K(a,a)}}
$$

を考える。

このとき対応する $F$ は等号を達成するため、

$$
F(\zeta)
=
\frac{1}{\sqrt{2\pi}}
$$

と選べる。

したがって、

$$
G(g(\zeta))
\sqrt{g'(\zeta)}
=
\frac{1}{\sqrt{2\pi}}.
$$

$\zeta=\gamma(z)$ とおくと、

$$
g'(\gamma(z))
=
\frac{1}{\gamma'(z)}
$$

なので、

$$
G(z)
=
\sqrt{
\frac{\gamma'(z)}
{2\pi}
}.
$$

よって、

$$
\frac{K(a,z)}
{\sqrt{K(a,a)}}
=
\sqrt{
\frac{\gamma'(z)}
{2\pi}
}.
$$

さらに

$$
K(a,a)
=
\frac{\gamma'(a)}
{2\pi}
$$

だから、

$$
K(a,z)^2
=
\frac{
\gamma'(a)\gamma'(z)
}
{4\pi^2}.
$$

したがって、

$$
\gamma'(z)
=
\frac{2\pi}{K(a,a)}
K(a,z)^2.
$$

## 6. 積分してリーマン写像を得る

$\gamma(a)=0$ なので、

$$
\gamma(z)
=
\int_a^z
\gamma'(\xi)\,d\xi.
$$

上の式を代入すると、

$$
\gamma(z)
=
\frac{2\pi}{K(a,a)}
\int_a^z
K(a,\xi)^2\,d\xi.
$$

さらに

$$
K_n(a,z)\to K(a,z),
\qquad
K_n(a,a)\to K(a,a)
$$

を用いると、

$$
\gamma(z)
=
\lim_{n\to\infty}
\frac{2\pi}{K_n(a,a)}
\int_a^z
K_n(a,\xi)^2\,d\xi
$$

を得る。
<div class="proof-end">\(\square\)</div>

## 注意

この表示では、有限次の再生核 $K_n$ が極限再生核へ収束するための仮定が必要である。任意の単純閉曲線に対して無条件にこの極限表示が成り立つ、という意味ではない。

## 関連記事

- [リーマンの写像定理の証明](/articles/riemann-mapping-theorem-proof.html)
- [正則関数の平均値公式](/articles/holomorphic-mean-value-formula.html)
