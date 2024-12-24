up:: [[C++ MOC]]
tags:: #Programming
# Creation Steps:

1. Initialize [[Inclusion Guards]] for multiple inclusion
2. "#include" all relevant libraries
3. Use [[Namespaces]] where relevant
4. Define the [[Class]]
5. Implement the [[Class]]
6. Close [[Namespaces]]
7. Close [[Inclusion Guards]]
8. Create a Test Program
### Every object should be divided into a:

## HPP File
- This is used to declare functions, variables, classes, etc..

## CPP File
- This is used to implement those functions, variables, classes, etc.. declared in the HPP

## 2 File Approach: 
###### - Sometimes an HPP implements directly, cutting out the need for a CPP file. It is better practice to **SEPARATE** the two files for the following reasons:

- Modularity
	- Design principle:
		- Breaking down the code to separate components (HPP and CPP)
			- Code becomes more readable
			- Allows for easier changes to implementation (CPP) -> changes to the implementation don't require re-compilation
- Reduced compile time
- [[Encapsulation]]
- Data_Hiding
	- Protects classes integrity by preventing external code from accessing the internal state
	- Enhances modularity : the private implementation of a class can change without affecting other parts of the program
	- Increases ease of maintenance and readability 
- Linkage
	- The separation of HPP and CPP allow for **multiple CPP files to be linked onto 1 HPP**
- Avoiding multiple inclusion
	- If a HPP file (with implementations) is included in multiple CPP files, this increases the chances of multiple inclusion due to potential additional implementations
- Library Reusability
	- Useful to have an HPP library without **giving away variable access** (in implementation) to many members or **re-defining implementations**
- 