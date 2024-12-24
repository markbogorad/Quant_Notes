up:: [[Fixed Income MOC]]
tags:: #Finance
# Spot Rates
- Spot rate refers to the yield on a 0 coupon bond
	- This information is used to price various kinds of bonds
	- The spot rate is essentially *the rate of return on the zero coupon bond*, as it earns no other income
- If spot rate price > market price -> bond is undervalued
-  If spot rate price < market price -> bond is overvalued
## Spot Rates & Forward Rates
**2 year spot rate**
$$ (1+S_2)^2=(1+S_1) \times (1+F_{1,1}) $$
- $S_1$ is the year 1 spot rate
- $S_2$ is the year 2 spot rate
- $F_{1,1}$ is the 1 year forward rate 1 year from now

**3 year spot rate**
$$ (1+S_3)^3=(1+S_2)^2 \times (1+F_{2,1}) $$
- $F_{2,1}$ is the 1 year forward rate 2 years from now
- Exponents represent number of years compounded for that specific product

**Generalized**
$$(1 + S_n)^n = (1 + S_{n-1})^{n-1} \times (1 + F_{n-1,1})$$
- $(1+S_{n−1}​)^{n−1}$: The growth over the first $n−1$ years.
- $(1+F_{n−1,1})$: The forward rate for the final year, starting after $n−1$ years.

## Applied to [[Futures Contracts]]
- Using spot rates, you can value futures by finding the spot rate in the future:
$$ FV = PV \times (1 + S_n)^n $$
- S is the spot rate for that prevailing period
### Calculating Forward Rate Using Spot Rates
- Rate used in forward contract (interest agreed today on a settlement in future)
$$ F_t(T_1, T_2) = \left( \frac{[1 + y_2]^{T_2 - t}}{[1 + y_1]^{T_1 - t}} \right)^{\frac{1}{T_2 - T_1}} - 1$$
- $Ft​(T1​,T2​)$: The forward rate starting at time $T1$​ and ending at time $T2$​.
- $y1$​: The spot rate for the period from $t$ to $T1$​.
- $y2$​: The spot rate for the period from $t$ to $T2$​.
- $T1$​ and $T2$​: Future times where $T2>T1$​.

- **Numerator** $[1+y_2]^{T2−t}$: This represents the growth factor of an investment from time $t$ to $T2$​ at the spot rate $y2$​.
- **Denominator** $[1+y_1]^{T1−t}$: This represents the growth factor of an investment from time $t$ to $T1$​ at the spot rate $y1$​.
- **Exponent** $\frac{1}{T_2−T_1}$​: This adjusts the ratio of growth factors to the specific period from $T1$​ to $T2$​.
- **Minus 1**: This subtracts 1 to convert the growth factor back to a forward rate.
#### Based off no-arbitrage
- These 2 portfolios should equal:
- ![[Pasted image 20240619144427.png]]
- Spot rates on risk free bonds should reflect forwards
	- Strategy A = Strategy B or else there is arbitrage