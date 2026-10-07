---
layout: article
title: "特性方程式と特性指数の導出"
seo_title: "特性方程式と特性指数の導出｜超幾何関数"
description: "y=x^αu の代入から特性方程式を導き、その根である特性指数と係数の関係を確認します。"
category: "hypergeometric-function"
category_label: "超幾何関数"
references:
  - "Harry Hochstadt, <cite>The Functions of Mathematical Physics</cite>, Wiley-Interscience, 1971."
---

2階方程式 $y''+P(x)y'+Q(x)y=0$ の確定特異点 $x=0$ を考える。その近傍で、係数を

$$
\begin{aligned}
P(x)&=p_{-1}x^{-1}+p_0+p_1x+\cdots,\\
Q(x)&=q_{-2}x^{-2}+q_{-1}x^{-1}+q_0+\cdots
\end{aligned}
$$

と展開し、$y=x^{\alpha}u$ とおく。微分すると、

$$
\begin{aligned}
y'&=x^{\alpha}u'+\alpha x^{\alpha-1}u,\\
y''&=x^{\alpha}u''+2\alpha x^{\alpha-1}u'
+\alpha(\alpha-1)x^{\alpha-2}u.
\end{aligned}
$$

したがって、$u$ に対する方程式は

$$
u''+\left(P(x)+\frac{2\alpha}{x}\right)u'
+\frac{\alpha(\alpha-1)+\alpha xP(x)+x^2Q(x)}{x^2}u=0.
$$

<div class="math-box definition-box" markdown="1">

<div class="math-box-title">定義：特性方程式と特性指数（Indicial Equation and Exponents）</div>

$u$ の係数の $x^{-2}$ の項を消す条件は、

$$
\alpha(\alpha-1)+p_{-1}\alpha+q_{-2}=0.
$$

これを特性方程式とし、その根を**特性指数**という。2つの根を $\alpha,\beta$ と書けば、根と係数の関係から

$$
\alpha+\beta=1-p_{-1}
$$

である。

</div>

## 続けて読む

[← 2階線形微分方程式の確定特異点](/articles/hypergeometric-regular-singular-points.html)

[フロベニウス法：漸化式・整数差・対数解 →](/articles/hypergeometric-frobenius-solutions.html)

[全体の目次](/articles/hypergeometric-differential-equation.html)
