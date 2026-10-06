---
layout: article
title: "エルミート多項式とラゲール多項式の完備性（Completeness of Hermite and Laguerre Polynomials）"
seo_title: "エルミート多項式とラゲール多項式の完備性｜無限区間での証明"
description: "エルミート多項式とラゲール多項式の完備性を、有限区間とは異なる無限区間上の議論と変換積分を用いて整理します。"
category: "classical-orthogonal-polynomials"
category_label: "古典的直交多項式"
---

有限区間ではワイエルシュトラスの近似定理を用いて直交多項式系の完備性を示すことができるが、エルミート多項式やラゲール多項式では区間が無限になるため同じ議論をそのまま使うことはできない。本記事では、変換積分を用いた完備性の考え方を整理する。

## 1. エルミート多項式の場合

重み $w_H(x)=e^{-x^2/2}$ に対する空間 $L^2(\mathbb R,w_H(x)\,dx)$ の関数 $f$ が、すべての多項式と直交しているとする。すなわち、

$$
\int_{-\infty}^{\infty}
e^{-x^2/2}
x^n f(x)\,dx
=
0
\qquad
(n=0,1,2,\ldots)
$$

を仮定する。

ここで、

$$
F(z)
=
\int_{-\infty}^{\infty}
e^{zx}
e^{-x^2/2}
f(x)\,dx
$$

を考える。

## 2. $F(z)$ の導関数

コーシー・シュワルツの不等式により、任意の $R>0$ と整数 $n\geq0$ に対して

$$
\int_{\mathbb R}|x|^n e^{R|x|}w_H(x)|f(x)|\,dx
\leq\|f\|_{L^2(w_H)}
\left(\int_{\mathbb R}|x|^{2n}e^{2R|x|}w_H(x)\,dx\right)^{1/2}<\infty.
$$

したがって、$F$ の積分は複素平面のコンパクト集合上で一様に支配され、積分の下で何回でも微分できる。特に $F$ は整関数である。

積分の中を $z$ で微分すると、

$$
F^{(n)}(z)
=
\int_{-\infty}^{\infty}
x^n e^{zx}
e^{-x^2/2}
f(x)\,dx
$$

となる。特に $z=0$ では、

$$
F^{(n)}(0)
=
\int_{-\infty}^{\infty}
x^n
e^{-x^2/2}
f(x)\,dx
=
0.
$$

したがって、$F$ の $0$ におけるすべてのテイラー係数が $0$ となる。$F$ は整関数なので、

$$
F(z)\equiv0.
$$

## 3. フーリエ変換との関係

$z=i\xi$ とおくと、

$$
F(i\xi)
=
\int_{-\infty}^{\infty}
e^{i\xi x}
e^{-x^2/2}
f(x)\,dx
=
0
$$

となる。

これは

$$
e^{-x^2/2}f(x)
$$

は上の評価の $n=0,R=0$ の場合から $L^1(\mathbb R)$ に属し、そのフーリエ変換が恒等的に $0$ である。フーリエ変換の一意性から、

$$
e^{-x^2/2}f(x)=0
$$

がほとんど至る所で成り立ち、重みは正なので、

$$
f(x)=0
$$

をほとんど至る所で得る。

したがって、エルミート多項式系にすべて直交する関数は零関数しかなく、エルミート多項式系の完備性につながる。

## 4. ラゲール多項式の場合

ラゲール多項式では $\alpha>-1$ とし、重み $w_L(x)=x^\alpha e^{-x}$ に対する空間 $L^2((0,\infty),w_L(x)\,dx)$ の関数 $f$ を考える。同様に、

$$
\int_0^\infty
x^\alpha e^{-x}
x^n f(x)\,dx
=
0
\qquad
(n=0,1,2,\ldots)
$$

を満たす関数 $f$ を考える。

ここでは、重みを含むラプラス型の変換

$$
F_L(z)=\int_0^\infty e^{zx}w_L(x)f(x)\,dx
$$

を直接用いる。$\operatorname{Re}z<1/2$ ならば、

$$
\int_0^\infty e^{(\operatorname{Re}z)x}w_L(x)|f(x)|\,dx
\leq\|f\|_{L^2(w_L)}
\left(\int_0^\infty x^\alpha e^{-(1-2\operatorname{Re}z)x}\,dx\right)^{1/2}<\infty.
$$

導関数についても同様に評価できるため、$F_L$ は半平面 $\operatorname{Re}z<1/2$ で正則である。モーメント条件から

$$
F_L^{(n)}(0)=\int_0^\infty x^n w_L(x)f(x)\,dx=0
\qquad(n=0,1,2,\ldots)
$$

なので、一致の定理よりこの半平面で $F_L\equiv0$ となる。

特に $F_L(i\xi)=0$ は、$w_Lf$ を負の実軸上で $0$ に拡張した $L^1(\mathbb R)$ 関数のフーリエ変換が零であることを意味する。一意性から $w_Lf=0$、したがって $f=0$ がほとんど至る所で成り立つ。これでラゲール多項式系の完備性も示された。

<div class="math-box theorem-box">

<div class="math-box-title">完備性の考え方（Idea of Completeness）</div>

無限区間におけるエルミート多項式系やラゲール多項式系では、すべての多項式との直交条件を変換積分へ移し、その一意性を利用することで零関数しか残らないことを示す。

</div>

## 次の記事

[母関数とは何か：エルミート多項式とラゲール多項式](/articles/generating-functions-hermite-laguerre.html)
