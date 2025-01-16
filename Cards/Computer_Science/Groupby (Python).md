up:: [[Python MOC]]
tags:: #Programming 
# Groupby
- Think of this as sorting data in excel
- The `groupby` operation in pandas is a powerful tool for grouping data based on the values of one or more columns and then performing some aggregate or transformation function on the grouped data. 
- It is often used to summarize or analyze data by categories, allowing you to apply operations like sum, mean, count, or custom functions to each group independently.
## Syntax:
- `df.groupby('column_name').operation()`

## Example
```
import pandas as pd

data = {
    'Category': ['A', 'B', 'A', 'B', 'A', 'B'],
    'Values': [10, 20, 30, 40, 50, 60]
}
df = pd.DataFrame(data)

# Group by 'Category' and sum the 'Values'
grouped = df.groupby('Category').sum()
print(grouped)

# OUTPUT

         Values
Category        
A             90
B            120

```


## From class
- Used when working with tine series operations to avoid merging data from 2 different series when unwanted (class example was merging tickers)
	- As an alternative --> *add history command* --> create fake data between tickers and do rolling --> **add_history_1** command
		- Essentially ignores the empty fake data
		- Allows calculations to be done faster