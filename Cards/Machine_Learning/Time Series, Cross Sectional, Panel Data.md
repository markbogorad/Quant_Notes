up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Time Series, Cross Sectional, and Panel Data
## Cross Sectional
**Cross-sectional** data investigates a moment in time and is generally easy to model.
- Order does not matter --> can be shuffled in [[Supervised Learning]]

|Instance|Income JAN|Savings JAN|Credit JAN|
|---|---|---|---|
|Sally|$100K|$110K|810|
|Yan|$120K|$20K|720|
|Freddy|$200K|$70K|935|
|Susan|$50K|$100K|680|

## Time Series
**Time series** data looks over many moments of time for one entity (say Sally). Essentially this adds an index factor to cross sectional data
- Order here matters --> can't be shuffled

|Date|Income|Savings|Credit|
|---|---|---|---|
|NOV|$100K|$45K|690|
|DEC|$110K|$30K|695|
|JAN|$120K|$20K|720|
|FEB|?|?|?|

## Panel Data
**Panel** data is time-series data collected for multiple entities _(not just for Sally),_ essentially **3D** data. Sometimes referred to as **time-series** **cross-sectional** **data**.
- This is a multi indexed [[Pandas]] data frame ([[Python MOC]])
- This is also like a 3-D matrix

Slice 1 (Sally)

|   |   |   |   |   |
|---|---|---|---|---|
|Date|ID|Income|Savings|Credit|
|NOV|Sally|$100K|$45K|690|
|DEC|Sally|$110K|$30K|695|
|JAN|Sally|$120K|$20K|720|
|FEB|Sally|?|?|?|

Slice 2 (Yan)

|   |   |   |   |   |
|---|---|---|---|---|
|Date|ID|Income|Savings|Credit|
|NOV|Yan|$100K|$45K|690|
|DEC|Yan|$110K|$30K|695|
|JAN|Yan|$120K|$20K|720|
|FEB|Yan|?|?|?|