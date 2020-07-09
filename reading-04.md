# Classes and Memory Management

## Classes
- Classes are reference types. At run time these have a null value unless declared with the ```new``` operator, or assign it to another object of compatible type.
- They are declared using the ``class``` operator followed by its identifying name.
- Have access levels as well.
- Objects are not classes, but classes define the types of objects.
- A ```new``` object is passed to the user by reference meaning that the variable itself does not contain all of the data.
- Inheritance allows data and behaviors of a class to be given to a potentially new class that can then add to the set of data and behaviors.
- A base class inherits everything except constructors.

## Constructors
- Has a name that acts as its type.
- There is a constructor for every class.
- Static constructors can be initialized, otherwise the compiler will use a default value.

## Properties
- A property is a member that provides a flexible mechanism to read, write, or compute the value of a private field.
- Properties enable a class to expose a public way of getting and setting values, while hiding implementation or verification code.
- Properties can be read-write, read-only, or write-only; they use the proper combinations of ```get``` and/or ```set```.

## Stack and Heap
- Stack: FILO order of operations wherin each new function that is being call goes on top of the stack, is run, then is popped of the top of it.
- Heap: All the related data is stored there and can be accessed in any order. This is great, except it cannot clean itself up like the stack. Additional management is required.
- Garbage Collection is the action of deleting any unrelated items in the heap after a program is run, both to keep data safe and to maintain performance

## Garbage Collection Fundamentals
- The heap lives in virtual memory where the programmer can control (as opposed to the physical memory).
- Virtual Memory can can be: Free, Reserved, or Committed.
- When a new process is started, the runtime reserves a piece of contiguous memory for it called the managed heap.
- Garbage collection occurs if the system has low physical memory, the memory that's used by allocated objects on the managed heap surpasses an acceptable threshold, or the ```GC.Collect``` method is called.



[Table of Contents](README.md)