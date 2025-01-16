up:: [[Operators]]
tags:: #Programming 
# C++ Standard Operators (List)
## Arithmetic Operators
1.  `+` - Addition
2. `-` - Subtraction
3. `*` - Multiplication
4. `/` - Division
	- Chopped results due to *truncation*: 5/2 = 2,    1/2 = 0
5. `%` - Modulo (Remainder)
	- Remainder after division --> 9 % 2 = $8\frac{1}{2}$
		- Modulo is 1 (from 1/2)
6. `++` - Increment
	- Postfix: val++
		- Return value, then increment
		- Ex: `int a = 5, int b = a++`
			- b is assigned 5, then a gets incremented to 6 behind the scenes
		- **NYU -> increment happens AFTER delimiter (;)**
	- Prefix: ++val (better for [[For Loop]]s)
		- Increment first, then return value
		- Ex: `int a = 5, int b = ++a`
			- a gets incremented to 6, then b is assigned to a
		- **NYU -> increment happens BEFORE delimiter (;)**
1. `--` - Decrement

## Assignment Operators
1. `+=` - Addition assignment
2. `-=` - Subtraction assignment
3. `*=` - Multiplication assignment
4. `'='` - Assigns the value of the right operand to the left operand.
5.  `/=` - Divides the left operand by the right operand and assigns the result to the left operand.
6. `%=` - Takes the modulus using two operands and assigns the result to the left operand.
7. `<<=` - Left shifts the left operand by the right operand and assigns the result to the left operand.
8.  `>>=` - Right shifts the left operand by the right operand and assigns the result to the left operand.
9. `&=` - Bitwise AND operation on the left and right operands and assigns the result to the left operand.
10. `|=` - Bitwise OR operation on the left and right operands and assigns the result to the left operand.
11. `^=` - Bitwise XOR operation on the left and right operands and assigns the result to the left operand.

## Relational Operators
- **Used for Booleans in loops**
1. `'=='` - Equal to (put in quotations for Obsidian)
2. `!=` - Not equal to
3. `>` - Greater than
4. `<` - Less than
5. `>=` - Greater than or equal to
6. `<=` - Less than or equal to
7. `<=>` - Three-way comparison operator (since C++20)

## Logical Operators
- **For concatenating (linking) boolean expressions**
1. `&&` - Logical AND
2. `||` - Logical OR
3. `!` - Logical NOT
4. `and` - Alternative spelling for `&&`
5. `or` - Alternative spelling for `||`
6. `not` - Alternative spelling for `!`
7. `^` - Bitwise XOR, often used in logical contexts
8. `&` - Bitwise AND, used in logical contexts with bitwise operations
9. `|` - Bitwise OR, also used logically with bitwise operations
10. `~` - Bitwise NOT, used for bitwise negation, applicable in logical bit manipulation

## Conditional Operator
- The one and only ternary operator (3 pieces), it can't be overloaded
```
(expr) ? expt : expf;
```
- If `expr` evaluates to true, `expt` is preformed
- Otherwise `expf` is preformed
### Example in practice:
![[Screenshot 2024-04-15 at 7.48.13 AM.png]]

## Bitwise Operators
1. `Sizeof` - Gives the size of an expression in bytes
```
void main()
{
float f; 
printf("%d\n" sizeof(int)); /* size of int in bytes */
```
2. `&` Bit-and
3. `|` Bit-or
4. `^` Exclusive bit-or
5. `<<` Shift left
6. `>>` Shift right
7. `~` One complement (unary)