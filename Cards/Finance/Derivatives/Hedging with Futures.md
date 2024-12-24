up:: [[Derivatives MOC]]
tags:: #Finance 
# Hedging with [[Futures Contracts]]
## Short Hedge
- Used when you are already long some asset
- Not a speculative strategy -> intended to purely reduce risk and *lock in the price today*
- **How the hedge works:**
	- You try to perfectly hedge your long position with a **short future** of equal maturity and under the same asset
	- Will miss out on any stock gains because your short future position will offset it
	- Will also escape any stock losses because your short future will bring in money to offset this
- **Value of hedged position:**
	-  $V_1 = S_1 - (F_1 - F) = F + (S_1 - F_1) = F + b_1$
	-  1st equation: *the value of your position is the value of the underlying in the future less the change in futures price*
		- $S_1$ is the value of the underlying when you plan on buying it in the future
		- ($F_1-F$) is the change in the futures price from today ($F$) to when you want to buy ($F_1$)
	- 2nd equation: the value of your position is todays futures price less the [[Basis]] of the position
		- $(S_1-F_1)$ is the [[Basis]]
- **Payoff:**
	- $\Pi = (S_1 - S) - (F_1 - F)$
		- $(S_1 - S)$
			- Change in underlying
		- $(F_1 - F)$
			- Change in future price
	- Or: final [[Basis]] - initial [[Basis]]
	
## Long Hedge
- Used when you are already short an asset and concerned that prices will rise
	- Want to lock in the price today
- **How the hedge works:**
	- Try to perfectly hedge your short position by going long a future
	- Will miss out on short position income on decrease because long future will offset
- **Value of position:**
	- $V_1 = (F_1 - F) - S_1 = -F - b_1$
	- 1st equation: the value of your position is the change in futures price less the value of the stock when we need to buy it to close the short
	- 2nd equation: (-) the price we paid for the future - the [[Basis]] (should be 0)
- **Payoff:**
	- $\Pi = (F_1 - F) - (S_1 - S) = b - b_1$
	- Change in futures - change in underlying
		- Reverse of short hedge payoff

## Cross Hedge
 - When you are working with different underlying investments and have an imperfect hedge
 - Correlation will be slightly imperfect
	 - Ex: need to hedge jet fuel but theres not jet fuel futures --> will hedge with heating oil
 - **How the hedge works:**
	 - Find an asset that is highly correlated with what you want to hedge and enter a future
 - **Value of position:**
	 - $V_1 = (F_{1,A} - F_{0,A}) - S_{1,B}\hspace{1cm}\text{or}\hspace{1cm}V_1 = (F_{1,A} - S_{1,B}) - F_{0,A}\hspace{1cm}\text{or}\hspace{1cm}= -b_{1,A} - (S_{1,B} - S_{1,A}) - F_{0,A}$
	 - $A$ denotes asset $A$ which is what we are hedging with (heating oil in example)
	 - $B$ denotes asset $B$ which is what we are looking to hedge (jet fuel in example)
	 - 1st equation: gain on future position for what we hedge with less the future market value of what we are hedging
	 - 2nd equation: futures price of asset B less price of asset A in the future less price of asset A today
	 - 3rd equation: (-) [[Basis]] less difference between spot price of 2 assets in future less price today
- Biggest risk: imperfect correlation in hedge
## Rolling Hedge
- When you have a maturity mismatch between your underlying and your future (time maturity mismatch)
- **How the hedge works:**
	- Trade out of your current hedge near expiry, then enter another one
	- Close out current hedge when it loses liquidity, enter the next one when it gains liquiditiy
		- The later in maturity the future, the less people want to buy it 
## Minimum Variance (Risk) Portfolio Hedge
- Used to find the minimum amount of futures contracts required to minimize risk
- $\Pi = (V_S \times R_S) + (N_F \times V_F \times R_F)$
	- Π: Total profit or loss from the hedged position.
	- $V_S$​: Value of the spot position (underlying asset).
	- $R_S$​: Return on the spot position.
	- **$N_F$​: Number of futures contracts.**
		- $= -\frac{V_S \, \text{Cov}(R_S, R_F)}{V_F \, \sigma_F^2}$
			- Number of contracts to minimize risk = - (Portfolio size /futures contract value) * slope coefficient
				- Slope coefficient is beta
			- $V_S$​: Value of the spot position (underlying asset).
			- $Cov(R_S​,R_F​)$: Covariance between the return on the spot position and the return on the futures position.
			- $V_F$​: Value of each futures contract.
			- $σF_2​$: Variance of the futures return.
			- $\beta$ : = $-\frac{\text{Cov}(R_S, R_F)}{\sigma_F^2}$
	- $V_F$​: Value of each futures contract.
	- $R_F$​: Return on the futures position.
### Example
- Portfolio size = 750000, Futures contract = 125000, Beta = 0.5
- ![[Pasted image 20240623151248.png]]
	- -3 means you short 3 contracts to hedge
## Currency Hedging
- [[FX MOC]]
- Used most commonly by companies who get paid in foreign currency
	- Enter a [[Forward Contracts]] or [[Futures Contracts]] to lock in the payment
- 