up:: [[C++ MOC]]
tags:: #Programming
# ToString
- Converts objects into strings
## In practice:
![[Screenshot 2024-04-20 at 1.48.58 PM.png]]
- std::stringstream ss;
	- This creates an output string stream via the standard command "stringstream". Concatenates various data types into a string
	- Stream --> name of the created ostringstream object
- stream << " Point(" << x << ", " << y << ")";
	- This is the actual output stream that will show up
	- Stream --> will give out a string (used like cout in this case)
	- " Point(" << x << ", " << y << ")" --> this is how the text will look
		- Point(3,2)
- return stream.str();
	- This part **converts** the contents of the stream object **into a string** and returns it
	- **.str()** is a member function of stringstream used to get the string that was built in the stream
##### Definitions:
- Stream
	- An object used for sequential input/output (IO) operations
	- Think of data stream
# Implementation with [[Inheritance]]
![[Screenshot 2024-04-20 at 1.59.51 PM.png]]
