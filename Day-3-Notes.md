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
9. We can subtract pointers and compare them if they have same data-type **(We can not add them because memory is not infinite so C will throw an error if you try to add two pointers)**. Also int and an int pointer can be added or subtracted. Details see - https://www.geeksforgeeks.org/pointer-arithmetics-in-c-with-examples/
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
12. NOTE - variable name is actually the address of value that it is storing. And pointers are special variables which store address of other variables as value.
13. In C - **variable ++** is **post-increment** and **++ variable** is **preincrement**.
14. In C - the name of the array stores address of the first element. (Check the downloaded PPT in desktop to know more)
15. In pass by value we only pass the value, i.e. a new variable whose scope is limited to the function is created, and even the things which are returned are also values, not the variables. So if we want to update current varible we have to use pass by reference, in which we pass pointers or address of the variable. In this case the origian variable value will be modified (Note - we need to modify the value of a variable while scanf, hence over there we pass the address, and in printf we just need the value to display, hence in printf we only pass variable or value.)
16. One can say variables are special types of pointers who will reveal their address after using &variable operator.
17. NOTE - If you have a big nested if conditions, then try to convert them into bunch of if negative statements of original ones, and add return in each of them, this will allow you to seperate if statements and code will be more maintainable.
