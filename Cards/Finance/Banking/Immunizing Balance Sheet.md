up:: [[Banking MOC]]
tags:: #Finance 
# Immunizing Balance Sheet
- [[Interest Rate Risk]] management strategy
- Intentionally structuring assets and liabilities so that changes in interest rates do not affect the portfolio significantly
	- Done by matching Macaulay durations of assets and liabilities [[Duration Model]]
- Maintained via periodic rebalancing
- Derivatives are used here [[Derivatives MOC]]
	- Interest rate swaps: convert fixed rate to floating or vice versa to modify duration
	- Options
	- Futures
## Immunization Formulae
- These measure the impact of certain factors on the balance sheet
**% Change in the price of the security**
$$\Delta P = -D \times P \times \frac{\Delta R}{(1+R)} $$
- **ΔP**: Change in the price of the underlying
- **D**: Duration 
- **P**: Price of underlying
- **ΔR** Change in interest rate.
- **R**: Initial interest rate.

**% Change in assets**
$$\Delta A = -D_A \times A \times \frac{\Delta R}{(1+R)}$$
- **ΔA**: Change in the value of assets.
- **DA​**: Duration of assets.
- **A**: Total value of assets.

**% Change in liabilities**
$$\Delta L = -D_L \times L \times \frac{\Delta R}{(1+R)}$$
- **ΔL**: Change in the value of liabilities.
- **DL​**: Duration of liabilities.
- **L**: Total value of liabilities.
   
**% Change in equity**
$$\Delta E = [-D_A \times A + D_L \times L] \frac{\Delta R}{(1+R)}$$
**% Alternative form of change in equity**
$$\Delta E = [-D_A - D_L \times k] \times A \left( \frac{\Delta R}{(1+R)} \right) \quad \text{with } k = \frac{L}{A}
$$
- **ΔE**: Change in equity (net worth).

### Concluding Relationships
**Leverage Adjusted Duration Gap**:  Da - ( DL * K)
**Size of FI**: A
**Interest Rate Shock:** ΔR/(1+R)