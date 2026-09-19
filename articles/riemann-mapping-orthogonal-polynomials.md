---
layout: article
title: "リーマンの写像定理と直交多項式"
category: "special-functions"
category_label: "特殊関数"
---

リーマンの写像定理は、複素解析における重要な定理の一つであり、複素平面上の広いクラスの領域を単位円板へ等角に写せることを主張する。本記事では、まずリーマンの写像定理を確認し、その後、領域の境界曲線上に正規直交多項式と再生核を導入する。最終的には、再生核を用いてリーマン写像関数を表す方法を考える。

## 1. 等角写像

<div class="math-box definition-box">

<div class="math-box-title">定義：等角写像</div>

写像 $f$ が点 $z_0$ において交わる任意の2曲線のなす角を保つとき、$f$ を $z_0$ における等角写像という。

</div>

複素解析では、正則関数 $f$ が点 $z_0$ において

$$
f'(z_0)\neq 0
$$

を満たせば、$f$ は $z_0$ の近傍で角度を保つ。したがって、微分が $0$ にならない正則写像は局所的に等角写像となる。

## 2. リーマンの写像定理

単位円板を

$$
\mathbb{D}
=
\left\{
z\in\mathbb{C}
\mid
\lvert z\rvert<1
\right\}
$$

とする。

<div class="math-box theorem-box">

<div class="math-box-title">定理：リーマンの写像定理</div>

$D\subsetneq\mathbb{C}$ を単連結領域とする。このとき、$D$ から単位円板 $\mathbb{D}$ への正則な全単射写像

$$
\gamma:D\longrightarrow\mathbb{D}
$$

が存在する。さらに、$a\in D$ を固定し、

$$
\gamma(a)=0,
\qquad
\gamma'(a)>0
$$

という正規化条件を課すと、$\gamma$ は一意に定まる。

</div>

リーマンの写像定理の証明は[こちら](/articles/riemann-mapping-theorem-proof.html)で詳しく扱う。

この定理は、単連結な真部分領域が正則写像という観点では単位円板と同じ複素解析的構造を持つことを意味している。領域そのものの形が単純になるのではなく、複雑な形をした領域であっても、それを単位円板へ等角に写す正則関数 $\gamma$ が存在するという主張である。

## 3. 境界曲線上の内積

ここから、リーマン写像と直交多項式を結びつけるために、複素平面上の曲線に沿って多項式の内積を定義する。$C$ を複素平面上の自己交叉を持たない曲線とし、

$$
z=z(t),
\qquad
a\leq t\leq b
$$

によって表されるものとする。また、$w(t)\geq0$ を重み関数とする。

<div class="math-box definition-box">

<div class="math-box-title">定義：曲線上の内積</div>

複素係数多項式 $f,g\in\mathbb{C}[z]$ に対して、

$$
\langle f,g\rangle
=
\int_a^b
w(t)
f(z(t))
\overline{g(z(t))}
\lvert z'(t)\rvert\,dt
$$

と定める。

</div>

曲線 $C$ の弧長パラメータを $s$ とすれば、

$$
ds
=
\lvert z'(t)\rvert\,dt
$$

であるから、内積は

$$
\langle f,g\rangle
=
\int_C
w(s)
f(z)
\overline{g(z)}
\,ds
$$

と書くことができる。この内積によって、多項式同士の直交性を境界曲線 $C$ 上で考えることができる。

## 4. 境界曲線上の正規直交多項式

<div class="math-box definition-box">

<div class="math-box-title">定義：正規直交多項式</div>

曲線 $C$ 上の多項式列

$$
\phi_0(z),
\phi_1(z),
\phi_2(z),
\ldots
$$

が

$$
\langle\phi_i,\phi_j\rangle
=
\delta_{ij}
$$

を満たすとき、$\{\phi_n\}_{n=0}^{\infty}$ を曲線 $C$ 上の正規直交多項式系という。ここで、

$$
\delta_{ij}
=
\begin{cases}
1 & (i=j),\\
0 & (i\neq j)
\end{cases}
$$

である。

</div>

つまり、異なる次数の多項式は互いに直交し、それぞれのノルムは $1$ になるように正規化されている。

## 5. 再生核

正規直交多項式を用いて、次の関数を定義する。

<div class="math-box definition-box">

<div class="math-box-title">定義：再生核</div>

正規直交多項式系 $\{\phi_k\}$ に対して、

$$
K_n(a,z)
=
\sum_{k=0}^{n}
\overline{\phi_k(a)}
\phi_k(z)
$$

を $n$ 次の再生核という。

</div>

$p(z)$ を高々 $n$ 次の多項式とすると、

$$
p(z)
=
\sum_{k=0}^{n}
c_k\phi_k(z)
$$

と展開できる。このとき、

$$
\langle p,K_n(a,\cdot)\rangle
=
p(a)
$$

