up:: [[C++ MOC]]
tags:: #Programming 
# Command Line Arguments
- A way to pass (by value) information to the program once it has started running
	- Want to change code behavior at runtime
- Used for file operations and configurations
## Main functions:
- `argc` - argument count
	- This is the number of command line arguments that will be passed to the program (including program itself)
- `argv[]` - An [[Arrays]] of strings representing the actual command line arguments, with `argv[0]` being the name of the program
## How to Use
- Code the implementation of individual `argv[]` members within your function
- Call them in terminal