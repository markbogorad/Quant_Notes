up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# Preprocessing
- This is the initial step where data is explored, cleaned, transformed, and prepared for modeling.
- **Exploratory Analysis**: Involves understanding the data through descriptive statistics and visual analytics.
- **Wrangling**: Deals with structuring unstructured data, detecting errors and outliers, and handling missing data.
- **Augmentation**: Focuses on transforming data, creating interaction terms, mapping, extracting features, synthesizing new data, and handling categorical variables with multiple levels.
- **Feature Selection**: Involves choosing the most relevant features through methods like embedding, filtering, and wrapping.
	- [[Feature Selection Techniques]]
## Label Development
- Working on the Y variable is very important
	- Engineering the target --> transformations
		- Return/volatility = risk adjusted return
## Wrangling
- Structuring unstructured data
	- Unstructured --> data this is not yet numbers 
	- [[One Hot Encoding]], binary encoding, 1 more
- Fixing errors
- Correcting for outliers
	- Outlier detection
		- Windzorization  --> replacing outlier with 99th percentile
- Cardinality
- Missing Data
	- Test what works and pick 3 or so methods - in class
	- MNAR --> missing not random
		- When the omitted information might be biased and labeling this as average is inaccurate
		- ML model assigns average but punishes omitted data to give it negative bias
		- If over 80% of column or row is missing --> drop it