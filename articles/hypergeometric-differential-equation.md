---
layout: article
title: "超幾何方程式のノート：全体の目次"
seo_title: "超幾何方程式のノート：全体の目次｜超幾何関数"
description: "超幾何方程式のノートを12のテーマに分け、級数展開から確定特異点、特性指数、線形系、2階方程式へ順に読み進める目次です。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
  - "NIST, <a href=\"https://dlmf.nist.gov/2.7#i\">Digital Library of Mathematical Functions: Regular Singularities: Fuchs–Frobenius Theory</a>."
---

提供されたノート『超幾何方程式.pdf』を、12本のテーマ別記事に分けて整理した。ノート中のバツで取り消された範囲は掲載していない。

## 読む順番

1. [べき級数・解析関数・解析接続](/articles/hypergeometric-power-series.html) — べき級数、解析関数、解析接続の定義を、超幾何方程式のノートの最初の用語整理に沿って確認します。
2. [ローラン展開と特異点：極・留数・真性特異点](/articles/hypergeometric-laurent-singularities.html) — ローラン展開を特異部と正則部に分け、極の位数、留数、真性特異点を整理します。
3. [2階線形微分方程式の確定特異点](/articles/hypergeometric-regular-singular-points.html) — 2階線形微分方程式で、係数の極の位数から確定特異点を判定する定義を整理します。
4. [特性方程式と特性指数の導出](/articles/hypergeometric-indicial-equation.html) — y=x^αu の代入から特性方程式を導き、その根である特性指数と係数の関係を確認します。
5. [フロベニウス法：漸化式・整数差・対数解](/articles/hypergeometric-frobenius-solutions.html) — 特性指数から級数の漸化式を求め、指数差が整数でない場合と整数の場合の解の形を整理します。
6. [無限遠点の確定特異点と変数変換](/articles/hypergeometric-singularity-at-infinity.html) — x=1/t の変換により無限遠点を原点へ移し、変換後の方程式と係数の正則性を確認します。
7. [3つの確定特異点とフックスの関係式](/articles/hypergeometric-three-singularities.html) — 確定特異点を0・1・∞に配置した方程式の係数と、特性指数の総和に関するフックスの関係式を整理します。
8. [確定特異点を持つ線形系と固有値](/articles/hypergeometric-linear-systems.html) — 行列による線形微分方程式、係数行列のべき級数、固有値・固有ベクトルと逆行列の条件を整理します。
9. [線形系の級数解と係数ベクトルの漸化式](/articles/hypergeometric-matrix-series-solutions.html) — X=z^μΣz^kX_k を代入して係数を比較し、固有値を用いて係数ベクトルを順に決める方法を整理します。
10. [線形系の無限遠点と3つの特異点の変換](/articles/hypergeometric-matrix-singularities.html) — 線形系のz=1/tによる変換と、0・1・aから0・1・∞への1次分数変換をノートに沿って整理します。
11. [2成分の線形系から2階微分方程式を導く](/articles/hypergeometric-system-elimination.html) — 2×2の係数行列を持つ線形系から一方の未知関数を消去し、2階方程式の係数を求めます。
12. [部分分数と無限遠の条件：係数の相殺に注意](/articles/hypergeometric-partial-fractions.html) — 部分分数で書かれた2階方程式を無限遠で調べ、係数の組合せの解析性と個別の定数性を区別します。

## 原ノートの確認箇所

指数差が整数の場合は、級数解を保証する指数と対数項の扱いを修正した。また、無限遠における係数の組合せの解析性から、個々の係数の定数性は一般には従わないことを整理した。これらの確認に用いた NIST DLMF は、該当記事の参考文献に記載している。
