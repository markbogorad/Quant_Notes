up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Chow Test
- Identifies the presence of a [[Structural Breaks]]
- Tests whether betas are constant after a specified event (***needs specific date***)
- Null: no break
- Follows [[F Distribution]]

**How it works**
- Estimates a model that assumes there is no break (restricted model) and compares this to a model thats composed of a regression pre and post break (2 regressions)

## Test statistic
$$ F = \frac{N - 2k}{k} \frac{RSS - (RSS_1 + RSS_2)}{RSS_1 + RSS_2}$$
**Rejection region:** choose significance level and find critical value from the $F(k, N - 2k)$ distribution. Reject null if test statistic exceeds critical value.
- M = K

