
# Vector STL in C++

**Vector** in C++ are kind of a dynamic sized array, which can grow and shrink as per the data inserted or deleted in runtime.

*Vectors => dynamic array*

To include vector in C++, but defined inside std namespace.
`#include <vector>`

Declaring a vector :
`std::vector<int> v1;`

To access an element in a vector :
`vec2[index];` or `vec2.at(index)` with bound checking

Vector is a class template in C++, so within the angled brackets insert the data type.

Frequently used methods :
- `push_back()` : Adds an element to the end of the vector.
- `pop_back()` : Removes the last element of the vector.
- `insert(pos, data)` : inserts elements at a specified position.
- `begin()` : returns the starting point iterator.
- `erase(pos)` : removes elements from a specified position or range.
- `clear()` : clears the vector space.
- `v1.swap(v2)` : swaps the contents of two vectors.
- `front()` : returns a reference to the first element.
- `back()` : returns a reference to the last element.
- `size()`, `capacity()`, `isEmpty()`.

To traverse elements of a vector using for loop.
```cpp
for (auto i : v1){
	std::cout << i << std::endl;
}
```
