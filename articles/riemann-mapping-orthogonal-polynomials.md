---
layout: article
title: リーマンの写像定理と直交多項式
---

## はじめに

リーマンの写像定理は、複素解析における基本的な定理の一つである。

この定理は、複素平面上の単連結領域を単位円板へ正則に写すことができる、ということを主張する。

一方、直交多項式は実数上で考えられることが多いが、複素平面上の曲線に対しても定義することができる。

この記事では、

1. 複素平面上の曲線における正規直交多項式
2. 再生核
3. リーマンの写像定理
4. 再生核とリーマン写像関数の関係

について説明する。

最終的には、正規直交多項式から作られる再生核を用いて、

$$
\gamma(z)
=
\lim_{n\to\infty}
\frac{2\pi}{K_n(a,a)}
\int_a^z K_n(a,\xi)^2\,d\xi
$$

という形でリーマン写像関数を表すことを目標とする。


## 1. 複素領域における多項式の内積

まず、複素平面上の曲線に対して多項式の内積を定義する。

<div class="math-box definition-box" markdown="1">

<p class="math-box-title">定義 1（内積）</p>

$\mathbb{C}[z]$ を複素係数の多項式全体の集合とする。

また、

$$
C:z=z(s),
\qquad
0\leq s\leq L
$$

を複素平面上の自己交叉がなく、長さをもつ曲線とする。

ここで $s$ は曲線 $C$ の弧長パラメータであり、

$$
w(s)\geq0
$$

を重み関数とする。

このとき、

$$
f(z),g(z)\in\mathbb{C}[z]
$$

に対して

$$
(f,g)
=
\int_0^L
w(s)
f(z(s))
\overline{g(z(s))}
|z'(s)|\,ds
$$

すなわち

$$
(f,g)
=
\int_C
w(s)f(z)\overline{g(z)}\,ds
$$

によって内積を定める。

</div>

この内積に関して、$n$ 次多項式

$$
\phi_n(z)
\qquad
(n=0,1,2,\ldots)
$$

が

$$
(\phi_i,\phi_j)
=
\delta_{ij}
$$

を満たすとする。

ここで

$$
\delta_{ij}
=
\begin{cases}
1 & (i=j),\\
0 & (i\neq j)
\end{cases}
$$

である。

このような

$$
\phi_0(z),\phi_1(z),\phi_2(z),\ldots
$$

を曲線 $C$ 上の**正規直交多項式**と呼ぶ。


## 2. 再生核

正規直交多項式を使って、次の関数を定義する。

<div class="math-box definition-box" markdown="1">

<p class="math-box-title">定義 2（再生核）</p>

$n$ 次多項式 $K_n(a,z)$ を

$$
K_n(a,z)
=
\sum_{k=0}^{n}
\overline{\phi_k(a)}\phi_k(z)
$$

と定義する。

これを**再生核**と呼ぶ。

</div>

再生核という名前は、次の性質に由来する。

<div class="math-box proposition-box" markdown="1">

<p class="math-box-title">命題 3（再生性）</p>

$p(z)$ を高々 $n$ 次の多項式とする。

このとき、

$$
(p(z),K_n(a,z))
=
\int_C
w(s)p(z)\overline{K_n(a,z)}\,ds
=
p(a)
$$

が成り立つ。

</div>

つまり、再生核 $K_n(a,z)$ との内積を取ることで、

$$
p(z)
$$

という多項式から

$$
p(a)
$$

という一点での値を取り出すことができる。

この性質が「再生」という名前の意味である。


## 3. 再生核の極値的性質

再生核から、次の多項式を作る。

<div class="math-box proposition-box" markdown="1">

<p class="math-box-title">命題 4</p>

$n$ 次多項式 $G_n(z)$ を

$$
G_n(z)
=
\frac{\varepsilon K_n(a,z)}
{\sqrt{K_n(a,a)}},
\qquad
|\varepsilon|=1
$$

と定義する。

このとき、

$$
\|G_n\|^2
=
(G_n,G_n)
=
\int_C
w(s)|G_n(z)|^2\,ds
=
1
$$

であり、

$$
|G_n(a)|
\geq
|\rho(a)|
$$

が成り立つ。

ここで $\rho(z)$ は

$$
\|\rho\|=1
$$

を満たす任意の高々 $n$ 次の多項式である。

</div>

したがって $G_n$ は、ノルムを1に固定した多項式の中で、点 $a$ における絶対値を最大にする性質をもつ。

