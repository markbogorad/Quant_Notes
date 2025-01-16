up:: [[C++ MOC]]
tags:: #Programming  
# Macros
- A preprocessor directive
- Essentially setting a certain magic number (like pi, or 52 for a deck of cards, anything that gets hard coded and you dont want that)
- Looks like: `#define PI 3.14`, include at top
	- This goes through the code and replaces every instance of `PI` with `3.14`
## Why its useful
- Example: cards
- You coded a card game using 52 cards as a deck
- You want to add another card game, but it only has 36 cards
	- Now, you just use a macro `#define 52 32` and problem solved
		- Instead of manually removing each 52 (and probably missing some)