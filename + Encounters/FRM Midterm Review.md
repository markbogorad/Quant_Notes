# FRM Midterm Detailed Solutions
### Question 3
- Key to the problem: recall that historic Sharpe ratio (Global Market Risk Premium aka GMRP) is 0.30. A value of 0.28 would also be acceptable (research by Goodall, Manzini, and Rose (1999)). After that, its a simple application of the **Singer and Terhaar model.**
	- *Details in pg. 36-45 in capital market expectations slide deck* 
1) Derive market risk premia (**integrated markets**) as $RP = \sigma_i \cdot \rho_i \cdot \text{Sharpe Ratio of the Global Market}$
	- **Remember:** risk premium depends on volatility (standard deviation) and correlation with the market
	- $\sigma_i$ is the standard deviation of the asset (given as 7% for bonds and 17% for equities)
	- $p_i$ is the correlation of the asset with the market (0.54 for bonds and 0.70 for equities)
	- Sharpe ratio is your assumption (0.30 or 0.28)
	- **For Canadian Bonds**
		- $RP_{\text{Bonds}} = 7\% \cdot 0.54 \cdot 0.30 = 1.134\%$
	- **For Canadian Equities**
		- $RP_{\text{Equities}} = 17\% \cdot 0.70 \cdot 0.30 = 3.57\%$
	
2) Derive risk premia for **completely segmented** markets 
	- Degree of segmentation is given as $0.80$ for both markets
		- **What is a segmented market?:** Think of this as a closed economy, where assets will never interact with global factors (i.e. degree of segmentation is 0)
	- For completely segmented markets ($\omega = 0)$, the risk premium is:
		- $RP = \sigma_i \cdot \text{Sharpe Ratio of the Global Market}$
			- *This is the same formula just the degree of integration is 0 as the markets are completely segmented*
	- **Canadian Bonds:** 
		- $RP_{\text{Bonds}} = 7\% \cdot 0.30 = 2.1\%$
	- **Canadian Equities:** 
		- $RP_{\text{Equities}} = 17\% \cdot 0.30 = 5.1\%$

3) Derive risk premia for **integrated** markets to get expected returns
	- This is where **Singer and Terharr** come in (weights are given)
	$$RP = \omega \cdot RP_{\text{Integrated}} + (1 - \omega) \cdot RP_{\text{Segmented}}$$
	-  Canadian Bonds: $RP_{\text{Bonds}} = (0.8 \cdot 1.134\%) + (0.2 \cdot 2.1\%)$
		- $RP_{\text{Bonds}} = 0.9072\% + 0.42\% = 1.3272\%\approx 1.33\%$
	- Canadian Equities: $RP_{\text{Equities}} = (0.8 \cdot 3.57\%) + (0.2 \cdot 5.1\%)$
		- $RP_{\text{Equities}} = 2.856\% + 1.02\% = 3.876\% \approx 3.88\%$

4) Add the risk free rate to integrated market figures
	- **Why?** - Think of any returns as a mix of a risk free rate and a premium for investing in that specific asset (CAPM framework). Under this logic, all returns can be decomposed into the returns one should get no matter what (risk free returns) and then extra return for taking specific risk in the asset class you invest in.
	- This actual figure is based off an assumption, so anything around 3-4% is valid (4% in solution set)

> In summary: get the integrated risk premia, get the segmented risk premia, use Singer and Terhaar, add the risk free rate.

*In practice, this is useful for investing into emerging markets, where some economies are more closed off (some fully closed off) than others.*



### Question 6
*Where to find details on this on Brightspace?:  "Introduction to Swap and Derivatives Chance Textbook Reference" -> derivative_session_hedging_with_futures -> slides 6-25*
#### A)
> For this part the key is to use the formula (definitely have this on your formula sheet) and to recognize that the reduction from 70-30 to 60-40 (% bonds-stock respectively) generates a transaction of 10 million synthetically sold stock and 10 million purchased bonds $(V)$