この極値的性質が、後でリーマン写像関数と再生核を結びつける際に重要になる。


## 4. リーマンの写像定理

ここで複素解析の基本定理であるリーマンの写像定理を確認する。

<div class="math-box theorem-box" markdown="1">

<p class="math-box-title">定理 5（リーマンの写像定理）</p>

$D\subsetneq\mathbb{C}$ が単連結領域ならば、$D$ から単位円板

$$
U
=
\{z\in\mathbb{C}\mid |z|<1\}
$$

への正則な全単射写像

$$
\gamma:D\longrightarrow U
$$

が存在する。

さらに $D$ の一点 $a$ を選び、

$$
\gamma(a)=0,
\qquad
\gamma'(a)>0
$$

という条件を加えると、$\gamma$ は一意に定まる。

</div>

写像を一意に決めるためには、

$$
\gamma(a)=0
$$

だけではなく、

$$
\gamma'(a)>0
$$

という条件も必要になる。


## 5. 平均値の定理

主定理の証明では、正則関数の平均値に関する性質を利用する。

<div class="math-box lemma-box" markdown="1">

<p class="math-box-title">補題 6（平均値の定理）</p>

領域 $D$ で正則な関数 $f$ の点 $a\in D$ における値は、$a$ を中心とする $D$ に含まれる十分小さい半径 $r$ の円周上の平均値に等しい。

すなわち、

$$
f(a)
=
\frac{1}{2\pi}
\int_0^{2\pi}
f(a+re^{i\theta})\,d\theta
$$

が成り立つ。

</div>


## 6. 再生核によるリーマン写像関数の表示

ここからがこの記事の中心となる。

以下では

$$
w(s)\equiv1
$$

とする。

<div class="math-box theorem-box" markdown="1">

<p class="math-box-title">定理 7</p>

$C$ を単純閉曲線とする。

$C$ の内部を単位円板へ写し、

$$
\gamma(a)=0,
\qquad
\gamma'(a)>0
$$

を満たす正則関数は、

$$
\boxed{
\gamma(z)
=
\lim_{n\to\infty}
\frac{2\pi}{K_n(a,a)}
\int_a^z
K_n(a,\xi)^2\,d\xi
}
$$

によって与えられる。

</div>

この公式は、

**曲線 $C$ 上の正規直交多項式から再生核を作れば、その曲線の内部を単位円板へ写す写像を構成できる**

ことを示している。

直交多項式という代数的・解析的な対象と、等角写像という幾何学的な対象が直接結びついている。


## 7. 定理 7 の証明

$C$ の内部を $D$

とおく。

証明を3つの段階に分ける。


### Step 1：再生核の極限

まず

$$
K(a,z)
=
\lim_{n\to\infty}
K_n(a,z)
$$

となる関数の存在を考える。

コーシーの積分公式から、

$$
K_n(a,a)^2
=
\frac{1}{2\pi i}
\int_C
\frac{K_n(a,z)^2}{z-a}\,dz
$$

を満たす。

ここで $\delta$ を点 $a$ と曲線 $C$ の距離とする。

両辺を $K_n(a,a)$ で割ると、

$$
K_n(a,a)
=
\frac{1}{2\pi i}
\int_C
\frac{K_n(a,z)^2}
{(z-a)K_n(a,a)}
\,dz.
$$

命題4で定義した $G_n$ を用いると、

$$
K_n(a,a)
=
\frac{1}{2\pi i}
\int_C
\frac{G_n(z)^2}
{\varepsilon(z-a)}
\,dz.
$$

積分の三角不等式から、

$$
K_n(a,a)
\leq
\frac{1}{|2\pi i|}
\int_C
\frac{|G_n(z)|^2}
{|\varepsilon|\,|z-a|}
\,|dz|.
$$

$\lvert \varepsilon \rvert = 1$ かつ

$$
|z-a|\geq\delta
$$

であるから、

$$
K_n(a,a)
\leq
\frac{1}{2\pi\delta}
\|G_n\|^2.
$$

さらに

$$
\|G_n\|=1
$$

なので、

$$
K_n(a,a)
\leq
\frac{1}{2\pi\delta}
$$

を得る。


次に、

$$
A=
\begin{pmatrix}
\phi_0(a)\\
\phi_1(a)\\
\vdots\\
\phi_n(a)
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
\phi_0(z)\\
\phi_1(z)\\
\vdots\\
\phi_n(z)
\end{pmatrix}
$$

