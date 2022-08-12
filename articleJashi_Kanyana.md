# Python Exceptions

The main goal here is to understand what an exception is in Python. 
Python, well known as a high-level, interpreted, general-purpose programming language with its design philosophy emphasizing code readability with the use of significant indentation, dynamically-typed and garbage-collected, supporting multiple programming paradigms, including structured (particularly procedural), object-oriented and functional programming.

## Errors in Python:
When a Python program meets an error, it stops the execution of the rest of the program. An error in Python might be either syntax errors, logic errors or exceptions . Logic errors and some exceptions are runtime errors.
##What is a syntax error?
Syntax errors are the most basic type of error. They arise when the Python parser is unable to understand a line of code. A syntax error is an error in the syntax of a coding or programming language, entered by a programmer. Syntax errors are caught by the Python parser, and the programmer must fix them before the program runs . Syntax errors are almost always fatal, it means there is almost never a way to successfully execute a piece of code containing syntax errors. The syntax error is an incorrect construction or misspelling in the code. Most syntax errors are typos, incorrect indentation, or incorrect arguments.
One way to think of a syntax error is that it presents a significant gatekeeping function in the clarity and usability of code. As in other digital technologies such as an email address, the omission or misplacement of just one letter, number or character creates critical problems for a computing system that has to read code in a linear way. It is also helpful to think about the usual causes of syntax errors – either a programmer makes a typographical error, or forgets the format or sequence of some word or command, it’s an Error caused by not following the proper structure (syntax) of the language is called.

Syntax errors are different from errors that affect programs during run time. Many logical errors in computer programming do not get caught by the compiler, because although they may cause grievous errors as the program runs, they do conform to the program's syntax. In other words, the computer cannot tell whether a logical error is going to create problems, but it can tell when code does not conform to the syntax, because the understanding of that syntax is built into the compiler’s native intelligence.

Another aspect of understanding syntax errors is that they demonstrate how, unlike humans, computers cannot use input that is not perfectly designed. The lack of a period or comma in a sentence or command, or two swapped letters in a word, confounds the compiler and makes its work impossible. On the other hand, human readers can spot typographical errors and understand them in the context of what they are reading. It is likely that as computers evolve through the coming decades, engineers may be able to create compilers and systems that can handle some types of syntax errors; even now, in some compiling environments, tools can auto-correct syntax errors on site. 
### An example of syntax error:


## What’s runtime error?
A runtime error is an error which occurs when a program is syntactically correct but contains an issue that is only detected during program execution. Errors that occur at runtime (after passing the syntax test) are called exceptions or logical errors.

## What is a Logic error?
A logic error is an error in a program’s code that gives way to unanticipated and erroneous behavior. A logic error is classified as a type of runtime error that can result in a program producing an incorrect output. It can also cause the program to crash when running.
Logic errors are not always easy to recognize immediately. This is due to the fact that such errors, unlike that of syntax errors, are valid when considered in the language, but do not produce the intended behavior. These can occur in both interpreted and compiled languages. A logic error is also known as a semantic error.
## What’s an Exception?
An exception in Python is an incident that happens while executing a program that causes the regular course of the program's commands to be disrupted. When a Python code comes across a condition it can't handle, it raises an exception. An object in Python that describes an error is called an exception. When a Python code throws an exception, it has two options: handle the exception immediately or stop and quit. Thus, an exception is a signal that a condition has occurred that can’t be easily handled using the normal flow-of-control of a Python program. Exceptions are often defined as being “errors” 
