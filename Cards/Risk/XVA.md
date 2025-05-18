up:: [[Risk Management MOC]]
tags:: #Finance 
# XVA
- Represents a set of adjustments to risk-neutral valuations (PV of cashflows) of financial instruments, to account for real-world market frictions, credit risk, funding costs, and regulatory capital.
- Moving from risk neutral valuation from real valuation (what you can actually put back into the market)
- [[CVA]]
- [[DVA]]
- [[FVA]]
	- [[FVA-C (COLVA)]]
- [[MVA]]
- [[KVA]]
## TLDR
- **Fair value = Risk-neutral valuation – CVA + DVA**
- **CVA ≈ CDS price on floating exposure**
- CVA only adjusts for **positive exposures**
- DVA represents **benefit from your own potential default**
- FVA reflects **trader’s cost of funding a trade**
- MVA = cost of posting initial margin at CCP
- KVA = expected return on capital **not deployable elsewhere**