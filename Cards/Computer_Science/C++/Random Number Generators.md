up:: [[BOOST]]
tags:: #Programming 
# Random Number Generators (RNGs)
## Usage
- From Paul Lopez on QuantNet
-  [[Monte-Carlo Simulation]] 
	- Monte Carlo simulations are widely used in quantitative finance for various purposes, such as pricing financial derivatives, risk assessment, and portfolio optimization. 
	- These simulations involve generating a large number of random scenarios to estimate the distribution of possible outcomes
	- In options pricing, Monte Carlo simulations are commonly used to estimate the fair value of complex financial derivatives.
		- **boost::mt19937** is widely employed in such simulations to generate random paths for underlying asset prices and calculate option payoffs.
- Backtesting and historical simulations
	- Backtesting involves simulating trading strategies on historical market data to evaluate their performance. 
	- Historical simulations rely on generating random sequences that closely resemble the statistical properties of real market data.
		- **boost::mt19937** is often utilized in portfolio optimization algorithms to generate random return scenarios and assess the robustness of optimization results.
- Risk management
	-  In quantitative finance, risk management involves assessing and quantifying various types of financial risks, such as market risk, credit risk, and liquidity risk. 
	- Random number generators are used in risk models to simulate potential future scenarios and estimate risk measures
	- In Value at Risk (VaR) calculations, random number generators are employed to simulate potential losses in a portfolio over a specified time horizon.
		- **boost::mt19937** is commonly used in VaR models to generate random market scenarios and estimate the distribution of potential losses.
- High Frequency Trading (HFT)
	- High-frequency trading (HFT) algorithms rely on fast and efficient generation of random numbers for various purposes, such as order placement, execution, and market data analysis. 
	- In HFT, the performance of the PRNG is critical, as even small delays can have significant impact on trading outcomes. boost::mt19937 is often preferred in HFT applications due to its fast generation speed and good statistical properties.
- Portfolio management
	- In portfolio optimization, random number generators are used to simulate future asset returns and optimize portfolio allocations.
## Pseudo RNG (PRNG)
- Use deterministic algos to generate a sequence that appears random
- In reality, the sequence is determined by the **seed**, the initial value of the sequence
- Some points:
	- Generates RNGs faster
	- Useful for debugging and other moments where consistent results are required
	- Used when absolute predictability isn't necessary
#### Seed
- Starting point of the sequence
- When you initialize a PRNG with a seed, the generator uses this seed as the basis for producing the first number in the sequence. 
	- Subsequent numbers are generated based on the algorithm's internal state, which evolves as the generator produces new numbers. 
	- The algorithm's design ensures that the sequence appears random despite being entirely determined by the initial seed.
## True RNG (TRNG)
- Fully unpredictable generators
	- Based on quantum phenomena or thermal noise
	- Don't use a deterministic algo
- No **seed** necessary
- Used in cryptography
	- "The practice and study of techniques for secure communication in the presence of adversarial behavior"
		- Encrypting stuff
### In general:
- **For simulations and general-purpose applications** where speed and reproducibility are important, PRNGs are often sufficient.
- **For high security**, such as in cryptography, TRNGs are preferred due to their unpredictability.
## Types of PRNGs
### Mersenne Twister (boost::mt19937)
- **Most commonly used**
- Exceptionally long period (2^19937 - 1) --> significantly more than lagged fibonacci
	- **Long period:** can generate much more unique sequences before repeating itself
- Excellent **statistical qualities**
	- High degree of equidistribution
	- Widely regarded as one of the best general-purpose PRNGs available
- **High speed:** faster than lagged fibonacci
	-  Has a small state size compared to its long period
- Not suitable for **cryptographic** purposes
- Applications of Mersenne Twister (Paul Lopez)
	- Monte-Carlo Simulation:
		- "The **statistical properties and randomness** of the PRNG are crucial in MC simulation. 
		- boost::mt19937, with its excellent statistical qualities and long period, is often preferred for Monte Carlo simulations in quantitative finance."
	- Backtesting & historical simulations
		- The choice of PRNG can impact the **accuracy and reliability** of backtesting results. 
		- boost::mt19937 is commonly used in backtesting and historical simulations due to its ability to generate high-quality random sequences that mimic real-world market behavior.
	- Risk Management
		- The choice of PRNG can affect the **accuracy and stability** of risk calculations. 
		- boost::mt19937, with its robust statistical properties, is often employed in risk management applications to ensure reliable risk estimates.
	- HFT
		- In HFT, the performance of the PRNG is critical, as even **small delays** can have significant impact on trading outcomes. 
		- boost::mt19937 is often preferred in HFT applications due to its fast generation speed and good statistical properties.
### Lagged Fibonacci (boost::lagged_fibonacci607)
- Very long period as well 
- Trumped by Mersenne Twister
-  Not suitable for **cryptographic** purposes
## RNG Exercise from QuantNet
- ![[Screenshot 2024-03-24 at 12.22.37 PM.png]]
```
#include <boost/random/mersenne_twister.hpp>
#include <boost/random/uniform_int_distribution.hpp>
#include <map>
#include <iostream>
#include <ctime>

// Mersenne Twister random number generator
	boost::random::mt19937 myRng;

int main() {

// Set the seed
	myRng.seed(static_cast<boost::uint32_t>(std::time(0)));

// Uniform distribution in range [1,6]
	boost::random::uniform_int_distribution<int> six(1, 6);

	std::map<int, long> statistics; // Structure to hold outcome frequencies
	int outcome; // Current outcome
	long trials; // Number of trials

	std::cout << "How many trials? ";
	std::cin >> trials;

for (long i = 0; i < trials; ++i) {
	outcome = six(myRng); // Generate outcome
	statistics[outcome]++; // Tally outcome
}

// Output the results
	for (int i = 1; i <= 6; ++i) {
		std::cout << "Trial " << i << " has "
		<< static_cast<double>(statistics[i]) / trials * 100
		<< "% outcomes\n";
}

return 0;

}
```

back:: [[BOOST]]