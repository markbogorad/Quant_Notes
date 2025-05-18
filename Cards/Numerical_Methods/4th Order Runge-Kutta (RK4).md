up:: [[Numerical Methods MOC]]
tags:: #Math 
# 4th Order Runge-Kutta
$$k_1 = h f(x_n, y_n)$$
$$k_2 = h f(x_n + h/2, y_n + k_1/2)$$
$$k_3 = h f(x_n + h/2, y_n + k_2/2)$$ $$k_4 = h f(x_n + h, y_n + k_3)$$
- k1​ is the slope at the beginning of the interval.
- k2​ and k3​ are estimates of the slope at the midpoint.
	- [[2nd Order Runge-Kutta (Midpoint Method)]]
- k4​ is the slope at the end of the interval.
- The final step is a **weighted average of all these slopes**, giving a more accurate estimate of yn+1​.