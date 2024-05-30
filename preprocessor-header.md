
# Pre-processor in C++

**Building** term refers to multiple process that converts a source code into an executable.

![[Pasted image 20240530144434.png]]

It consists of following stages :-
- Pre-processing
- Compiling
- Linking

## Pre-processor directives

Directives or statements written for pre-processor to operate upon.
starts with `#`

`#include <headerFileName>`
`#define FILE_H`
`#define HELLO 5`
`#pragma once`
`#ifdef` or `#ifndef` or `#endif`

## Header files

Header files typically consists for function & variables forward declarations.

To include header file named *user.h*
`#include "user.h"`

Above directive will just copy and paste content from this file to the file it is being included into.

File : print.cpp
```cpp
#include "Print.h"
#include <iostream>

void Print(const char* text){
	std::cout << text << std::endl;
}
```

File : print.h
```cpp
#ifndef PRINT_H     // header guards to make preprocessor not to
#define PRINT_H     // include same file twice in the program.

// Forward declaration
void Print(const char* text);

#endif
```

File : main.cpp
```cpp
#include "Print.h"

int main(){
	Print("Hello world");
}
```

---
