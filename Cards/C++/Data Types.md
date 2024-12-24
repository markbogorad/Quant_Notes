up:: [[C++ MOC]]
tags:: #Programming 
# Data Types
- C++ offers a rich set of built-in as well as user-defined data types. The built-in data types can be categorized into several groups:
## Fundamental Types
1. **Character types**:
    - `char`: Typically one byte. This is an integer type (ASCII type)

2. **Integer types** (signed and unsigned):
	- `Short`: 16 bits - for smaller numbers (max 65,000)
	- `Long`: 32-64 bits - for massive numbers
	- `Signed`: Stores positive and negative values
	- `Unsigned`: Only stores positive values and 0
		- For variables that will never have negative values

4. **Floating-point types**:
    - `float`: 7 decimals of precision
    - `double`: 15 decimals of precision
    - `long double`: 19 decimals of precision

5. **Boolean type**:
    - `bool`: True/false variable

6. **Void type**:
    - `void` (indicates absence of type i.e. no type)
	    - Function does not return a value

7. **std::nullptr_t**:
    - Represents the null pointer literal, `nullptr`. [[Pointers]]
    - Pointer that doesn't point to anything
	    - Used in function overloading and when you intend to use the pointer later
8. **Literals**
	- Represent fixed values within code, these are hard written on the back end
	- EX:
		- `int hexadecimal = 0x2A;`
		- `double exponential = 2.5e3; // equivalent to 2.5 * 10^3 or 2500`
		- `char newline = '\n';`
		- `bool isReady = true; bool isFalse = false;`
## Compound Types & User-Defined Types
1. **[[Arrays]]**: A collection of elements of the same type.
2. **[[Functions]]**: Behaviors defined to take zero or more arguments and optionally return a value.
3. **[[Pointers]]**: Variables that store the memory address of another variable.
4. **References**: An alias for another variable. [[Call by Reference]]
6. **[[Class]]es**: User-defined types that can contain data members and member functions.
7. **Unions**: Similar to classes, but all members share the same memory location. See [[Variant]], even better.
8. **Enumerations**: Define a type by enumerating its possible values with `enum`.
	- Basically a class of integral constants. Useful for representing a group of related constants
	- Basically using **descriptive names for numbers** via a a class like structure
1. **Typedefs** and **alias declarations**: Define a type alias for another data type.
	- Declarations: `typedef` and `using`
		- `Using` `new_name = old_name`
	- Referring to an existing type with a new name
		- Useful for categorizing (naming) complex structures
## Type Modifiers
These aren't types themselves but can modify the meaning of a type:

- `const`: Specifies that a variable's value cannot be modified.
- `volatile`: Indicates that a variable can be modified in ways not explicitly specified by the program.
- `signed` and `unsigned`: Specify whether integers are signed or unsigned.
- `short` and `long`: Adjust the size of integer types.
## Auto Type
- `auto`: Enables automatic type inference, where the compiler deduces the type of the variable from its initializer expression.