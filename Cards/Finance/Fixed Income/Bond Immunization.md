up:: [[Fixed Income MOC]]
tags:: #Finance
# Immunization
- An [[Interest Rate Risk]] protection strategy
	- Goal: ensure portfolio reaches a certain return, regardless of interest rate changes
- *Logic: essentially use reinvestment risk to offset the interest rate risk*
	- If interest rates increase: bond price drop is negated by higher [[Reinvestment Income]]
	- If interest rates drop: bond price increase is slowed down by decrease in reinvestment income
- Maturity < investment horizon → interest rate risk
- Maturity > investment horizon → reinvestment risk + interest rate risk
- Maturity = investment horizon → reinvestment risk
- Maturity = investment horizon and duration → no risk

## Strategy
- Match the Macaulay duration with time to maturity [[Duration Model]]
$$ D_p = \sum_{i=1}^{m} w_i \cdot D_i $$
- Portfolio duration = sum of all weights * their individual durations
- This should equal the investment horizon