$$N_{\text{futures}} = \frac{(T - C) \cdot V}{F \cdot \beta \ (\text{for stocks}) \ \text{or} \ D \ (\text{for bonds})}$$
		- T: Target beta (for stocks) or target duration (for bonds).
		- C: Current beta (for stocks) or current duration (for bonds).
		- V: Value of the portfolio segment to be adjusted.
		- F: Futures contract price.
		- $β$: Beta of the futures contract (for stocks).
		- D: Modified duration of the futures contract (for bonds).
	
- **Determine stock futures**
	- $N_{\text{futures, stocks}} = \frac{(0 - 1.05) \cdot \$10,000,000}{0.98 \cdot 280,000} = -38.27 \ (\text{round to } -38 \ \text{contracts (short)})$
- **Determine bond futures**
	- $N_{\text{futures, bonds}} = \frac{(5.5 - 0.25) \cdot \$10,000,000}{6.5 \cdot 125,000} = 64.62 \ (\text{round to } 65 \ \text{contracts (long)})$
- Adjust Beta and Duration (same formula):
	- **Beta:**
		- $N_{\text{futures}} = \frac{(1.00 - 1.05) \cdot \$60,000,000}{0.98 \cdot 280,000}$
		- $N_{\text{futures}} = -10.93 \ (\text{round to -11 contracts})$
	- **Duration:**
		- $N_{\text{futures}} = \frac{(5.0 - 5.5) \cdot \$40,000,000}{6.5 \cdot 125,000}$
		- $N_{\text{futures}} = -24.62 \ (\text{round to -25 contracts})$
- Finally, calculate net positions:
	- **Sell:** $-38 - 11$  =  Sell (short) 49 Contracts
	- **Buy:** $65 -25$  = Buy 40 Contracts
#### B)
> Analyze the changes by portfolio. Nothing more than knowing where to apply which formulas

- Stock portfolio
	- $\text{New Stock Value} = \$70,000,000 \cdot (1 - 0.03) = \$67,900,000$
		- 3% drop
	- $\text{Profit} = -49 \cdot (\$272,160 - \$280,000) = -49 \cdot (-\$7,840) = \$384,160$
		- $\text{Net Position} \times \text{Change in Portfolio Value}$
	- $\text{Total Stock Position} = \$67,900,000 + \$384,160 = \$68,284,160$
	
- Bond portfolio
	- $\text{New Bond Value} = \$30,000,000 \cdot (1 + 0.01) = \$30,300,000$
		- 1% increase
	- $\text{Profit} = 40 \cdot (\$126,500 - \$125,000) = 40 \cdot \$1,500 = \$60,000$
		- Same as before: $\text{Net Position} \times \text{Change in Portfolio Value}$
	- $\text{Total Bond Position} = \$30,300,000 + \$60,000 = \$30,360,000$
	
- Final portfolio value 
	- $\text{Total Portfolio Value} = \$68,284,160 + \$30,360,000 = \$98,644,160$
	
- Compare with transactions done with securities themselves
	- What does this mean?: instead of using **futures contracts** to adjust the portfolio, the investor directly **buys or sells the underlying assets**. This requires cash upfront whereas futures are on margin - this will make portfolio adjustments with futures cheaper most of the time. 
		- $\text{Stock Value} = \$60,000,000 \cdot (1 - 0.03) = \$58,200,000$
		- $\text{Bond Value} = \$40,000,000 \cdot (1 + 0.01) = \$40,400,000$
		- $\text{Total Value} = \$58,200,000 + \$40,400,000 = \$98,600,000$
	- $\$98,644,160 - \$98,600,000 = \$44,160 \ (\approx 0.044\% \ \text{of portfolio value})$


### Question 7
> *Where to find details on this on Brightspace?: "Introduction to Swap and Derivatives Chance Textbook Reference" -> Hedging_with_Options_Swaps -> slides 27-29*
#### A)
- Determine durations of the **2 fixed to floating swaps**
- 3 key formulas here
	- **Duration of a floating bond**
		- $\text{Duration (floating)} = \frac{\text{Payment Interval}}{2}$
		- Where Payment IntervalPayment Interval is the time between payments (e.g., 1/12 for monthly, 1/2 for semiannual).
	- **Duration of a fixed bond**
		- $\text{Duration (fixed)} = \text{Percent of Maturity (0.75)} \cdot \text{Maturity}$
	- **Duration of a swap**
		- $\text{Duration (swap)} = \text{Duration (floating)} - \text{Duration (fixed)}$

