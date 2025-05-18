up:: [[Data MOC]]
tags:: #Programming 
# JSON Parser
- A [[JSON]] parser translates JSON format into the language equivalent version (dict for python, Json::value for C++)
- What makes JSON language agnostic
- Can then access like this:
	- Python: `data["price"]`
	- C++: `data["price"].asFloat()`
- Without parsing, JSON is just a string
- In C++, JSON CPP uses an [[Iterators]] to go through the objects in a JSON file