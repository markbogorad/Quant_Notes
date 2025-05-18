up:: [[Data MOC]]
tags:: #Programming 
# Financial Data
- Financial data has a high variety and volume
- Can be split into
	- Entities (stocks, bonds, ETFs,...)
	- Characteristics of entities (price, volume, etc)
	- Relationships (links between entities like issuer to security)
- **3 general types of market data are**
	- [[Reference Data]]
	- [[Business Data]]
	- [[Static Data]]

|Type|Role|Examples|Persistence|
|---|---|---|---|
|**Reference**|Who/what|`CUSIP`, `Ticker`, `Exchange`|Stable|
|**Business**|What’s happening|`OHLCV`, ratings, earnings|Dynamic|
|**Static**|How to interpret|`Exchange codes`, `Currency lists`|Semi-static|

![[Pasted image 20250505213939.png]]
![[Pasted image 20250505215411.png]]