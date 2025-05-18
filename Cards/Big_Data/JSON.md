up:: [[Data MOC]]
tags:: #Programming 
# JSON (Javascript Object Notation)
- Data interchange format
	- Used for communication between server and client
	- **A data transfer mechanism**
- Language independent!
- Comparable to XML but better because its human readable

Great question — understanding this distinction is essential for parsing and working with JSON data in market feeds or APIs.
## JSON Object vs JSON Array

| Concept         | **JSON Object**                           | **JSON Array**                                               |
| --------------- | ----------------------------------------- | ------------------------------------------------------------ |
| **Structure**   | Unordered set of key-value pairs          | Ordered list of values (indexed by position)                 |
| **Enclosed by** | Curly braces `{}` (similar to dict)       | Square brackets `[]`                                         |
| **Accessed by** | **Keys** (like dictionary/map)            | **Index** (like a list/array)                                |
| **Used for**    | Representing **entities** (e.g., a stock) | Representing **collections** (e.g., a time series of stocks) |

![[Pasted image 20250505222708.png]]

### Real Example from Market Data API

```json
{
  "date": "2022-02-04",
  "intraday_data": [
    {
      "timestamp": "09:30",
      "open": 137.71,
      "close": 138.20
    },
    {
      "timestamp": "09:31",
      "open": 138.22,
      "close": 138.75
    }
  ]
}
```
