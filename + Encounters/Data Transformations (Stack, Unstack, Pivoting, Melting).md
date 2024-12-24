up:: [[Python MOC]]
tags:: #Programming 
# Different Types:

| **Operation** | **Function**  | **Purpose**                                                 | **Input Format**           | **Output Format**          | **Use Case**                                                                                         |
|---------------|---------------|-------------------------------------------------------------|----------------------------|----------------------------|-------------------------------------------------------------------------------------------------------|
| **Pivoting**  | `.pivot()` / `.pivot_table()` | Reshape data from long to wide format by spreading unique values into columns | Long (tidy) format          | Wide format                 | When you have repeated identifiers and want to spread them across columns based on unique values.       |
| **Melting**   | `.melt()`     | Reshape data from wide to long format by gathering columns into key-value pairs | Wide format                 | Long (tidy) format          | When you want to gather multiple columns into a single column for easier analysis or visualization.     |
| **Stacking**  | `.stack()`    | Convert columns into a row-level structure with a multi-level index | Wide format                 | Long format (with MultiIndex) | When you want to collapse columns into a longer format, turning them into part of the index.            |
| **Unstacking**| `.unstack()`  | Convert a multi-level index back into columns, reversing the stacking operation | Long format (with MultiIndex)| Wide format                 | When you want to pivot one level of a MultiIndex back into columns, returning to a wide format.         |

### Example Scenarios:
- **Pivoting**: Suppose you have sales data where each row represents a different date and product category, and you want each product category to have its own column with sales figures for each date.
	- Output: 
		- `Variable      A  B`
		- `Date              
		- `2021-01-01  1  2`
		- `2021-01-02  3  4`

- **Melting**: Suppose you have a DataFrame with different measurement types (e.g., temperature, humidity) as columns, and you want to convert it to a long format where each row represents a single measurement type for a given time.
	-  Output: 
		- `ID variable  value`
		- `0   1        A      3`
		- `1   2        A      4`
		- `2   1        B      5`
		- `3   2        B      6`


- **Stacking**: Suppose you have a DataFrame with different financial metrics (e.g., revenue, profit) as columns for multiple companies, and you want to stack those metrics into a single column while preserving the company names in the index.
	- Output
		- ![[Pasted image 20240820112233.png]]

- **Unstacking**: Suppose you have a Series with a MultiIndex (e.g., date and product category) and want to unstack the product category to spread it across columns, returning to a wide format where each column represents a product category.
	-  Output: 
		- ![[Pasted image 20240820112224.png]]
## Wide Data
```
import pandas as pd

data = {
    'value': [10, 20, 30, 40, 50, 60]
}

index = pd.MultiIndex.from_tuples([
    ('A', 'X'),
    ('A', 'Y'),
    ('A', 'Z'),
    ('B', 'X'),
    ('B', 'Y'),
    ('B', 'Z')
], names=['letter', 'sub_letter'])

df = pd.DataFrame(data, index=index)
print(df)

# AND LOOKS LIKE THIS

               value
letter sub_letter      
A      X            10
       Y            20
       Z            30
B      X            40
       Y            50
       Z            60

```

## Unstack Into Long Data
```
df_unstacked = df.unstack(level='sub_letter')
print(df_unstacked)
```

```
        value       
sub_letter    X   Y   Z
letter                  
A            10  20  30
B            40  50  60
```
- Essentially becomes in time series format

### Key Points:
1. **Unstacking the Last Level by Default**: By default, `.unstack()` will unstack the last level of the index (in this case, `sub_letter`).
2. **Unstacking a Specific Level**: You can specify which level to unstack by passing the level's name or its position as an argument.
3. **Creating a Wide Format**: After unstacking, the DataFrame typically has more columns and fewer rows, effectively converting it from a long format to a wide format.
4. **Missing Data Handling**: If unstacking results in missing data, pandas will automatically fill these with `NaN`.


## Long Data to Wide Data
