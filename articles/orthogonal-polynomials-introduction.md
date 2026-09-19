---

layout: article
title: "直交多項式とは何か — 内積から正規直交多項式まで"
---


直交多項式とは、多項式同士に「内積」を定義したとき、互いに直交するように選ばれた多項式のことである。通常のベクトルでは、2つのベクトルが垂直であることを内積が $0$ になることで表すが、同じ考え方を関数や多項式にも拡張することができる。この記事では、直交多項式を定義するために必要となる線形空間、内積、ノルム、直交性を順に確認し、最後に正規直交多項式を定義する。

## 1. 線形空間

まず、直交多項式を考えるための土台となる線形空間について確認する。ここでは実数を係数とする線形空間を考える。

<div class="math-box definition-box">

<div class="math-box-title">定義：線形空間</div>

集合 $V$ に対して、任意の $a,b\in V$ と $\lambda,\mu\in\mathbb{R}$ について、和 $a+b\in V$ とスカラー倍 $\lambda a\in V$ が定義され、ベクトルの加法とスカラー倍に関する通常の演算法則を満たすとき、$V$ を実数体 $\mathbb{R}$ 上の線形空間という。

</div>

たとえば、実数を係数とする多項式全体の集合 $\mathbb{R}[x]$ は線形空間である。実際、2つの多項式を足しても再び多項式になり、多項式を実数倍しても再び多項式になる。

## 2. 内積

通常のベクトルでは、内積を使うことで2つのベクトルの長さや角度を考えることができる。同じ考え方を一般の線形空間に導入する。

<div class="math-box definition-box">

<div class="math-box-title">定義：内積</div>

実線形空間 $V$ において、任意の $f,g\in V$ に対して実数 $\langle f,g\rangle$ が定まり、次の性質を満たすとき、$\langle f,g\rangle$ を $f$ と $g$ の内積という。

$$
\langle f,g\rangle=\langle g,f\rangle
$$

$$
\langle \alpha f+\beta g,h\rangle=\alpha\langle f,h\rangle+\beta\langle g,h\rangle
$$

$$
\langle f,f\rangle\geq0,
\qquad
\langle f,f\rangle=0\iff f=0.
$$

</div>

1つ目は対称性、2つ目は線形性、3つ目は正定値性を表している。これらの性質によって、通常のベクトルの内積と同じような考え方を関数や多項式にも導入できる。

## 3. ノルム

内積を使うと、ベクトルや関数の「大きさ」に相当する量を定義できる。

<div class="math-box definition-box">

<div class="math-box-title">定義：ノルム</div>

$f\in V$ に対して、

$$
\lVert f\rVert=\sqrt{\langle f,f\rangle}
$$

によって定められる値を $f$ のノルムという。

</div>

ノルムは通常のベクトルの長さを一般化したものであり、たとえば関数同士がどの程度離れているかを $\lVert f-g\rVert$ によって測ることができる。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ノルムの基本性質</div>

任意の $f,g\in V$ と $\alpha\in\mathbb{R}$ に対して、

$$
\lVert f\rVert\geq0
$$

が成り立ち、$\lVert f\rVert=0$ となるのは $f=0$ のときに限る。また、

$$
\lVert\alpha f\rVert=\lvert\alpha\rvert\lVert f\rVert
$$

および三角不等式

$$
\lVert f+g\rVert\leq\lVert f\rVert+\lVert g\rVert
$$

が成り立つ。

</div>

## 4. 直交

ベクトルの場合、2つのベクトルが垂直であることは内積が $0$ になることによって特徴づけられる。この考え方を一般の線形空間でもそのまま利用する。

<div class="math-box definition-box">

<div class="math-box-title">定義：直交</div>

$0$ ではない $f,g\in V$ に対して、

$$
\langle f,g\rangle=0
$$

が成り立つとき、$f$ と $g$ は直交するといい、

$$
f\perp g
$$

と表す。

</div>

さらに、複数のベクトルが互いに直交し、それぞれのノルムが $1$ である場合を正規直交という。

