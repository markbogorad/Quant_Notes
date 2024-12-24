up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# One Hot Encoding
- An ML technique used for essentially making data into binary form for computers to be able to work with it
- Example: real estate data showing neighborhoods -> If house is in Canary Wharf, then it is marked with a 1 in the Canary Wharf column and a 0 in all other locations
	- Allows you to observe correlations with Canary Wharf
## Example in Prof Snow code
```
# Encode the selected columns
dummies = pd.get_dummies(train_df[categorical_features], drop_first=True)

# Concatenate the encoded columns with the original dataset
train_df = pd.concat([train_df, dummies], axis=1)

# Drop the original columns that have been encoded
train_df.drop(categorical_features, axis=1, inplace=True)

# Output the modified dataset
train_df.head()
```
