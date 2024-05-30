
---
# Fundamental Data types in C++

Memory is organized in sequential units called 'memory address' which holds 1 byte each. Modern standard is `1 byte = 8 bits`

**Datatype :** It tells the compiler how to interpret the content of memory in some meaningful way. It tells how many bytes to sequentially club together to grab the data stored.

C++ comes with following built-in data types designed in the language itself :-

1. Floating Point : useful for storing no. with decimals, mantissa etc. **IEEE-754 Standard**
	1. `float :` 7-point precision means can store upto 7-digits of significant figures.
	2. `double :` 14-point precision 
	3. `long double :` much higher 16-point precision

2. Integral type : 
	1. `boolean :` true or false, not available in C.
	2. `character :` 
		1. `char :` 'A' or any ascii value. Generally 1 byte.
		2. `wchar_t :` Supports utf-8 characters.
		3. `char8_t`
		4. `char16_t`
		5. `char32_t`
	3. `integer :`
		1. `short int`
		2. `int`
		3. `long int`
		4. `long long int`

3. Miscellaneous types
	1. `std::nullptr_t :` Null pointer nullptr
	2. `void :` used for denoting no special type. *used in Void pointer*

*Unsigned numbers* should  be used carefully, may lead to many unnoticeable bugs.
*Signed numbers* should be noted for **modulo-operando behaviour.** i.e. memory overflow when the data exceeds the bits available in a data type.

### Fixed-width integers

Due to historical reasons, compilers were given freedom to defined data type size for performance on their respective machines.

To avoid variable size of data types and to make the code consistent on each architecture, 
`C++ 11` introduced the concept of fixed-width integer defined in `<cstdint>` header file.


> C++ ISO standard only defines the least size for datatypes not exact size compiler should opt.

### Fixed-width integers

Due to historical reasons, compilers were given freedom to defined data type size for performance on their respective machines.

To avoid variable size of data types and to make the code consistent on each architecture, 
`C++ 11` introduced the concept of fixed-width integer defined in `<cstdint>` header file.

| Data types      | Description     |
| --------------- | --------------- |
| `std::int8_t`   | 1 byte signed   |
| `std::uint8_t`  | 1 byte unsigned |
| `std::int16_t`  | 2 byte signed   |
| `std::uint16_t` | 2 byte unsigned |
| `std::int32_t`  | 4 byte signed   |
| `std::uint32_t` | 4 byte unsigned |
| `std::int64_t`  | 8 byte signed   |
| `std::uint64_t` | 8 byte unsigned |

**Tip :** 1. Don't focus too much on writing optimized code by over-emphasising datatypes.
		2. `sizeof()` operator can be used to check size of any datatype.
		3. A lot of modern architecture nowadays is more or like operates faster on some fixed size. Often CPU Cycles are the bottleneck not the memory consumption.
		4. When not sure if one data type would be sufficient enough to store data, instead use bigger size one.



---
