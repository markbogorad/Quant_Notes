up:: [[Python MOC]]
tags:: #Programming 
# Query
- A way to filter rows base don a query expression
	- A query is a request for information
- Like [[SQL]] syntax

## Example
```
import pandas as pd

# Sample DataFrame
df = pd.DataFrame({
    'Name': ['Alice', 'Bob', 'Charlie', 'David'],
    'Age': [25, 30, 35, 40],
    'Score': [85, 90, 88, 92]
})

# Query to select rows where Age is greater than 30
result = df.query('Age > 30')
print(result)

```
