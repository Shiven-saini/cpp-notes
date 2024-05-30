# Classes in C++

**Syntax :**

```cpp
class ClassName {
private:
	int id{};
	std::string name{};

	static int count{};
	// general convention name variable prefixed with m like m_id
	// make member variables private and
public:
	// Constructors can be overloaded 
	// Constructors have same name as class.
	// Doesn't have any return type.
	ClassName() {
		// Default constructor
	}
	ClassName(int _id, std::string _name) : id{ _id }, name{ _name } {
		// _variables are generally used to store hidden data.
		// Member intializer list to intialize the variables in constructor.
	}
	// Copy constructor to duplicate data object.
	ClassName(const ClassName& obj){
		id = obj.id;
		name = obj.name;
	}
	// Destructor will be called when the object goes out of scope.
	~ClassName(){
		// data cleaning tasks.
	}
	friend void display(const char* text);
}
```

**static member variable:** not linked to any object but to the class itself. 

**static member function:** not linked to any function but to the class itself.

**friend function :** can be used to give the function access rights to the private members.


---
## Inheritance in C++

- Virtual functions `virtual` & `override`
- Inheritance 
- Abstract class : class only defined implementation and meant to be derived only.

```cpp
class Base {
private:
	int m_num;
	float m_roll;
public:
	void foo() {
		// logic
	}
	// virtual function.
	virtual void boo() {
		// logic 
	}	
}

class Derived : public Base {
public:
	void boo() override {
		// logic
	}
}

class AbstractExample {
public:
	virtual void foo() = 0;
	virtual void boo() = 0;
}
```