- **1 year swap with monthly payments**
	- $\text{Duration (floating)} = \frac{\text{Payment Interval}}{2}= \frac{1/12}{2} = 0.042$ 
	- $\text{Duration (fixed)} = 0.75 \cdot 1 = 0.75$
	- $\text{Duration (swap)} = 0.042 - 0.75 = -0.708$
- **2 year swap with semi-annual payments**
	- $\text{Duration (floating)} = \frac{\text{Payment Interval}}{2} = \frac{1/2}{2} = 0.25$
	- $\text{Duration (fixed)} = 0.75 \cdot 2 = 1.50$
	- $\text{Duration (swap)} = 0.25 - 1.50 = -1.25$
#### B)
- Choose the longer (more negative) duration swap
	- $-1.25$ in this case
- Apply formula for notional principal
	- $NP = B \cdot \frac{\text{MDUR}_{T} - \text{MDUR}_{B}}{\text{MDUR}_{S}}$
	- $NP = 250,000,000 \cdot \frac{4.50 - 5.50}{-1.25}$
	- $NP = 250,000,000 \cdot \frac{-1.00}{-1.25}$
	- $NP = 250,000,000 \cdot 0.80 = 200,000,000$
- **Explaination:**
	- This means a notional principal of $200 million in the two-year pay-fixed, receive-floating swap is required to reduce the duration to the target level.
	- The swap's duration determines its impact on the portfolio. The larger the absolute value of the swap’s duration (e.g., $−1.25$ for the two-year swap vs. $−0.708$ for the one-year swap), the more effective the swap is at adjusting the portfolio duration.
	- The longer absolute duration swap is chosen to maximize efficiency, and the notional principal ensures the desired adjustment in the portfolio’s duration.


### Question 9
> *Where to find details on this on Brightspace?:  "Introduction to Swap and Derivatives Chance Textbook Reference" -> derivative_session_swaps -> slides 26-29*
#### A)
- **What the Company Wants:** The company wants the flexibility to **enter into a swap as a fixed-rate payer** (to convert the floating-rate loan into a fixed-rate loan).
- **Type of Swaption:** A **payer swaption** gives the company the right, but not the obligation, to enter into a swap where it **pays a fixed rate** and **receives a floating rate**.
- **Should the Company Buy or Sell the Swaption?**: The company should **buy the payer swaption** because it wants the option to lock in a fixed rate if the swap rate becomes attractive (greater than the exercise rate).
#### B)
>*My advice for questions like these - the hardest part here is not getting lost in the intermediary calculations. The best way to prep for these in the future is just to practice working with similar problems a lot.*

