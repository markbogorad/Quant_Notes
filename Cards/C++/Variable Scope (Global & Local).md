up:: [[C++ MOC]]
tags:: #Programming 
# Global Variables
- Declared outside of all functions
- Typically at the top of a program file
	- Like outside of `main` for example
- Accessible for any function within the file
	- Accessible to other functions and files with the `extern` keyword
- Static lifetime: allocated when program starts and deallocated when it ends

# Local Variables
- Declared within functions
	- Only associated and works within that function
- Automatic lifetime: only exist during execution of specific coding block where it is created
- Local variables are safer and more secure than global variables because they prevent access from unintended parts of the program, reducing the risk of unintended side effects.
	- Increased modularity

## Extern Keyword
- Makes it possible to use a global variable from another file
	- `extern int linenumber`

## Static Keyword
- When you want to **bind** a global variable **only** to the local file
	- `static int linenumber`