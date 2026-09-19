---
layout: article
title: "Mellin変換による代数方程式の解の表示"
category: "gamma-function"
category_label: "ガンマ関数"
---

Mellin変換は積分計算だけでなく、代数方程式の解を積分表示へ変換するためにも利用できる。本記事では、

$$
y^\mu
+
xy^p
-
1
=
0,
\qquad
\mu>p>0
$$

という方程式を考える。

## 1. $x=0$ における解

$x=0$ では、

$$
y^\mu=1
$$

である。

$$
\varepsilon
=
e^{2\pi i/\mu}
$$

とおけば、解は、

$$
y_k(0)
=
\varepsilon^k,
\qquad
k=0,1,\ldots,\mu-1
$$

となる。

## 2. 解の対称性

<div class="math-box theorem-box">

<div class="math-box-title">解の回転対称性</div>

$y(x)$ が

$$
y^\mu+xy^p-1=0
$$

の解ならば、

$$
\varepsilon^k
y\left(
\varepsilon^{pk}x
\right)
$$

も解になる。

</div>

実際、

$$
t=\varepsilon^{pk}x
$$

とおくと、

$$
\left[
\varepsilon^ky(t)
\right]^\mu
+
x\left[
\varepsilon^ky(t)
\right]^p
-
1
=
y(t)^\mu
+
ty(t)^p
-
1
=
0
$$

となる。

## 3. 小さな $x$ に対する解

$x$ が十分小さいとき、ルーシェの定理を用いることで、$y=1$ の近くに解が1つ存在することを示すことができる。上の回転対称性を利用すれば、$x=0$ における各 $\mu$ 乗根から出る解を対応させることができる。

## 4. 実数上の正の解

$x>0$ に対して $y(0)=1$ から続く実数解を考える。方程式から、

$$
x
=
y^{-p}
-
y^{\mu-p}
$$

と書ける。

$x$ が $0$ から $\infty$ へ動くとき、この解では $y$ は $1$ から $0$ へ動く。

## 5. $y^\mu$ のMellin変換

$$
Y(z)
=
\int_0^\infty
y^\mu(x)x^{z-1}\,dx
$$

とおく。

$x=y^{-p}-y^{\mu-p}$ を用いて変数変換し、ベータ関数の表示へ整理すると、

<div class="math-box theorem-box">

<div class="math-box-title">Mellin変換</div>

$$
Y(z)
=
\frac{
\Gamma(z)
\Gamma\left(
\frac{\mu-pz}{\mu}
\right)
}{
\Gamma\left(
\frac{\mu-pz}{\mu}
+
z
+
1
\right)
}
$$

を得る。

</div>

積分の収束範囲は、

$$
0<\operatorname{Re}z<\frac{\mu}{p}
$$

となる。

## 6. Mellin反転

Mellin反転公式により、

$$
y^\mu(x)
=
\frac{1}{2\pi i}
\int_{c-i\infty}^{c+i\infty}
Y(z)x^{-z}\,dz,
\qquad
0<c<\frac{\mu}{p}
$$

と表される。

この積分では、$\Gamma(z)$ の極が左半平面に並び、

$$
\Gamma\left(
\frac{\mu-pz}{\mu}
\right)
$$

の極が右半平面に並ぶ。積分路をどちらへ閉じるかによって、異なる領域での級数表示が得られる。

## 7. Mellin変換と微分作用素

Mellin反転積分では、

$$
-x\frac{d}{dx}
$$

という微分作用素が、Mellin変数側の $z$ の掛け算に対応する。

すなわち、多項式 $\phi$ に対して、

$$
\phi\left(
-x\frac{d}{dx}
\right)
y^\mu(x)
=
\frac{1}{2\pi i}
\int
\phi(z)Y(z)x^{-z}\,dz
$$

という対応を考えることができる。

また、$Y(z+\mu)/Y(z)$ をガンマ関数の関数方程式で整理すると有理関数になるため、これを用いて $y^\mu(x)$ が線形微分方程式を満たすことが導かれる。

## 8. まとめ

代数方程式の解をMellin変換すると、ガンマ関数の積と商で表される関数 $Y(z)$ が現れる。Mellin反転によって元の解を複素積分として表すことができ、極と留数から級数展開を得ることができる。
