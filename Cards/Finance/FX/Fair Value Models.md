up:: [[FX MOC]]
tags:: #Finance 
# Fair Value Models
## Monetary Models
**Flexible Price Monetary Model (FPMM)**
- Assumes [[Purchasing Power Parity]] holds
- Based on money demand [[Quantity Theory of Money]]
$$s_t = m_t - m_t - \alpha (y_t - y_t^*) + \beta (i_t - i_t^*)$$
- $\text{Spot rate\%} = \text{(money supply differential\%)} - \text{alpha * (income level differential\%)} * \text{beta (interest rate differential\%)}$
- S (spot rate) increases → fx rate has increased → domestic currency is weakening
- M (domestic money supply) increases → uk govt is printing money → S increases
- M* (foreign money supply) increases → foreign govt printing money → S decreases
- Y (income) increases → people get richer → S decreases
	- 1% increase in Y leads to an “alpha” % increase in the spot rate
- Y* increases → foreign ppl get richer → S increases
- I (interest rate) increases → higher rates → S increases → currency weakens
	- Interest rate logic → interest rates try to match inflation at same horizon
		- Anything above inflation rate → real interest rate
		- Interest rate = inflation rate + interest component
		- Interest rates and inflation are related → increasing rate suggest increasing inflation → S increases → home currency weakens

**Simple Fair Value Model**
$$\Delta_k s_{t+k} = \alpha + \beta_k (z_t - s_t) + u_{t+k}$$
- Logic
	- The k period ahead % change in the exchange rate = gap between the % current for value of the rate and the current % spot rate
where:
- $z_t = \underbrace{(m_t - m_t^*) - \gamma (y_t - y_t^*)}_{\text{fundamentals giving fair value}}$




## Asset Approach
- These are forward looking models (future expectations enter the models)

**FPPM With Fundamentals**
$$ s_t = z_t + \beta (s_{t+1}^e - s_t) \hspace{1cm} \text{OR} \hspace{1cm} s_t = \frac{1}{1 + \beta} z_t + \frac{\beta}{1 + \beta} s_{t+1}^e$$
- Principle: value of the currency today represents the value of it's future fundamentals (money supply, income, interest rates)
	- *Today’s exchange rate is weighted average of future fundamentals + what we think the currency will be worth next period*
- $\beta$ is sensitivity of money demand to interest rates
- $z_t$ is as before the fundamentals giving fair value

**News Approach (Asset Approach)**
$$s_t = \frac{1}{1 + \beta} \sum_{j=0}^{\infty} \left( \textcolor{red}{\frac{\beta}{1 + \beta}} \right)^j \textcolor{orange}{z_{t+j}^e}$$
- Principle: todays exchange rate is the sum of all future fundementals
- Red: discount factor for all future fundamentals with $\beta$ as the sensitivity of money demand to interest rates
- Incorporates [[Uncovered Interest Rate Parity]]



## Meese and Rogoff Model Testing
- Found that out of all models, the best predictor was a random walk:
- ![[Pasted image 20240622172744.png]]

