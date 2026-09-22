---
layout: article
title: "ガンマ関数の定義（Definition of the Gamma Function）"
seo_title: "ガンマ関数とは？定義・収束条件と階乗との関係"
description: "ガンマ関数 Γ(z) のオイラー積分による定義、Re z>0 という収束条件、階乗との関係を数式とともに解説します。"
category: "gamma-function"
category_label: "ガンマ関数"
---

ガンマ関数は、階乗を複素数の領域へ拡張する特殊関数である。このページでは定義と、後続の定理記事への入口だけをまとめる。

## オイラー積分による定義

<div class="math-box definition-box">

<div class="math-box-title">定義：ガンマ関数（Gamma Function）</div>

$\operatorname{Re}z>0$ に対して、

$$
\Gamma(z)
=
\int_0^\infty e^{-t}t^{z-1}\,dt
$$

と定める。

</div>

$t\to\infty$ では $e^{-t}$ が急速に減衰する。一方、$t\to0$ では

$$
|t^{z-1}|=t^{\operatorname{Re}z-1}
$$

なので、積分が収束するために

$$
\operatorname{Re}z>0
$$

が必要になる。

## このあと使う定理

ガンマ関数の基本性質は、1つの定理ごとに別の記事で扱う。

- [ガウスの極限表示](/articles/gamma-gauss-limit-formula.html)
- [ワイエルシュトラスの積表示](/articles/gamma-weierstrass-product.html)
- [ガンマ関数の関数方程式](/articles/gamma-functional-equation.html)
- [ガンマ関数の極と留数](/articles/gamma-poles-residues.html)

これらを使うことで、オイラー積分で最初に定義された右半平面から、非正整数を除く複素平面全体へガンマ関数を解析接続できる。