Generalized cash flow formulas
- If Swap Rate $( FS > \text{Exercise Rate}$ : 
	- $\text{Net Cash Flow} = \text{Exercise Rate} \cdot \text{Notional Principal}$
- If Swap Rate $( FS \leq \text{Exercise Rate})$ :
	- $\text{Net Cash Flow} = FS \cdot \text{Notional Principal}$
	
- $\textbf{Case 1:} (FS(2,7) > 6.5\%)$
	- The company exercises the swaption to lock in a fixed rate of **6.5%**
	- Cash flow on swap
		- The company **pays the fixed market rate** $FS(2,7)$ on $10 million:
			- Pay: $0.065 \cdot 10,000,000 = 650,000$ on swap
		- The company **receives LIBOR (L)** on $10 million:
			- Receive: $(L \cdot 10,000,000)$ on swap
	- Cash flow on loan
		- The company **pays LIBOR (L)** on $10 million:
			- Pay: $(L \cdot 10,000,000)$ on loan
	- Net cash flow
		- Again, the LIBOR payments cancel out, leaving the company with the fixed payment from the new swap:
			- Net Payment: $650,000$

- $\textbf{Case 2:} (FS(2,7) \leq 6.5\%)$
	- The company does not exercise the swaption because the swap rate is lower than the exercise rate. Instead, it enters into a new swap at the market rate $FS(2,7)$.
	- Cash flow on swap
		- Pay: $(FS(2,7) \cdot 10,000,000)$ on swap
		- Receive: $(L \cdot 10,000,000)$ on swap
	- Cash flow on loan
		- Pay: $(L \cdot 10,000,000)$ on loan
	- Net cash flow
		- Net Payment: $(FS(2,7) \cdot 10,000,000)$
		- Note: This is less than $\$650,000$
#### C)
- The original solution set explains this fairly well:
	- At this point, the swaption (payer swaption) is **in-the-money**, meaning the fixed swap rate in the market is higher than the exercise rate (6.5%).
	- Since the company no longer wants to enter into the swap, it has two options:
	- **Do Nothing:** Simply let the swaption expire. However, this would waste the value of the swaption, especially because it’s in-the-money.
	- **Sell the Swaption (Best Option):**
	    - The company can sell the swaption in the market to another party.
	    - By selling it, the company can capture its **intrinsic value**, which is the difference between the market swap rate and the exercise rate.
	    - This way, the company doesn’t exercise the swaption but still gains financial value from it.
	- **Why Sell Instead of Letting It Expire?**
		- The swaption has value because the market swap rate is higher than the exercise rate.
		- Selling it allows the company to recover some money instead of losing the premium it paid to buy the swaption.

### Question 11
*Where to find details on this on Brightspace?:  "Introduction to Swap and Derivatives Chance Textbook Reference" -> derivative_session_hedging_with_futures -> slides 4 and 5.*
#### Pre Solution Steps
- Compound the premium
	- The loan will not be issued until 65 days from now, so we need add a premium for the foregone opportunity cost of these 65 days
	- General formula: $\text{Effective Premium} = \text{Premium} \cdot \left[ 1 + (\text{Current LIBOR} + \text{Spread}) \cdot \frac{\text{Days}}{360} \right]$
	- $\text{Effective Premium} = 475,000 \cdot \left[ 1 + (0.07125 + 0.01) \cdot \frac{65}{360} \right] = 475,000 \cdot 1.014640625 = 481,968$
- Derive the total outlay
	- SBT’s total outlay includes the loan amount ($100 million) plus the compounded premium:
		- $\text{Total Outlay} = 100,000,000 + 481,968 = 100,481,968$
- Total outlay will be in the effective annual rate calculation:
$$\text{EAR} = \left( \frac{\text{Total Outlay} + \text{Total Loan Interest}}{\text{Total Outlay}} \right)^{\frac{365}{182}} - 1$$
#### I) 180 Day ATM Option @ 9%
- Calculate total interest
	- $\text{Loan Interest} = \text{Loan Amount} \cdot \text{Loan Rate} \cdot \frac{\text{Loan Term (Days)}}{360}$
	- $\text{Loan Interest} = 100,000,000 \cdot 0.10 \cdot \frac{182}{360} = 5,055,556$
- Apply EAR formula
$$\text{EAR} = \left( \frac{100,481,968 + 5,055,556}{100,481,968} \right)^{\frac{365}{182}} - 1 \left( 1.0503 \right)^2 - 1 \approx 0.0934 = 9.34\%$$
#### II) 180 Day ATM Option @ 5%
- Calculate total interest
	- $\text{Loan Interest} = \text{Loan Amount} \cdot \text{Loan Rate} \cdot \frac{\text{Loan Term (Days)}}{360}$
	- $\text{Loan Interest} = 100,000,000 \cdot 0.06 \cdot \frac{182}{360} = 3,033,333$
- Apply EAR formula
$$\text{EAR} = \left( \frac{100,481,968 + 4,044,444}{100,481,968} \right)^{\frac{365}{182}} - 1 = \left( 1.0403 \right)^2 - 1 \approx 0.0724 = 7.24\%$$

- *Why does one of the formulas use 360 and the other 365?*
	- Loan Interest Calculation: Uses 360 days because the loan is based on LIBOR, which follows the 360-day convention (given in problem)
	- Effective Annual Rate (EAR): Uses 365 days because it expresses the total cost of borrowing (including interest and premium) in a full calendar year.