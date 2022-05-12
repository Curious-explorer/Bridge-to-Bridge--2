## Day 3 Notes ->

### Pointers and Memory Visdualization 
1. Pointers are variables, which contain the address of some other variables.
2. Syntax - datatype * pointername;
3. Note - Pointers also have data-types.
4. All data-types have memory values (i.e. the amount of memory the occupy), we can find that using sizeof(), but these numbers are not same for all
computers. So always check them.
5. If you try to assign value of a pointer to int, c will throw an error, because pointer of int is different datatype than int.
6. There are two unary operations to consider.
    - The * operator: If **ptra** is a pointer variable, then **∗ptra**
    gives you the content of the location pointed to by ptr.
    - The & operator: If **v** is a variable, then **&v** is the address of
    the variable.
7. The null pointer is the only integer literal that may be assigned to a pointer. 
You may NOT assign arbitrary numbers to pointers: int * p = 0; // okay.
8. There are three values that can be used to initialize a pointer; 0, NULL, or an address. Initializing a pointer to 0 and initializing that same pointer to NULL are identical. The only integer that can be assigned to a pointer is 0.
9. We can add pointers and compare them if they have same data-type. Also int and an int pointer can be added or subtracted. Details see - https://www.geeksforgeeks.org/pointer-arithmetics-in-c-with-examples/
10. If there is an error in a program using pointers, when executing,
you will most probably get “Segmentation Fault”.
There are several ways to find the error.
  - Go through the code carefully and see if you can locate the
        bug. (perfect!)
  - Use a debugger like gdb to debug the code and step through
        the execution to locate the error. Examine the memory
        contents when you debug.
  - Insert printf statements to pinpoint where the code crashes.
        (When doing so, make sure to put “\n” at the end of the
        message - it might not print otherwise!)
11. Pass by value vs pass by reference - https://www.educative.io/edpresso/pass-by-value-vs-pass-by-reference
