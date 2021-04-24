A storage class defines the ***scope*** (visibility) and ***life-time* **of variables and/or functions within a C Program. 

We have four different storage classes in a C program :
1. auto
2. register
3. static
4. extern

## auto
The auto storage class is the default storage class for all ***local variables***.
```c
{
   int mount;   //default auto
   auto int month;
}
```
## register
- The register storage class is used to define ***local variables*** that should be stored in a register instead of RAM. 
- it MIGHT be stored in a register depending on hardware and implementation restrictions.
- If the variable is storaged in a register, which has a maximum size equal to the register size (usually one word) .
- The register should only be used for variables that require quick access such as counters.
```c
{
   register int  counter;
}
```
## static
- The static storage class instructs the compiler to keep a ***local variable*** in existence during the life-time of the program instead of creating and destroying it each time it comes into and goes out of scope. 



