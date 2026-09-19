---
layout: article
title: "一般化二項定理"
category: "gamma-function"
category_label: "ガンマ関数"
---

<div class="math-box theorem-box">

<div class="math-box-title">定理：一般化二項定理</div>

$|x|<1$ とする。$x=0$ の近傍で選んだ $(1+x)^\alpha$ の正則な分枝に対して、

$$
(1+x)^\alpha
=
\sum_{n=0}^{\infty}
\binom{\alpha}{n}x^n
$$

が成り立つ。ここで、

$$
\binom{\alpha}{n}
=
\frac{
\alpha(\alpha-1)\cdots(\alpha-n+1)
}{n!}.
$$

</div>

## 証明

$$
f(x)=(1+x)^\alpha
$$

とおく。

微分を繰り返すと、

$$
f^{(n)}(x)
=
\alpha(\alpha-1)\cdots(\alpha-n+1)
(1+x)^{\alpha-n}.
$$

したがって $x=0$ では、

$$
f^{(n)}(0)
=
\alpha(\alpha-1)\cdots(\alpha-n+1).
$$

テイラー展開より、

$$
f(x)
=
\sum_{n=0}^{\infty}
\frac{f^{(n)}(0)}{n!}x^n.
$$

よって、

$$
(1+x)^\alpha
=
\sum_{n=0}^{\infty}
\frac{
\alpha(\alpha-1)\cdots(\alpha-n+1)
}{n!}
x^n
$$

となる。

$x=-1$ が最も近い分岐点または特異点になるため、この展開は少なくとも

$$
|x|<1
$$

で収束する。したがって、

$$
(1+x)^\alpha
=
\sum_{n=0}^{\infty}
\binom{\alpha}{n}x^n.
$$

$\square$

## 次の記事

[ガンマ関数による二項係数の表示](/articles/gamma-binomial-coefficient.html)