とする。

コーシー・シュワルツの不等式より、

$$
|K_n(a,z)|^2
\leq
K_n(a,a)K_n(z,z)
$$

となる。

上で得た評価を用いれば、

$$
|K_n(a,z)|^2
\leq
\frac{1}{4\pi^2\delta^2}
$$

を得る。

したがって $K_n(a,z)$ は領域 $D$ の内部で制御され、極限関数

$$
K(a,z)
=
\lim_{n\to\infty}
K_n(a,z)
$$

を考えることができる。

これに伴って、

$$
G(z)
=
\lim_{n\to\infty}
\frac{K_n(a,z)}
{\sqrt{K_n(a,a)}}
$$

を考える。


### Step 2：リーマン写像との関係

リーマンの写像定理によって得られる

$$
\gamma:D\longrightarrow U
$$

の逆関数を

$$
g=\gamma^{-1}
$$

とする。

単位円周上では、

$$
\gamma
=
\gamma(z(s))
=
e^{i\theta}
$$

と表すことができる。

このとき、

$$
|d\gamma|
=
|\gamma'(z)|\,ds
=
d\theta.
$$

また、$g$ は $\gamma$ の逆関数なので、

$$
\gamma'(z)g'(\gamma)=1.
$$

したがって、

$$
ds
=
\frac{d\theta}{|\gamma'(z)|}
=
|g'(\gamma)|\,d\theta.
$$

これを利用すると、

$$
\int_C
|G(z)|^2\,ds
=
\int_0^{2\pi}
|G(g(\gamma))|^2
|g'(\gamma)|\,d\theta.
$$

ここで

$$
F(\gamma)
=
G(g(\gamma))
g'(\gamma)^{1/2}
$$

とおく。

すると、

$$
\int_0^{2\pi}
|F(\gamma)|^2\,d\theta
=
1.
$$

$F$ を

$$
F(\gamma)
=
\sum_{n=0}^{\infty}
a_n\gamma^n
$$

と展開する。

$\gamma=e^{i\theta}$ とすると、

$$
2\pi
\sum_{n=0}^{\infty}
|a_n|^2
=
1.
$$

ここで

$$
\gamma(a)=0
$$

である。

この条件のもとで $|G(a)|$ を最大にするためには、定数項以外を0とする必要がある。

したがって、

$$
F(\gamma)=a_0.
$$

よって、

$$
|a_0|^2
=
\frac{1}{2\pi}.
$$

一方、

$$
|G(a)|^2
=
\frac{|F(0)|^2}{|g'(0)|}.
$$

逆関数の微分から、

$$
g'(0)
=
\frac{1}{\gamma'(a)}
$$

なので、

$$
|G(a)|^2
=
\frac{\gamma'(a)}{2\pi}.
$$

また、

$$
|G(a)|^2
=
\lim_{n\to\infty}
K_n(a,a)
$$

である。

したがって、

$$
\boxed{
\frac{\gamma'(a)}{2\pi}
=
\lim_{n\to\infty}
K_n(a,a)
}
$$

を得る。


### Step 3：再生核と $\gamma'(z)$

次の積分を考える。

$$
J_n
=
\int_C
\left|
K_n(a,z)
-
\frac{1}{2\pi}
\{\gamma'(a)\gamma'(z)\}^{1/2}
\right|^2
ds.
$$

これを展開すると、

$$
J_n
=
\int_C
|K_n(a,z)|^2\,ds
+
\frac{\gamma'(a)}{4\pi^2}
\int_C
|\gamma'(z)|\,ds
-
\frac{1}{\pi}
\operatorname{Re}
\int_C
K_n(a,z)
\{\gamma'(a)\gamma'(z)\}^{1/2}
ds.
$$

第1項は、

$$
\int_C
|K_n(a,z)|^2\,ds
=
K_n(a,a).
$$

第2項は、

$$
\frac{\gamma'(a)}{4\pi^2}
\int_C
|\gamma'(z)|\,ds
=
\frac{\gamma'(a)}{2\pi}.
$$

第3項について平均値の定理を利用すると、

$$
\frac{1}{\pi}
\int_C
K_n(a,z)
\{\gamma'(a)\gamma'(z)\}^{1/2}
ds
=
2K_n(a,a)
$$

となる。

したがって、

$$
J_n
=
K_n(a,a)
+
\frac{\gamma'(a)}{2\pi}
-
2K_n(a,a).
$$

すなわち、

$$
J_n
=
\frac{\gamma'(a)}{2\pi}
-
K_n(a,a).
$$

Step 2 の結果から、

$$
\lim_{n\to\infty}J_n=0
$$

となる。

この関係から再生核とリーマン写像の微分の関係

$$
\gamma'(z)
=
\lim_{n\to\infty}
\frac{2\pi}
{K_n(a,a)}
K_n(a,z)^2
$$

が得られる。

最後に

$$
\gamma(a)=0
$$

であることを利用して $a$ から $z$ まで積分すると、

$$
\boxed{
\gamma(z)
=
\lim_{n\to\infty}
\frac{2\pi}
{K_n(a,a)}
\int_a^z
K_n(a,\xi)^2\,d\xi
}
$$

を得る。


<div class="math-box" markdown="1">

<p class="math-box-title">数学的な注意</p>

ここではスライドで示した証明の流れに沿って説明している。

特に Step 1 の収束の扱いや、Step 3 で

$$
J_n\to0
$$

から再生核の点ごとの極限関係を導く部分について、完全に厳密な証明を書く場合には、正規族・広義一様収束などを用いた追加の議論が必要になる。

</div>


## 8. 具体例：単位円

最後に、単位円の場合を考える。

単純閉曲線 $C$ を

$$
z(s)=e^{is},
\qquad
0\leq s\leq2\pi
$$

とし、

$$
w(s)=1
$$

とする。

このとき、正規直交多項式は

$$
\phi_k(z)
=
\frac{1}{\sqrt{2\pi}}z^k
$$

となる。

実際、

$$
(\phi_j,\phi_k)
=
\int_C
\phi_j(z)\overline{\phi_k(z)}\,ds
$$

であり、

$$
(\phi_j,\phi_k)
=
\frac{1}{2\pi}
\int_0^{2\pi}
e^{i(j-k)s}\,ds
=
\delta_{jk}
$$

となる。

したがって、この多項式系は単位円上で正規直交系になっている。


### 再生核を求める

定義より、

$$
K(a,z)
=
\sum_{n=0}^{\infty}
\overline{\phi_n(a)}
\phi_n(z).
$$

ここで、

$$
\overline{\phi_n(a)}
\phi_n(z)
=
\frac{(\overline{a}z)^n}{2\pi}
$$

なので、

$$
K(a,z)
=
\frac{1}{2\pi}
\sum_{n=0}^{\infty}
(\overline{a}z)^n.
$$

これは等比級数であるから、

$$
K(a,z)
=
\frac{1}
{2\pi(1-\overline{a}z)}
$$

となる。


### 写像関数を求める

定理7の公式に代入すると、

$$
\gamma(z)
=
4\pi^2(1-|a|^2)
\int_a^z
\frac{1}
{4\pi^2(1-\overline{a}\xi)^2}
\,d\xi.
$$

積分を計算すると、

$$
\boxed{
\gamma(z)
=
\frac{z-a}
{1-\overline{a}z}
}
$$

を得る。

これは単位円板を自分自身へ写す一次分数変換である。

特に、

$$
\gamma(a)=0
$$

を満たしており、指定した点 $a$ を原点へ移している。


## 9. まとめ

この記事では、複素平面上の曲線における正規直交多項式から出発して、再生核とリーマン写像関数の関係を見た。

流れをまとめると、

1. 曲線 $C$ 上に多項式の内積を定義する
2. 正規直交多項式 $\phi_n$ を考える
3. 正規直交多項式から再生核 $K_n(a,z)$ を作る
4. 再生核の極値的性質を利用する
5. リーマンの写像定理と結びつける

という構成になっている。

特に重要な公式は、

$$
\boxed{
\gamma(z)
=
\lim_{n\to\infty}
\frac{2\pi}{K_n(a,a)}
\int_a^z
K_n(a,\xi)^2\,d\xi
}
$$

である。

これは、**直交多項式から等角写像を構成できる**ことを示している。

直交多項式と複素解析が直接結びつく興味深い例である。


## 参考文献

- H. ホックシタット『特殊関数』培風館, 1974年
- 杉浦光夫『解析入門 II』東京大学出版会, 1985年
- 神保道夫『複素関数入門』岩波書店, 2024年
- 藤本担孝『複素解析』岩波書店, 2019年
