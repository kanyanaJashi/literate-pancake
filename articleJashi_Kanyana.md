# Python Exceptions

The main goal here is to understand what an exception is in Python.
Python, well known as a high-level, interpreted, general-purpose programming language with its design philosophy emphasizing code readability with the use of significant indentation, dynamically-typed and garbage-collected, supporting multiple programming paradigms, including structured (particularly procedural), object-oriented and functional programming.
Let's come from a perspective of studying exceptions from a well known notion of errors, there will be some good reason that we'll discover together in this developpement.


## Errors in Python:
When a Python program meets an error, it stops the execution of the rest of the program. An error in Python might be either syntax errors, logic errors or exceptions . Thus, it is said Logic errors and some exceptions are runtime errors.

## What is a syntax error?
Syntax errors are the most basic type of error. They arise when the Python parser is unable to understand a line of code. A syntax error is an error in the syntax of a coding or programming language, entered by a programmer. Syntax errors are caught by the Python parser, and the programmer must fix them before the program runs . Syntax errors are almost always fatal, it means there is almost never a way to successfully execute a piece of code containing syntax errors. The syntax error is an incorrect construction or misspelling in the code. Most syntax errors are typos, incorrect indentation, or incorrect arguments.
One way to think of a syntax error is that it presents a significant gatekeeping function in the clarity and usability of code. As in other digital technologies such as an email address, the omission or misplacement of just one letter, number or character creates critical problems for a computing system that has to read code in a linear way. It is also helpful to think about the usual causes of syntax errors – either a programmer makes a typographical error, or forgets the format or sequence of some word or command, it’s an Error caused by not following the proper structure (syntax) of the language is called.

Syntax errors are different from errors that affect programs during run time. Many logical errors in computer programming do not get caught by the compiler, because although they may cause grievous errors as the program runs, they do conform to the program's syntax. In other words, the computer cannot tell whether a logical error is going to create problems, but it can tell when code does not conform to the syntax, because the understanding of that syntax is built into the compiler’s native intelligence.

Another aspect of understanding syntax errors is that they demonstrate how, unlike humans, computers cannot use input that is not perfectly designed. The lack of a period or comma in a sentence or command, or two swapped letters in a word, confounds the compiler and makes its work impossible. On the other hand, human readers can spot typographical errors and understand them in the context of what they are reading. It is likely that as computers evolve through the coming decades, engineers may be able to create compilers and systems that can handle some types of syntax errors; even now, in some compiling environments, tools can auto-correct syntax errors on site.

### An example of syntax error:


## What is a runtime error?
A runtime error is an error which occurs when a program is syntactically correct but contains an issue that is only detected during program execution. Errors that occur at runtime (after passing the syntax test) are called exceptions or logical errors.

## What is a Logic error?
A logic error is an error in a program’s code that gives way to unanticipated and erroneous behavior. A logic error is classified as a type of runtime error that can result in a program producing an incorrect output. It can also cause the program to crash when running.
Logic errors are not always easy to recognize immediately. This is due to the fact that such errors, unlike that of syntax errors, are valid when considered in the language, but do not produce the intended behavior. These can occur in both interpreted and compiled languages. A logic error is also known as a semantic error.
## What’s an Exception?
An exception in Python is an incident that happens while executing a program that causes the regular course of the program's commands to be disrupted. When a Python code comes across a condition it can't handle, it raises an exception. An object in Python that describes an error is called an exception. When a Python code throws an exception, it has two options: handle the exception immediately or stop and quit. Thus, an exception is a signal that a condition has occurred that can’t be easily handled using the normal flow-of-control of a Python program. Exceptions are often defined as being “errors”
but this is not always the case. All errors in Python are dealt with using exceptions, but not all exceptions are errors.
If you have been coding in Python for any length of time, no doubt you have seen a traceback. Just in case you haven't, here we'll make one happen. You can open up a Python console and type in the statements that follow, or just read along:


list1 = [1,2,3]               

list1['apples']               
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: list indices must be integers, not str

list1[4]                      
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range

list[1]
2


So here is what we just did. In line 1 we made a list with three elements in it. Line 2 tries to access the element at the index 'apples'. Now, since that's just really not right, Python complains. It does so by raising a TypeError. TypeError is a kind of Exception. When an Exception gets raised and but does not get caught, then it ends up printing a traceback to the error output. In the case of the Python console, the error output is just the console. A traceback message gives some information about the actual error and gives some detail about how we got to the point where the error actually happened.
The TypeError complains that it was expecting an integer and not a string. This seems like a pretty reasonable reaction. So in line 3 we give it an integer. Unfortunately the only indices available for list1 are 0,1 and 2, but we're trying to access list1[4]. Naturally this also isn't right. So Python complains again by raising an IndexError and printing an appropriate traceback.
Finally, we do something sensible and access list1[1]. This, as compared to our other attempts, is right. list1[1] has the value 2.
Python uses Exceptions to tell on bad code. Exceptions are raised when something doesn't work according to plan, where the program cannot proceed. And there are different types of exceptions for different situations.

## Type of Exceptions:

Built-in Exceptions

User-define Exceptions or Custom Exceptions




## References
https://www.javatpoint.com/python-exception-handling#:~:text=In%20Python%2C%20we%20catch%20exceptions,lines%20that%20handle%20the%20exception.
https://www.programiz.com/python-programming/exceptions
https://www.techopedia.com/definition/13391/syntax-error
https://runestone.academy/ns/books/published/fopp/Exceptions/intro-exceptions.html?highlight=error
https://www.codementor.io/@sheena/how-to-write-python-custom-exceptions-du107ufv9
