---
layout: article
title: "ガンマ関数の関数方程式"
seo_title: "ガンマ関数の関数方程式 Γ(z+1)=zΓ(z)｜証明と意味"
description: "ガンマ関数の基本公式 Γ(z+1)=zΓ(z) を部分積分から証明し、階乗の拡張との関係を説明します。"
category: "gamma-function"
category_label: "ガンマ関数"
---

ガンマ関数が階乗の拡張になることを示す中心的な関係が、関数方程式

$$
\Gamma(z+1)=z\Gamma(z)
$$

である。

<div class="math-box theorem-box">

<div class="math-box-title">定理：ガンマ関数の関数方程式</div>

$\operatorname{Re}z>0$ に対して、

$$
\Gamma(z+1)=z\Gamma(z)
$$

が成り立つ。さらに解析接続によって、この関係は両辺が定義されるすべての $z$ に対して成り立つ。

</div>

## 証明

オイラー積分から、

$$
\Gamma(z+1)
=
\int_0^\infty
e^{-t}t^z\,dt.
$$

ここで部分積分を行う。

$$
u=t^z,
\qquad
dv=e^{-t}\,dt
$$

とおけば、

$$
du=zt^{z-1}\,dt,
\qquad
v=-e^{-t}.
$$

したがって、

$$
\Gamma(z+1)
=
\left[
-e^{-t}t^z
\right]_{0}^{\infty}
+
z
\int_0^\infty
e^{-t}t^{z-1}\,dt.
$$

$\operatorname{Re}z>0$ ならば、

$$
e^{-t}t^z\to0
\qquad(t\to\infty)
$$

かつ

$$
t^z\to0
\qquad(t\to0^+)
$$

なので境界項は $0$ である。

よって、

$$
\Gamma(z+1)
=
z
\int_0^\infty
e^{-t}t^{z-1}\,dt
=
z\Gamma(z).
$$

解析接続の一意性により、この恒等式はガンマ関数を解析接続した領域でも成り立つ。
<div class="proof-end">\(\square\)</div>

## 系：階乗との関係

$\Gamma(1)=1$ なので、正整数 $n$ に対して

$$
\Gamma(n+1)
=
n!
$$

となる。

## 次の記事

[ガンマ関数の極と留数](/articles/gamma-poles-residues.html)
