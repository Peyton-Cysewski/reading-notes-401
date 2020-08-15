# Exception Handling & Debugging

## Debugging for Absolute Beginners
- The first step is to ask the right questions. It helps to identify a specific behavior of the function before you begin the debugging process.
- Often you will have underlying assumptions about the code. It is beneficial to examine those so that you don't overlook anything.
- Try stepping through the code to find exactly where the breakpoint is at.
- The best approach is always to find the problem region of code, then carefully step through it to find the exact issue that is causing the error.

## Try/Catch
- Code can be placed in ```try``` block to execute the code.
- If an exception is thrown or expected to be thrown, then a ```catch``` block with the specified exception can handle the error.
- If an exception occurs that is not explicitly written in a ```catch``` block, then a dialog box will open with info about the exception.

## Exception Handling
- ```throw```: can be used to intentionally throw an exception.
- ```try-catch```: a ```try``` block followed by one or more ```catch``` clauses.
- ```try-finally```: the code in a ```finally``` block executes whenever the control leaves the ```try``` block, either intentionally or through an exception.
- ```try-catch-finally```: using all three of the code blocks together allows for code to run in the ```try``` block, exceptions to be handled in the ```catch``` block, and the resources to be released in the ```finally``` block.

## C# 8.0 in a Nutshell pg. 170-179
- The dynamic of exception handling is that a ```try``` block runs some code, the ```catch``` block has access to the exception object and information about the error, and the ```finally``` block adds determinism to the program performing relative actions or simple clean-up code.
- Catching ```System.Exception``` catches all possible errors as opposed to just a specific exception.
- Exception filters allow types of exceptions to be filtered out using a conditional after the catch conditional with a ```when```.
- ```finally``` blocks always will be executed.
- The ```using``` statement can be used to encapsulate the try-catch-finally structure with a ```Dispose``` method in the finally section to neatly wrap up that section of code.
- If an exception is caught, simply stating ```throw``` will re-throw the same exception.
Properties of ```System.Exception```:
- ```StackTrace```: a string representing all the methods that are called from the origin of the exception to the catch block.
- ```Message```: a string with a description of the error.
- ```InnerException```: The inner exception (if any) that caused the outer exception. This, itself, can have another ```InnerException```.

## Therac-25
- A radiation therapy machine that was controlled by software and produced in 1982 had poor software control safety systems that allowed bugs to expose patients to deadly levels of radiation. It is an extreme example of the consequence of engineers not doing their due diligence to make sure bugs are handled properly in a program.

## Ariane 5
- The first test flight of the Ariane 5 rocket in 1996 resulted in self-destruction because a data type was not properly protected in the code. The data mishap caused an operand error in the software that was not handled, ultimately leading to its own destruction.



[Table of Contents](../README.md)
