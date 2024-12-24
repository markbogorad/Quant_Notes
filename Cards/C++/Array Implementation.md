up:: [[Arrays]]
tags:: #Programming
# Implementation is different:
- Use **loops and dynamic memory** for copy constructor, assignment operator, setters/getters, and bracket operator
	- Pretty much the same as regular implementation except you need to iterate via a loop and you have `new` and `delete` here and there...
## Copy Constructor
```
// Copy constructor

template <typename T> 

Array<T>::Array(const Array<T>& source) : m_size(source.m_size), m_data (new T[source.m_size]) { 

// Dynamically allocates memory for an array of type T with size same as source

for (int i = 0; i < m_size; ++i) {

m_data[i] = source.m_data[i]; 

// Copies each element from source to the newly created array

}

}
```
- Use a loop to copy each element at each index of the array
	- As long as `i` is less than `m_size`, copy it over using `m_data[i] = source.n_data[i];`
## Assignment Operator
```
// Assignment operator

template <typename T>

Array<T>& Array<T>::operator=(const Array<T>& source) {

if (this == &source) { // Self-assignment check

return *this;

}

delete[] m_data; // Deallocates current memory to avoid memory leaks.

m_size = source.m_size; // Copies the size from source.

m_data = new T[m_size]; // Allocates new memory for the array.

for (int i = 0; i < m_size; ++i) {

m_data[i] = source.m_data[i]; // Copies each element from source to the newly created array.

}

return *this; // Returns a reference to the current object.

}
```
## Setters/Getters
```
// Setter

template <typename T>

void Array<T>::SetElement(int index, const T& val) {

if (index >= 0 && index < m_size) {

m_data[index] = val; // Sets the value of the element at the given index.

} else {

std::cerr << "Index out of bounds!" << std::endl;

}

}

  

// Getter

template <typename T>

T& Array<T>::GetElement(int index) const {

if (index >= 0 && index < m_size) {

return m_data[index]; // Returns a reference to the element at the given index.

} else {

std::cerr << "Index out of bounds!" << std::endl; // Prints an error message if index is out of bounds.

// Return a reference to a default value in case of out-of-bounds access

return m_data[0]; // Returns a reference to the first element if index is out of bounds.

}

}
```
## Bracket Operator
```
// Bracket operator

template<typename T>

T& Array<T>::operator[](int index) const {

if (index < 0 || index >= m_size) {

throw OutOfBoundsException(); // Throws out of bounds exception

}

return m_data[index];

}
```



