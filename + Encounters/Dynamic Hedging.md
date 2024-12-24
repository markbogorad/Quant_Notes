up:: [[Home]]
tags:: #MOC 
# Ideas
- Greek price - time graphs
	- Delta, gamma, vega?
- Maybe price - time graphs of overall positions
- Benchmarks for hedging
	- Compare to minimum variance hedge ratio or static hedge ratio
# Dynamic Hedging
- Optimizing hedge ratios in response to market conditions
	- Hedge ratio -> % of the position that should be hedged to protect against a certain level of risk
		- This number changes as other factors change - hence dynamic hedging
	- #### Example of a hedge ratio
		- Suppose you are an airline looking to hedge your fuel costs. You anticipate needing 1,000 barrels of jet fuel, and the fuel price tends to move with crude oil. You might use crude oil futures to hedge your exposure. If a price change of 1% in crude oil futures corresponds to a 0.8% change in jet fuel prices, the hedge ratio would be 0.8. Therefore, you’d take a futures position equivalent to 800 barrels to hedge the risk associated with 1,000 barrels of jet fuel.
- Areas used in
	- market risk
	- volatility risk
	- interest rate risk
	- liquidity risk
## AI Technique Used
- Reinforcement learning most popular
	- Q learning
	- Deep Q networks
	- Policy gradient methods
	- proximal policy optimization
- Neural Networks
	- LSTM
	- RNN
- Support vector machines
- Decision trees
- 
## Anticipated Benefits
## Associated Risks
## Challenges
- Transaction cost to perfect hedging ratio via frequency of trading
	- The more you trade to try and nail a perfect delta neutral position, the more transaction costs you incur
- Cross hedges
	- How correlated are these and under what circumstances are they not?
	- Could use some pairs trading related strats here
- Slippage on larger hedges



## Data Set
- Options data
	- Ex: hedging SPY
		- would need SPY, SPY option chain (calls/puts across varying strikes), greeks, implied volatility, and option premiums
- FX data
- Interest rates
- Commodity/energy hedging
	- Would also include macroeconomic variables
- Equities (beta hedging)
- Minimum variance hedging (futures)


## Hands on Exercise


# Things to decide
- What market will we focus on (dataset to work with) and who's POV are we looking from (buy side vs sell side)
	- 2nd meeting could be after we all work with data we choose
	- **DATA IS MOST IMPORTANT FOR STEP 1**
- Are we going to be sort of just documenting the approches, how they've worked, etc... or do we want to actually make a final product that dynamically hedges using an ML algo?
- Are we going to be working on finding an optimal hedge ratio (most likely RL) or to forecast future prices and dynamically hedge with that information (say using LSTMs)



## Ideas
- Forecasting parameter and using forecast to make an optimal hedging decision




### Matt references
- slide deck 4 pgs 68-77
	- Cross sectional factor model approach
	- stacks and unstacks the data
		- Stack data -> run model -> mack prediction -> unstack data -> calculate trading systems daily returns
- Week 5 50-54
	- Another factor model that uses time series data but as a cross sectional approach
	- This regression model becomes cross-sectional because the βi​(s) parameters (factor loadings) are specific to each stock s, meaning that **the regression equation applies to multiple stocks at the same point in time.** 
		- Runnong a regression individually for each stock across many stocks
		- You are examining the **exposure of multiple stocks** on the same time series factors
		- you essentially derive a **cross-sectional mapping** of how stocks relate to the common time-series factors at that time.
	- In dynamic hedging:
		- By running this regression periodically (e.g., daily or weekly), you can update the estimated βi​(s) values and adjust your hedges accordingly.
		- Example: If the sensitivity to a volatility factor (Factorvol​(t)) increases for a stock, you might need to adjust the number of options or VIX futures in your hedging portfolio.
- Week 8 pg 41 - 56
	- Same stacking and unstacking approach under a RF

## Write up guidelines
**Write-up of a Case Study Leveraging AI to Solve a Finance Problem**
    - **AI Technique Used**: Detail the specific AI methods or algorithms you have chosen and explain why they are suitable for the problem.
    - **Anticipated Benefits**: Discuss the expected positive outcomes, such as increased efficiency, cost savings, or improved customer experience.
    - **Associated Risks**: Identify potential risks, including ethical considerations, data privacy issues, or implementation challenges.
    - **Challenges Faced**: Reflect on any obstacles encountered during your project and how you addressed them.
 **Data Set Underlying the AI Model**
    - Provide a thorough description of the dataset you are using, including its source, structure, and any preprocessing steps you have performed. If you are not able to find real data, please generate your own synthetic data and explain the generation process.
**Practical Hands-On Exercise**
	- Take a very simple example, similarly to what we usually do in the classroom, to illustrate your case by hand and provide a sample code for it.
#### Grading
- **Complete Code Submission: 15%**
- **Final Report: 25%**  
    Must include a detailed account of each member's contributions.
- **15-Minute Presentation: 10%**

## RL Approach
### Pseudocode for RL in Dynamic Hedging
```
Initialize environment:
    State = [Option Greeks, SPX price, Volatility, Portfolio Value] # BS features, Greeks, portfolio value
    Actions = [Adjust hedge positions (e.g., buy/sell SPX)]
    Reward = - (Hedging cost + P&L variance) # reward is minimizing hedge cost and risk

Initialize agent:
    Policy = Neural network mapping state to action probabilities # mechanism to decide adjustments (hardest part)
    Value Function = Neural network estimating reward for state-action pairs # forecast
    Learning Algorithm = PPO or DQN

# Training loop - simulate MKT dynamics and train the agent
For episode in range(total_episodes):
    Reset environment
    State = Initial portfolio values and market conditions

    While not terminal:
        1. Use policy to select an action:
            Action = Policy(State)
        
        2. Execute action in the environment:
            NextState, Reward = Environment.step(Action)
        
        3. Store experience (State, Action, Reward, NextState) in replay buffer
        
        4. Update policy and value function using RL algorithm:
            - Calculate TD error or policy gradient loss
            - Backpropagate to optimize networks
        
        5. Update State = NextState

# key components
State = [SPX Price, Portfolio Delta, Portfolio Gamma, Portfolio Vega, Time to Maturity]
Actions = [Buy/Sell SPX, Buy/Sell Call Options, Buy/Sell Put Options]
Reward = - (Hedging Cost + P&L Variance)

For test_episode in range(test_episodes):
    Reset environment
    Run trained policy on test market data
    Record metrics: Cumulative P&L, Hedging Cost

```

At its core, reinforcement learning (RL) in this context essentially leverages a **Markov Decision Process (MDP)** to:

1. **Model the Environment**: The environment (market dynamics) and agent interaction are represented as a Markov chain. Each state encapsulates the current market conditions (e.g., SPX price, Greeks, portfolio value, time to maturity), and transitions between states depend on the agent's actions (e.g., adjusting hedge positions).
    
2. **Optimize Decisions**: The agent learns a **policy** to decide which action to take in each state to minimize a long-term objective function (variance and hedging costs). The RL algorithm trains the Markov chain to "go in specific directions" by identifying the optimal transitions (actions) at each state.


#### Hands on Example:
- Show a Markov chain that constantly adjusts to the learning algo over each transition
	- $Q(s, a) \leftarrow Q(s, a) + \alpha \big[ R + \gamma \max_{a'} Q(s', a') - Q(s, a) \big]$
		- R: Immediate reward.
		- $\gamma$: Discount factor, representing the importance of future rewards $( 0 \leq \gamma \leq 1)$. 
		- $( \alpha)$: Learning rate, controlling the step size of the update $( 0 < \alpha \leq 1 )$
		