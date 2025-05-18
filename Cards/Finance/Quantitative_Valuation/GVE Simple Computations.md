up:: [[Quantitative Valuation MOC]]
tags:: #Finance  
### GVE: 1 Period Payment
$$rV_0 + 0 = (0-V_0)+C_1$$
$$=V_0 = \frac{C_1}{1+r}$$
- No risk charge
- Future cash flows are 0 (1 period payment)
### GVE: Annuities and Perpetuities

#### Flat Perpetuity
$$rV_0 + 0 = 0 + C$$
$$V_0 = \frac {C}{r}$$
- Capital gain
	- Infinite series in a perpetuity:
	- $V_0 = PV[C, C, C...]$
	- $V_1 = PV[C, C, C...]$
		- $V_1 - V_0 = 0$
#### Deferred Perpetuity
$$rV_0 + 0 =0 + C \times d$$
$$V_0 = \frac{C}{r}d$$
- where d is the discount parameter $d_i=\frac{1}{(1+r)^i}$
#### Linear Growth Perpetuity
$$rV_0 + 0 = \frac{1}{r} + 1$$
$$V_0 = \frac{1+r}{r^2}$$
- Capital gain
	- 
#### Quadratic Perpetuity
- 
#### Exponential Growth Perpetuity
$$rV_0 + 0 = gV_0 + C$$
$$V_0 = \frac{C}{r-g}$$
- Capital gain
	- $V_1 = (1+g)V_0$
		- By distributive property:
			- $V_1 - V_0 = gV_0$
#### Flat Annuity
$$rV_0 + 0 = \frac{-C}{(1+r)^n} + C$$
$$V_0 = \frac{C}{r}(1-\frac{1}{(1+r)^n})$$
- Capital gain
	- $V_0 = PV[C, C, C...C]$
	- $V_1 = PV[C, C, C... 0]$
	- $V_1 - V_0 = \frac{-C}{(1+r^n)}$
		- $V_1 - V_0 = PV[0,0,0...-C]$ with -C in the nth position at the end
- This can also be thought of as the difference between the perpetuity and deferred perpetuity
#### Exponentially Growing Annuity
$$rV_0 + 0 = gV_0 - \frac{(1+g)(C_0)(1+g)^n}{(1+r)^n}+C_0(1+g)$$ 
$$V_0 = \frac{C}{r} +(1-\frac{1}{(1+r)^n})$$
- A growing annuity is also how [[COLA]] linked products can be valued