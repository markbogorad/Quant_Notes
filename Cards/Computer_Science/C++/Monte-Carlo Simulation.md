up:: [[Derivatives MOC]], [[Option Pricing C++]]
tags:: #Programming #Finance 
# Monte Carlo Pricing Method
For C++, see: [[Monte-Carlo Simulation C++]]
- Not very efficient (slow)
- Not very accurate
	- More accuracy --> more simulations --> less efficiency (more time)
## Pros
- Applicable to wide range of problems
- Easy to understand
- Useful as a secondary opinion with other methods (like FDM)
## Cons
- Applicability breaks down
	- For option sensitivities, early exercise, etc
- Lack of predictable accuracy
	- If you increase number of repetitions (simulations), you won't necessarily get better accuracy
- Very slow
	- Solving a FDM per simulation --> lot of work