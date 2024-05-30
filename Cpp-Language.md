# History of C & C++

C language was developed by **Dennis Ritchie** in the year **1972** as a systems programming language.

C language was used extensively in the development of unix Operating system being developed at **Bell Labs.**

## Advancement in C++

- Developed by **Bjarne Stroutstrup** in **1979**
- Supported **Object oriented Programming(OOP)**
- Standardized later on in the year **1998** by **ISO Committee**
- Major updates cycle of 3 years (*C++ 11*, *C++ 14*, *C++ 17*, *C++ 20*)

> C++ philosophy can be summarized as '*Trust the programmer*', allowing the programmer a higher degree of freedom but with increased danger of issues as well.

## C++ use cases and applications

- **Video game development:** thanks to it's extensive control over hardware leading to powerful resource management.
- **Real-time systems:** thanks to it's low overhead of execution since the output file is directly executed from the lowest machine code file.
- **HFTs:** used in high frequency trading applications.
- **Embedded software:** Close to hardware performance.

----
## Compilation process in C++

Compilation or Building is an umbrella term that defines the cycle of generation of output from the stage of code written by the programmer.

![[Pasted image 20240529122927.png]]

1. Pre-processing
2. Compilation
3. Linking

*In larger projects, build tools like Cmake, Make & build2 tools are used to automate the task of building the project.*

### Common terms related to building process

- **Build:** Compiles all the *modified* code and then link the object files into an executable.
- **Clean:** Removes all cached object files and executables.
- **Rebuild:** *Clean* -> *Build*
- **Compile:** Recompiles a single code file.

----

# Comments in C++

Comment is a programmer readable note, ignored by compiler.

**Syntax:**
```cpp
// Single line comment

/* multi line 
* comment
* asterisk can be added for better legibility
*/
```

**Important:** Good characteristics of a comment statement:
1. Use of class, library or function
2. How the code is going to accomplish the task not the code stuff. (Kind of **Abstract stuff**)
3. At the statement level, comment should descirbe *why* instead of *what*.

```cpp
/* Bad comment
* Set sight range to 0. 
* why bad ? : coz it shows literally what the code is doing.
*/*
sight = 0;

/* Good comment
* Player drank a potion of poison.
* why good ? : coz it shows what the code is doing logic wise.
*/
sight = 0;
```

**General shortcut to comment in IDEs :**  `ctrl + /`

----

# Objects & Variables

Direct memory access is discouraged in C++, each memory location is divided and operated upon in *byte-sized* manner.

- An object is a region of storage that can store a value.
- C++ favours OOPs paradigm in fact each and every stuff in c++ is an object in one way or another.
- An object when given a name is called **"Variable."**

Earlier on the size of byte (i.e. how many bits will be stored in 1 byte) was not standardized but completely free to the system designer.

Today it is pretty much standardized and each moder architecture stores `1 byte = 8 bits`

### Declaration of variables syntax in C++
```cpp
int num1, num2; // Can do but not recommended.
int num1, float num2; // Error : Can't declare different types in same statement.
int num1;
int num2; // For better legibility.

// Suggestion: Prefer list initialization
int num1{7}; // Avoid narrow conversion and intialize it properly.
```

### Identifier naming rules :
1. Cannot be a keyword.
2. Can only be composed of letters, numbers and underscore(\_).
3. identifier must not start with a number.

**Best practices & conventions :**
1. Identifier names for user-defined type (struct, class, enums) should start with uppercase letter.
2. Personal preference : for variables : `snake_case` | for functions : `camelCase`
3. Make the length of identifier as per frequency used.
4. For constant variables : `kConstantValue` prefixed with letter 'k'

**Fun-fact:**
>Identifier names must not start with a number because of fortran back then fortran and basic(only designed to teaching purpose) used numbers to denote the flow of program, which may lead to identifier prefixed with number resulting in an error.

### Related terms :
1. Unintialized  : A variable that has not given a known value. It's value will be whatever is already stored at that particular memory address.
2. Initialized  : A variable that is given a known value at the point of definition.
3. Assignment  : A variable that is given a value but later on in another statement.

**Fun Fact:**
>Lack of initialization is a performance improvement inherited from C language. Earlier on it was really costly to execute even the basic functions like assignment coz of expensive cycles.
>PS: We are living in the golden age of computing!

---
# Undefined behaviour
Result of executing code whose behaviour is not well-defined by the C++ language. It can lead to a couple of invisible bugs later on down the line.

### Symptoms that might show presence of undefined behaviour.
- Program produces different results every time it is run.
- Program consistently produces the incorrect result.
- Program behaves inconsistently.
- Program crashes immediately or later.
- Program may or may not compile on different compilers.

---