が成り立つ。この性質は、曲線全体にわたる内積から一点 $a$ における値 $p(a)$ を再現できることを意味しており、そのため $K_n$ は再生核と呼ばれる。

## 6. 再生核の基本的な不等式

再生核にコーシー・シュワルツの不等式を適用すると、

$$
\lvert K_n(a,z)\rvert^2
\leq
K_n(a,a)K_n(z,z)
$$

が得られる。実際、

$$
K_n(a,z)
=
\sum_{k=0}^{n}
\overline{\phi_k(a)}
\phi_k(z)
$$

であるから、

$$
\lvert K_n(a,z)\rvert^2
=
\left|
\sum_{k=0}^{n}
\overline{\phi_k(a)}
\phi_k(z)
\right|^2
$$

となり、コーシー・シュワルツの不等式によって

$$
\lvert K_n(a,z)\rvert^2
\leq
\left(
\sum_{k=0}^{n}
\lvert\phi_k(a)\rvert^2
\right)
\left(
\sum_{k=0}^{n}
\lvert\phi_k(z)\rvert^2
\right)
$$

を得る。右辺はそれぞれ $K_n(a,a)$ と $K_n(z,z)$ であるため、

$$
\lvert K_n(a,z)\rvert^2
\leq
K_n(a,a)K_n(z,z)
$$

が成り立つ。

## 7. 正規化された再生核

次の関数を考える。

$$
G_n(z)
=
\varepsilon
\frac{K_n(a,z)}
{\sqrt{K_n(a,a)}},
\qquad
\lvert\varepsilon\rvert=1.
$$

再生核の性質から、

$$
\lVert G_n\rVert^2=1
$$

が成り立つ。また、高々 $n$ 次でノルムが $1$ の多項式 $p$ を考えると、$|p(a)|$ を最大にする多項式は、絶対値 $1$ の定数倍を除いて、再生核を正規化した形で与えられる。この極値性は、再生核とリーマン写像を結びつけるうえで重要な役割を果たす。

## 8. 正則関数の平均値公式

リーマン写像と再生核を結びつける準備として、正則関数の平均値公式を確認する。

<div class="math-box theorem-box">

<div class="math-box-title">定理：正則関数の平均値公式</div>

$f$ を領域 $D$ 上の正則関数とし、$a\in D$ とする。$a$ を中心とする半径 $r$ の閉円板が $D$ に含まれるとき、

$$
f(a)
=
\frac{1}{2\pi}
\int_0^{2\pi}
f(a+re^{i\theta})
\,d\theta
$$

が成り立つ。

</div>

### 証明

コーシーの積分公式より、

$$
f(a)
=
\frac{1}{2\pi i}
\int_{\lvert\xi-a\rvert=r}
\frac{f(\xi)}
{\xi-a}
\,d\xi
$$

が成り立つ。ここで、

$$
\xi
=
a+re^{i\theta}
$$

とおくと、

$$
d\xi
=
ire^{i\theta}\,d\theta
$$

であるから、

$$
f(a)
=
\frac{1}{2\pi i}
\int_0^{2\pi}
\frac{f(a+re^{i\theta})}
{re^{i\theta}}
ire^{i\theta}
\,d\theta
$$

となる。したがって、

$$
f(a)
=
\frac{1}{2\pi}
\int_0^{2\pi}
f(a+re^{i\theta})
\,d\theta
$$

を得る。

## 9. 再生核によるリーマン写像

ここから、正規直交多項式から構成した再生核とリーマン写像との関係を考える。$D$ を有界な単連結領域とし、$C=\partial D$ をその境界曲線とする。また、$a\in D$ を固定し、

$$
\gamma(a)=0,
\qquad
\gamma'(a)>0
$$

を満たす $D$ から単位円板へのリーマン写像を $\gamma$ とする。

<div class="math-box theorem-box">

<div class="math-box-title">定理：再生核によるリーマン写像の表示</div>

境界 $C$ に十分な正則性があり、境界上の正規直交多項式から作られる再生核 $K_n(a,z)$ が対応する再生核へ収束するための条件を満たしているとする。このとき、リーマン写像 $\gamma$ は

$$
\gamma(z)
=
\lim_{n\to\infty}
\frac{2\pi}
{K_n(a,a)}
\int_a^z
K_n(a,\xi)^2
\,d\xi
$$

によって表される。

</div>

この公式は、幾何学的に定義されるリーマン写像を、境界上の正規直交多項式と再生核を用いて構成できることを示している。なお、有限次の再生核 $K_n$ から極限へ移るためには境界の正則性や近似に関する仮定が必要であり、任意の単純閉曲線に対して無条件に成り立つと考えるべきではない。

## 10. 再生核の極限

有限次の再生核から極限関数

$$
K(a,z)
=
\lim_{n\to\infty}
K_n(a,z)
$$

を考える。コーシー・シュワルツの不等式から、

$$
\lvert K_n(a,z)\rvert^2
\leq
K_n(a,a)K_n(z,z)
$$

