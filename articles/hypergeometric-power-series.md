---
layout: article
title: "べき級数・解析関数・解析接続"
seo_title: "べき級数・解析関数・解析接続｜超幾何関数"
description: "べき級数、解析関数、解析接続の定義を、超幾何方程式のノートの最初の用語整理に沿って確認します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
---

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：べき級数（Power Series）</div>

中心を $c\in\mathbb C$ とする級数

$$
\sum_{n=0}^{\infty}a_n(z-c)^n
=a_0+a_1(z-c)+\cdots
$$

を、$c$ を中心とするべき級数という。

</div>

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：解析関数（Analytic Function）</div>

定義域 $D$ の各点 $c$ を中心とするべき級数で表せる関数 $f(z)$ を解析関数という。ノートでは、級数が正の収束半径を持ち、その和が $f(z)$ に等しいことを条件としている。

</div>

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：解析接続（Analytic Continuation）</div>

$D$ を含む定義域 $G$ に定義された解析関数 $g$ が、$D\cap G$ 上で $f$ と等しいとき、$g$ を $f$ の解析接続という。

</div>

## 続けて読む

[ローラン展開と特異点：極・留数・真性特異点 →](/articles/hypergeometric-laurent-singularities.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)

出典ノート：『超幾何方程式.pdf』1ページ。
