up:: [[Fixed Income MOC]]
tags:: #Finance 
# Continuous Bond Price
$$V(r,t) = \frac{C}{r} \left(1 - e^{-r(T-t)}\right) + F e^{-r(T-t)} = \int_{0}^{T-t} C e^{-rs} \, ds + F e^{-r(T-t)}$$
$$$$
where
	$C$ is the continuous coupon payment rate 
	$r$ is the continuous discount rate 
	$T$ is total time to maturity of the bond
	$t$ is calendar time (elapsed time)
	$F$ is the face value of the bond \item $T$ is the time to maturity
	- for info on e see [[Fractional Period Bond]]

- $V(r,0)$ = present value of bond
- $\frac{\partial v}{\partial t}$ = capital gain/loss
- $rV - \frac{\partial v}{\partial t}$ = total return (capital gain + cash flow income)
	- This is also an ordinary differential equation ([[Derivatives]]) (first order linear ODE) --> $rV = V_t + C$
- $\frac{\partial v}{\partial r}$ = interest rate sensitivity [[Duration Model]]
- $\frac{\partial v/v}{\partial r}$ = % change in bond price per actual change in interest rates (negative modified duration)