が成り立つ。適切な仮定のもとでは、$K_n(a,z)$ は領域 $D$ のコンパクト部分集合上で局所有界となり、正則関数列として極限関数 $K(a,z)$ を考えることができる。同様に、

$$
G(z)
=
\lim_{n\to\infty}
\frac{K_n(a,z)}
{\sqrt{K_n(a,a)}}
$$

という正規化された極限も考えることができる。

## 11. リーマン写像の逆関数

リーマン写像

$$
\gamma:D\longrightarrow\mathbb{D}
$$

の逆関数を

$$
g=\gamma^{-1}
$$

とする。境界上で

$$
\gamma(z(s))
=
e^{i\theta}
$$

と表せる場合、

$$
\lvert d\gamma\rvert
=
\lvert\gamma'(z)\rvert\,ds
=
d\theta
$$

となる。また、

$$
\gamma'(z)g'(\gamma(z))=1
$$

であるから、

$$
ds
=
\lvert g'(e^{i\theta})\rvert\,d\theta
$$

と書ける。この変数変換によって、境界曲線 $C$ 上の積分を単位円周上の積分へ移すことができる。

## 12. $K_n(a,a)$ と $\gamma'(a)$ の関係

極限再生核とリーマン写像の間には、

$$
\lim_{n\to\infty}
K_n(a,a)
=
\frac{\gamma'(a)}
{2\pi}
$$

という関係が現れる。この等式は、再生核の点 $a$ における値が、正規化されたリーマン写像の微分係数と直接結びついていることを示している。

## 13. リーマン写像の微分

さらに再生核の極限を用いると、

$$
\gamma'(z)
=
\lim_{n\to\infty}
\frac{2\pi}
{K_n(a,a)}
K_n(a,z)^2
$$

という表示が得られる。$\gamma(a)=0$ であることに注意して $a$ から $z$ まで積分すると、

$$
\gamma(z)
=
\int_a^z
\gamma'(\xi)
\,d\xi
$$

であるから、

$$
\gamma(z)
=
\lim_{n\to\infty}
\frac{2\pi}
{K_n(a,a)}
\int_a^z
K_n(a,\xi)^2
\,d\xi
$$

を得る。これが、正規直交多項式から構成された再生核によるリーマン写像の表示である。

## 14. 単位円板の場合

具体例として、領域そのものが単位円板である場合を考える。境界曲線を

$$
C:
z(s)=e^{is},
\qquad
0\leq s\leq2\pi
$$

とし、重み関数を

$$
w(s)=1
$$

とする。このとき、

$$
\phi_k(z)
=
\frac{1}{\sqrt{2\pi}}z^k
$$

とおけば、

$$
\langle\phi_j,\phi_k\rangle
=
\frac{1}{2\pi}
\int_0^{2\pi}
e^{i(j-k)s}
\,ds
=
\delta_{jk}
$$

となるため、$\{\phi_k\}_{k=0}^{\infty}$ は正規直交多項式系である。

## 15. 単位円板の再生核

単位円板の場合、極限再生核は

$$
K(a,z)
=
\sum_{k=0}^{\infty}
\overline{\phi_k(a)}
\phi_k(z)
$$

であるから、

$$
K(a,z)
=
\frac{1}{2\pi}
\sum_{k=0}^{\infty}
(\overline{a}z)^k
$$

となる。$\lvert a\rvert<1$、$\lvert z\rvert<1$ であるため、等比級数の公式から、

$$
K(a,z)
=
\frac{1}
{2\pi(1-\overline{a}z)}
$$

を得る。

## 16. 単位円板のリーマン写像

この再生核をリーマン写像の公式に代入すると、

$$
\gamma(z)
=
\frac{z-a}
{1-\overline{a}z}
$$

が得られる。これは単位円板を単位円板へ写す一次分数変換であり、

$$
\gamma(a)=0
$$

を満たす。また、

$$
\gamma'(a)
=
\frac{1}{1-\lvert a\rvert^2}
>0
$$

であるため、ここで課した正規化条件も満たしている。

## 17. まとめ

リーマンの写像定理は、単連結な真部分領域 $D\subsetneq\mathbb{C}$ が単位円板と等角同値であることを保証する。一方、境界曲線 $C=\partial D$ 上に内積を導入すると、正規直交多項式系 $\{\phi_n\}$ を構成でき、それらから再生核

$$
K_n(a,z)
=
\sum_{k=0}^{n}
\overline{\phi_k(a)}
\phi_k(z)
$$

を定義できる。

適切な正則性と収束の仮定のもとでは、この再生核は

$$
\gamma(z)
=
\lim_{n\to\infty}
\frac{2\pi}
{K_n(a,a)}
\int_a^z
K_n(a,\xi)^2
\,d\xi
$$

という形でリーマン写像と結びつく。この結果は、直交多項式という代数的・解析的な対象から、領域の幾何学的情報を持つリーマン写像を構成できることを示している。
