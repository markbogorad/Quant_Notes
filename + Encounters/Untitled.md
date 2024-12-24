## Python Option Pricing & Hedging Tool
### Introduction

After completing the C++ Programming for Financial Engineering course, I was eager to build on my knowledge and take my skills to the next level. My goal was to simplify and modularize my approach to option pricing, making the code more accessible and flexible while still retaining the computational rigor required in financial engineering. Moreover, I knew I needed to get my Python skills back into good shape for the start of my MFE program. This ambition led to the creation of the Python Option Pricing & Hedging Tool.

This project allowed me to translate the concepts I worked on in C++ into Python, a language known for its versatility and ease of use. By leveraging Python’s Streamlit library and the Black-Scholes framework, I was able to create an intuitive and interactive graphical user interface (GUI) that simplifies the complexities of option pricing. The modular design of the tool ensures that each component—whether it’s the pricing models, strategy overlays, or hedging techniques—can be easily adapted or expanded upon as needed.

One of the key features of this tool is the Strike Price vs. Volatility Analysis. In the world of options trading, the interplay between strike price and volatility is a critical factor that influences pricing decisions. This feature allows users to visually explore how varying strike prices and volatility levels affect option prices in the Black-Scholes framework, offering a deeper understanding of the market dynamics at play.

In addition to this, I’ve incorporated trading strategy overlays. These overlays provide users with the ability to visualize the payoffs of various trading strategies, such as covered calls, bull spreads, butterflies, and more. The visualizations and the heat maps help the user get a better understanding of what these positions actually look like and the intentions behind them.

To ensure a comprehensive approach to risk management, I also developed a section on Optimal Hedging Techniques. By utilizing Black-Scholes parameters, the tool calculates the neutral (0) positions for delta, gamma, vega, rho, and theta hedging. This feature is particularly valuable for those looking to mitigate risk effectively in their trading portfolios, and can be built upon in the future to auto provide these for an entire portfolio.

Drawing on the online Q/KDB+ courses at KX Academy, I integrated a live Q server into the tool, enabling real-time storage and retrieval of user inputs and option prices. This not only enhances the tool’s functionality but opens the door to a potential high-frequency data input and constant graphical monitoring of option positions through time using KDB+.

Finally, I need to give credit to some folks who inspired me to make this:

The idea for a Streamlit application came from CodingJesus on YouTube, who worked with one of his clients to develop the call-put heatmap project idea. I ran by my idea with his client, [Prudhvi Reddy](https://www.linkedin.com/in/mprudhvi/), before creating this to make sure he was alright with me using his work as inspiration. Do check out his content and LinkedIn, I believe he has another Streamlit application on VaR for those of you interested in risk applications.

The video to the project idea is [here](https://www.youtube.com/watch?v=lY-NP4X455U), it may help those of you who are interested in this come up with unique applications and additions.

### FAQ

**Q1: What are the main features of this tool?**  
**A:** The tool offers several standout features:
- **Strike Price vs. Volatility Analysis**: Understand how option prices change with varying strike prices and volatility levels.
- **Trading Strategy Overlays**: Visualize the payoffs of popular trading strategies like covered calls, bull spreads, and more.
- **Optimal Hedging Techniques**: Derive neutral positions for delta, gamma, vega, rho, and theta hedging using Black-Scholes parameters.
- **Integration with Q/Kdb+**: Utilize a live Q server for real-time storage and output of user inputs and option prices, enhancing the tool’s functionality with advanced data handling capabilities.

**Q2:  Why are out of the money strike prices not being recorded at a loss of their full purchase price at all nodes?
**A:** The essence of this project was to study the Black-Scholes framework and show how the model reacts to changes in strike price and volatility. Think of the figures more as live P/L at each point in strike and volatility. Intuitively, you are “down” the amount of money at each node rather than it being a final loss at the expiry. The point of the graph additions is to show both perspectives – a live P/L and a final expiry P/L for each trade.

**Q3: How does the Integration with Q/Kdb+ enhance the tool?**  
**A:** The integration with Q/Kdb+ allows for real-time storage and output of user inputs and option prices. This feature is particularly useful for users who need to handle large datasets or require real-time data analysis, bridging the gap between Python and Q/Kdb+.

**Q4: Where did I find $100k/year to pay for KDB+?**
**A:** KX Systems are kind enough to provide a free demo for a whole year. As an alternative, a mySQL database can do the same job, but there is more potential for this project if one searches for ways to optimize the GUI for high frequency data inputs from KDB+ in the future. Though this would likely require migration away from Streamlit and investing into something more serious to keep up with the speed.

**Q5: What do I think can be built on to improve the project?**
**A:** The optimal hedging section can be built upon to handle the trading strategies or even larger option portfolios in a more modularized way. A deeper dive into the KDB+ integration likely has the most potential for really cool additions. Speed of the algorithm can certainly be improved.

**Q6:** What are the requirements for the project to run?
**A:**
- streamlit==1.12.0
- pandas==1.5.3
- numpy==1.23.5
- scipy==1.10.0
- matplotlib==3.7.1
- seaborn==0.12.2
- qpython

---

## Python Option Pricing & Hedging Tool

### Introduction

After completing the C++ Programming for Financial Engineering course, I was eager to build on my knowledge and take my skills to the next level. My goal was to simplify and modularize my approach to option pricing, making the code more accessible and flexible while still retaining the computational rigor required in financial engineering. Moreover, I knew I needed to get my Python skills back into good shape for the start of my MFE program. This ambition led to the creation of the Python Option Pricing & Hedging Tool.

This project allowed me to translate the concepts I worked on in C++ into Python, a language known for its versatility and ease of use. By leveraging Python’s Streamlit library and the Black-Scholes framework, I was able to create an intuitive and interactive graphical user interface (GUI) that simplifies the complexities of option pricing. The modular design of the tool ensures that each component—whether it’s the pricing models, strategy overlays, or hedging techniques—can be easily adapted or expanded upon as needed.

One of the key features of this tool is the **Strike Price vs. Volatility Analysis**. In the world of options trading, the interplay between strike price and volatility is a critical factor that influences pricing decisions. This feature allows users to visually explore how varying strike prices and volatility levels affect option prices in the Black-Scholes framework, offering a deeper understanding of the market dynamics at play.

In addition to this, I’ve incorporated **Trading Strategy Overlays**. These overlays provide users with the ability to visualize the payoffs of various trading strategies, such as covered calls, bull spreads, butterflies, and more. The visualizations and heat maps help users gain a better understanding of what these positions actually look like and the intentions behind them.

To ensure a comprehensive approach to risk management, I also developed a section on **Optimal Hedging Techniques**. By utilizing Black-Scholes parameters, the tool calculates the neutral (0) positions for delta, gamma, vega, rho, and theta hedging. This feature is particularly valuable for those looking to mitigate risk effectively in their trading portfolios, and it can be expanded in the future to automate these calculations for an entire portfolio.

Drawing on the online Q/Kdb+ courses at KX Academy, I integrated a live Q server into the tool, enabling real-time storage and retrieval of user inputs and option prices. This not only enhances the tool’s functionality but also opens the door to potential high-frequency data input and constant graphical monitoring of option positions over time using Kdb+.

Finally, I need to give credit to some folks who inspired me to make this:

The idea for a Streamlit application came from CodingJesus on YouTube, who worked with one of his clients to develop the call-put heatmap project idea. I ran my idea by his client, [Prudhvi Reddy](https://www.linkedin.com/in/mprudhvi/), before creating this to ensure he was okay with me using his work as inspiration. Do check out his content and LinkedIn—I believe he has another Streamlit application on VaR for those interested in risk applications.

The video to the project idea is [here](https://www.youtube.com/watch?v=lY-NP4X455U); it may help those of you interested in this area come up with unique applications and additions.

### FAQ

**Q1: What are the main features of this tool?**  
**A:** The tool offers several standout features:
- **Strike Price vs. Volatility Analysis**: Understand how option prices change with varying strike prices and volatility levels.
- **Trading Strategy Overlays**: Visualize the payoffs of popular trading strategies like covered calls, bull spreads, and more.
- **Optimal Hedging Techniques**: Derive neutral positions for delta, gamma, vega, rho, and theta hedging using Black-Scholes parameters.
- **Integration with Q/Kdb+**: Utilize a live Q server for real-time storage and output of user inputs and option prices, enhancing the tool’s functionality with advanced data handling capabilities.

**Q2: Why are out-of-the-money strike prices not being recorded at a loss of their full purchase price at all nodes?**  
**A:** The essence of this project was to study the Black-Scholes framework and show how the model reacts to changes in strike price and volatility. Think of the figures more as live P/L at each point in strike and volatility. Intuitively, you are “down” the amount of money at each node rather than it being a final loss at expiry. The point of the graph additions is to show both perspectives—a live P/L and a final expiry P/L for each trade.

**Q3: How does the Integration with Q/Kdb+ enhance the tool?**  
**A:** The integration with Q/Kdb+ allows for real-time storage and output of user inputs and option prices. This feature is particularly useful for users who need to handle large datasets or require real-time data analysis, bridging the gap between Python and Q/Kdb+.

**Q4: Where did I find $100k/year to pay for Kdb+?**  
**A:** KX Systems are kind enough to provide a free demo for a whole year. As an alternative, a MySQL database can do the same job, but there is more potential for this project if one searches for ways to optimize the GUI for high-frequency data inputs from Kdb+ in the future. Though this would likely require migrating away from Streamlit and investing in something more robust to keep up with the speed.

**Q5: What do I think can be built on to improve the project?**  
**A:** The optimal hedging section can be built upon to handle trading strategies or even larger option portfolios in a more modularized way. A deeper dive into the Kdb+ integration likely has the most potential for really cool additions. The speed of the algorithm can certainly be improved.

**Q6: What are the requirements for the project to run?**  
**A:** 
- streamlit==1.12.0
- pandas==1.5.3
- numpy==1.23.5
- scipy==1.10.0
- matplotlib==3.7.1
- seaborn==0.12.2
- qpython


