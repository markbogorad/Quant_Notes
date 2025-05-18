up:: [[Supervised Learning MOC]], [[Time Series MOC]]
tags:: #Machine_Learning 
# Rolling Window Statistics
- Features over a given time period
- Ex:
	- 5 day rolling mean
	- min/max per period
	- momentum features
	- mean reversion
	- rolling volatility
## Python:
```
from pandas import read_csv
from pandas import DataFrame
from pandas import concat
series = read_csv('daily-min-temperatures.csv', header=0, index_col=0)
temps = DataFrame(series.values)
shifted = temps.shift(1)
window = shifted.rolling(window=2)
means = window.mean()
dataframe = concat([means, temps], axis=1)
dataframe.columns = ['mean(t-2,t-1)', 't+1']
print(dataframe.head(5))
```