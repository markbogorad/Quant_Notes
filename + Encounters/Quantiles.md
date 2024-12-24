up:: [[Probability MOC]]
tags:: #Math
# Quantiles
- **Quantiles** are values that divide a probability distribution or a set of data into equal-sized intervals. In other words, quantiles are cut points in a distribution such that a certain proportion of the data falls below each cut point.
### Key Concepts:
1. **p-th Quantile**:
   - The p-th quantile is the value below which a proportion $( p )$ of the data falls. For example, the 0.25 quantile (or 25th percentile) is the value below which 25% of the data lies.

2. **Common Quantiles**:
   - **Percentiles**: Divides the data into 100 equal parts. For example, the 25th percentile (also known as the first quartile) is the value below which 25% of the data falls.
   - **Quartiles**: Divides the data into 4 equal parts:
     - **Q1** (First Quartile, 25th percentile): 25% of the data falls below this value.
     - **Q2** (Second Quartile, 50th percentile or Median): 50% of the data falls below this value.
     - **Q3** (Third Quartile, 75th percentile): 75% of the data falls below this value.
   - **Deciles**: Divides the data into 10 equal parts.
   - **Median**: The 50th percentile (or 0.5 quantile) is a special quantile that divides the data into two equal halves.

3. **Calculating Quantiles**:
   - For a given distribution, the quantile function $( Q(p) )$ gives the p-th quantile. If $( F(x) )$ is the cumulative distribution function (CDF), the p-th quantile is the value $( x )$ such that:
     $$F(x) = p$$
   - In practice, quantiles are often found using statistical software or tables, especially for common distributions like the normal distribution.

### Example:
For a standard normal distribution:
- The 0.25 quantile is approximately -0.674 (i.e., 25% of the values fall below -0.674).
- The 0.5 quantile (median) is 0.
- The 0.75 quantile is approximately 0.674 (i.e., 75% of the values fall below 0.674).

### Importance of Quantiles:
- **Data Analysis**: Quantiles are used in descriptive statistics to summarize data. They help describe the spread and central tendency of the data.
- **Boxplots**: In visualizations like boxplots, quartiles are used to show the distribution of data, highlighting the median, the interquartile range (IQR), and potential outliers.
- **Risk Management**: In finance, quantiles are used to calculate [[Value at Risk (VaR)]], which estimates the potential loss in a portfolio at a given confidence level.