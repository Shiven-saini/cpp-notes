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
