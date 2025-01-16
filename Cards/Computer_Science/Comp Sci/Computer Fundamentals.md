up:: [[Computer Science MOC]]
tags:: #Programming  
# Fundamentals
## Binary Language
- 0s and 1s --> represent all of computer code (its internal language)
- Think of these 2 options as **an on and off switch for lightbulbs**
	- 0 would be off, 1 would be on
	- To display numbers or letters, some parts stay on some are shut off --> combination = actual number
- Bit --> singe binary digit
- Byte --> 8 bits, 256 possible values in the code
- Binary is only necessary for hardware specialists
## ASCII
- For representing language
- Assign letters bit combos
- To read from computer, it goes binary --> decimal --> character (ex: 0100100 --> 72 --> H)
	- Binary to decimal conversion, **how it works**:
		    - 0×2^7=0
		    - 1×2^6=64
		    - 0×2^5=0
		    - 0×2^4=0
		    - 1×2^3=8
		    - 0×2^2=0
		    - 0×2^1=0
		    - 0×2^0=0
		    - Sum: 64+8=72
	- Decimal to character --> use an ASCII chart
## Unicode
- A superset of ASCII --> 8 bits was too small to encompass additional languages, emojis, etc
- 16-32 bits per character (1-4 bytes)
	- 2^32 = 4 billion possible characters
- Unicode is mean't to digitally preserve human language
- How it looks
	- U+1F602
		- A mathematical system called base 16 / hexadecimal
		- Uses 0-9 and A-F
## How Computers Find Things (Halving)
- Divide information by *half* to narrow down quickly (log base 2 operation of continuous halving)
	- Follow the destination each time
- The speed of this is all about **code design**
## Main building blocks
- Functions
- Conditionals (ex: else statement)
- Variables (ex: boolean)
