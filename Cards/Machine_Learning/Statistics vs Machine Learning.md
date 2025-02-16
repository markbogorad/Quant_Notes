up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# What is Machine Learning
- Algorithms that enable computers to learn from mistakes by extracting patterns from data and improve forecasting performance through experience
- In ML, inputs (data) derive the model, whereas in finance methods such as [[DCF Real Estate]] use model to derive inputs (price)
## ML V Stats
- Both deal with data analysis
- Statistics
	- Goal is to understand data (relationships and forecasting)
	- Focuses on hypothesis testing and decision making
	- Example: Determining if there is a significant difference in average income between two groups.
	- Uses parametric methods (i.e. it assumes data follows a distribution)
	- Stats is about in sample perfomance and understanding the problem
- Machine Learning
	- Goal is prediction and pattern recognition
	- Focuses on building algorithms that can learn from data, generalize from past experiences, and perform tasks such as classification, regression, clustering, etc.
    - Example: Predicting the price of a house based on various features like size, location, and number of rooms
	- Does not have a parametric method
	- ML is about predictive power and out of sample performing
## Table
|Property|**Statistical Inference**|**Supervised Machine Learning**|
|---|---|---|
|Goal|Causal models with explanatory power|Predictive model often with limited explanatory power|
|Data|The data is generated by the model|The data generation process is unknown|
|Expressibility|Typically linear|Linear or Non-linear|
|Model Selection|Information Criteria|Numerical validation|
|Scalability|Limited to lower-dimensional data|Scaled to high-dimensional input data|
|Robustness|Prone to over-fitting|Designed for out-of-sample performance|
|Interpretability|High, as models are built to understand relationships|Can be low leading to “black box” models|
|Domain Knowledge|Often requires substantial domain knowledge|Can automate feature learning and selection|
|Use Case|Eg., Risk Factor Analysis, Time-Series Analysis, Econometric Modeling, Volatility Modeling, Cointegration Analysis, Mean Reversion Strategies.|Eg., Predictive Trading, Sentiment Analysis, Portfolio Optimization, Micro-Pattern Recognition, Continuous Model Refinement|