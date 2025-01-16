up:: [[Time Series MOC]], [[Supervised Learning MOC]]
tags:: #Machine_Learning 
# Date-Time Features
- Sort of like [[Dummy Variables]] for time
- Categorical encoding
	- Ex:
		- Months 0-12
		- Hours 0-23
		- Seasons 1-2-3-4
## Python:

```from pandas import read_csv
from pandas import DataFrame
series = read_csv('daily-minimum-temperatures.csv', header=0, index_col=0, parse_dates=True, squeeze=True)
dataframe = DataFrame()
dataframe['month'] = [series.index[i].month for i in range(len(series))]
dataframe['day'] = [series.index[i].day for i in range(len(series))]
dataframe['temperature'] = [series[i] for i in range(len(series))]
print(dataframe.head(5))`
	- Lag Features
	- Window Features