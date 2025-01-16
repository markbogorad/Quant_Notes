up:: [[BOOST]]
tags:: #Programming 
# Tuples
- A fixed-size collection of heterogeneous elements, meaning that it can store objects of different types together in a single unit
## Purpose
- To store different kinds of data (string, double, int) as one entity
	- vs [[Arrays]] that store elements of only 1 type (array of doubles)
- Can combine data without the need of a class
- Tuples can be used to return multiple values from a function. This is particularly useful in languages like [[Python MOC]], where a function might return multiple values packed into a single tuple.
- Used purely in [[Test Program]]
### Some Uses:
- For returning multiple varying values form a function
	- This can be helpful for some sort of tabulation (like with age, height, name in exercise)
		- Basically an excel
	- Optimization: need to return maximum and minimum
		- Instead of using global variables or modifying inputs, a tuple allows the function to return both values in a single call neatly.
## Example (C++ Course Level 8 exercise 2):
```
// Typedef for a Person tuple that contains name (string), age (integer), and height (double)

typedef boost::tuple<std::string, int, double> Person;

// Function to print the person tuple

void printPerson(const Person& person) {
std::cout << "Name: " << person.get<0>()
					<< ", Age: " << person.get<1>()
					<< ", Height: " << person.get<2>() << " cm" << std::endl;
}

int main() {
// Creating a few person tuple instances
Person person1 = boost::make_tuple("Kobe", 24, 198.5);
Person person2 = boost::make_tuple("LeBron", 6, 206.3);
Person person3 = boost::make_tuple("Shaq", 32, 216.5);

// Print the person tuples
printPerson(person1);
printPerson(person2);
printPerson(person3);

// Increment the age of one of the persons (person2)
person1.get<1>() += 1;
person2.get<1>() += 1;
person3.get<1>() += 1;

// Print the person tuple again to see the updated age
std::cout << "\nAfter incrementing age:" << std::endl;
printPerson(person1);
printPerson(person2);
printPerson(person3);

return 0;

}
```

