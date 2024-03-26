# Enum in C

## How is enum data stored in memory?
Enum data is typically stored in memory as integer values. Each enum value is assigned an integer that represents its position within the enum. When the program runs, these integer values are used to represent the enum values in memory. This allows for efficient storage and comparison of enum values within the program.

`Example:`

**Code**
~~~cpp
#include<iostream>
#include <cstdint>

enum foo
{
    typeA = 0,
    typeB,
    typeC
};

enum two : int8_t
{
    typeD = 0,
    typeE,
    typeF
};

enum bar : uint64_t
{
    typeG = 0,
    typeH,
    typeK
};
int main()
{
    std::cout << "Size of <foo> type variable: " << sizeof(foo) << " bytes" << std::endl;
    std::cout << "Size of <bar> type variable: " << sizeof(two) << " bytes" << std::endl;
    std::cout << "Size of <bar> type variable: " << sizeof(bar) << " bytes" << std::endl;
    return 0;
}
~~~
**Output:**
~~~cpp
Size of <foo> type variable: 4 bytes
Size of <two> type variable: 1 bytes
Size of <bar> type variable: 8 bytes
~~~
