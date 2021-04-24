A storage class defines the ***scope*** (visibility) and ***life-time* **of variables and/or functions within a C Program. 

We have four different storage classes in a C program :
1. auto
2. register
3. static
4. extern

## auto
The ***auto*** storage class is the default storage class for all ***local variables***.
```c
{
   int mount;   //default auto
   auto int month;
}
```
## register
- The ***register*** storage class is used to define ***local variables*** that should be stored in a register instead of RAM. 
- it MIGHT be stored in a register depending on hardware and implementation restrictions.
- If the variable is storaged in a register, which has a maximum size equal to the register size (usually one word) .
- The register should only be used for variables that require quick access such as counters.
```c
{
   register int  counter;
}
```
## static
- The ***static*** storage class instructs the compiler to keep a ***local variable*** in existence during the ***life-time*** of the program instead of creating and destroying it each time it comes into and goes out of scope. 
- The static modifier can also be applied to ***global variable***, which causes that variable's scope to be restricted to the file in which it is declared and one copy of that member to be shared by all the objects of its class.

## extern
- The ***extern*** storage class is used to give a reference of a ***global variable*** that is visible to ***ALL*** the program files. It means that you define a ***global variable*** or ***function***, which will also be used in other files.
- The extern modifier is most commonly used when there are two or more files sharing the same global variables or functions.

**First File:main.c**
```c
#include <stdio.h>
 
int count ;
extern void write_extern();
 
main() {
   count = 5;
   write_extern();
}
```
**Second File: support.c**
```c
#include <stdio.h>
 
extern int count;
 
void write_extern(void) {
   printf("count is %d\n", count);
}
```







