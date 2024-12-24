up:: [[Stochastic Calculus MOC]]
tags:: #Math
# Ito's Lemma
- Let $X_t$ be a stochastic process defined by:
	- $dX_t = \mu_t \, dt + \sigma_t \, dW_t$
- and let $f(t, X_t)$ be a twice-differentiable function. Then, Itô's Lemma states:
$$df(t, X_t) = \left( \frac{\partial f}{\partial t} + \mu_t \frac{\partial f}{\partial X} + \frac{1}{2} \sigma_t^2 \frac{\partial^2 f}{\partial X^2} \right) dt + \sigma_t \frac{\partial f}{\partial X} \, dW_t$$
- 