<div class="math-box definition-box">

<div class="math-box-title">定義：正規直交</div>

$f_0,f_1,\ldots,f_n$ が互いに直交し、

$$
\lVert f_k\rVert=1
$$

をすべての $k$ について満たすとき、$f_0,f_1,\ldots,f_n$ は正規直交しているという。クロネッカーのデルタ

$$
\delta_{ij}
=
\begin{cases}
1 & (i=j),\\
0 & (i\neq j)
\end{cases}
$$

を用いると、この条件は

$$
\langle f_i,f_j\rangle=\delta_{ij}
$$

とまとめて書くことができる。

</div>

## 5. 多項式に内積を定義する

ここから多項式について考える。実数係数の多項式全体を $\mathbb{R}[x]$ とする。区間 $(a,b)$ 上で正の重み関数 $w(x)$ を選び、必要な積分が存在すると仮定する。

<div class="math-box definition-box">

<div class="math-box-title">定義：多項式の内積</div>

$f,g\in\mathbb{R}[x]$ に対して、

$$
\langle f,g\rangle
=
\int_a^b w(x)f(x)g(x)\,dx
$$

と定める。この積分によって $\mathbb{R}[x]$ 上の内積を定義する。

</div>

ここで重要なのが重み関数 $w(x)$ である。同じ多項式を考えていても、区間 $(a,b)$ や重み関数 $w(x)$ を変更すると内積が変わる。その結果、直交する多項式も変化する。

## 6. 直交多項式

多項式の内積を定義すると、異なる次数の多項式が互いに直交するような多項式列を考えることができる。

<div class="math-box definition-box">

<div class="math-box-title">定義：正規直交多項式</div>

$n$ 次多項式 $\phi_n(x)$ を

$$
\phi_n(x)=k_nx^n+\cdots,
\qquad
k_n>0
$$

とする。多項式列

$$
\phi_0(x),\phi_1(x),\phi_2(x),\ldots
$$

が

$$
\langle\phi_i,\phi_j\rangle=\delta_{ij}
$$

を満たすとき、${\phi_n(x)}_{n=0}^{\infty}$ を正規直交多項式系という。

</div>

つまり、

$$
\langle\phi_i,\phi_j\rangle=0
\qquad(i\neq j)
$$

であり、それぞれについて

$$
\lVert\phi_n\rVert=1
$$

となるように多項式を選んでいる。

## 7. 直交多項式のイメージ

通常の空間で $(1,0)$ と $(0,1)$ が直交しているように、関数の空間でも内積が $0$ となる関数同士を「直交している」と考える。直交多項式は、無限に多くの多項式が存在する空間の中から、互いに直交するように整理された多項式列と見ることができる。

特に

$$
1,\quad x,\quad x^2,\quad x^3,\ldots
$$

という通常の多項式列は一般には互いに直交していないが、これらを内積に関して直交するように組み替えることで、正規直交多項式系を構成することができる。このような多項式系は、関数近似、積分公式、微分方程式などさまざまな場面に現れる。

## 8. ここまでのまとめ

直交多項式を考えるためには、まず多項式の空間に内積を導入する必要がある。内積からノルムと直交性を定義し、異なる次数の多項式が互いに直交し、さらにそれぞれのノルムを $1$ にしたものが正規直交多項式である。

今回の中心となる定義は、

$$
\langle f,g\rangle
=
\int_a^b w(x)f(x)g(x)\,dx
$$

と、

$$
\langle\phi_i,\phi_j\rangle
=
\delta_{ij}
$$

の2つである。今後は、このように定義された正規直交多項式がどのような性質を持つのかを調べていく。

## 次の記事

次の記事では、正規直交多項式が満たす重要な性質の1つである**3項間漸化式**を扱う。正規直交多項式 $\phi_n$ は、隣り合う次数の多項式 $\phi_{n-1},\phi_n,\phi_{n+1}$ の間に特別な関係を持つことを示す。
