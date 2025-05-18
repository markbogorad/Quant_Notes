up:: [[Supervised Learning MOC]], [[Time Series MOC]]
tags:: #Machine_Learning 
# Lag Features
- Just lagged values
## Python:

```
from pandas import read_csv
from pandas import DataFrame
from pandas import concat
series = read_csv('daily-min-temperatures.csv', header=0, index_col=0)
temps = DataFrame(series.values)
dataframe = concat([temps.shift(1), temps], axis=1)
dataframe.columns = ['t-1', 't+1']
print(dataframe.head(5))
```

