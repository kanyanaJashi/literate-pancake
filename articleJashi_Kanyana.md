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

An example of syntax error:

#theofficefacts.py <br/>
<em><strong>ages = { <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'pam': 24,<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'jim': 24 <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'michael': 43 <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} <br/>
print(f'Michael is {ages["michael"]} years old.')

$ python theofficefacts.py <br/>
File "theofficefacts.py", line 5 <br/>
'jim': 24 <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ^^
SyntaxError: invalid syntax. Perhaps you forgot a comma?

Process finished with exit code 1</strong></em>




## What is a runtime error?
A runtime error is an error which occurs when a program is syntactically correct but contains an issue that is only detected during program execution. Errors that occur at runtime (after passing the syntax test) are called exceptions or logical errors.

## What is a Logic error?
A logic error is an error in a program’s code that gives way to unanticipated and erroneous behavior. A logic error is classified as a type of runtime error that can result in a program producing an incorrect output. It can also cause the program to crash when running.
Logic errors are not always easy to recognize immediately. This is due to the fact that such errors, unlike that of syntax errors, are valid when considered in the language, but do not produce the intended behavior. These can occur in both interpreted and compiled languages. A logic error is also known as a semantic error.
## What’s an Exception?
An exception in Python is an incident that happens while executing a program that causes the regular course of the program's commands to be disrupted. When a Python code comes across a condition it can't handle, it raises an exception. An object in Python that describes an error is called an exception. When a Python code throws an exception, it has two options: handle the exception immediately or stop and quit. Thus, an exception is a signal that a condition has occurred that can’t be easily handled using the normal flow-of-control of a Python program. Exceptions are often defined as being “errors”
but this is not always the case. All errors in Python are dealt with using exceptions, but not all exceptions are errors.
If you have been coding in Python for any length of time, no doubt you have seen a traceback. Just in case you haven't, here we'll make one happen. You can open up a Python console and type in the statements that follow, or just read along:


<em><strong>list1 = [1,2,3]<br />             
list1['apples']<br />           
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: list indices must be integers, not str <br />
list1[4]                      
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range <br />
list[1]
2</strong></em>


So here is what we just did. In line 1 we made a list with three elements in it. Line 2 tries to access the element at the index 'apples'. Now, since that's just really not right, Python complains. It does so by raising a TypeError. TypeError is a kind of Exception. When an Exception gets raised and but does not get caught, then it ends up printing a traceback to the error output. In the case of the Python console, the error output is just the console. A traceback message gives some information about the actual error and gives some detail about how we got to the point where the error actually happened.
The TypeError complains that it was expecting an integer and not a string. This seems like a pretty reasonable reaction. So in line 3 we give it an integer. Unfortunately the only indices available for list1 are 0,1 and 2, but we're trying to access list1[4]. Naturally this also isn't right. So Python complains again by raising an IndexError and printing an appropriate traceback.
Finally, we do something sensible and access list1[1]. This, as compared to our other attempts, is right. list1[1] has the value 2.
Python uses Exceptions to tell on bad code. Exceptions are raised when something doesn't work according to plan, where the program cannot proceed. And there are different types of exceptions for different situations.

## Type of Exceptions:
There are two types of exceptions in Python :
### Built-in Exceptions
In Python, exceptions are objects of the exception classes. All exception classes are the subclasses of the BaseException class.
However, almost all built-in exception classes inherit from the Exception class, which is the subclass of the BaseException class:
The built-in exceptions can be generated by the interpreter or built-in functions.
There are several built-in exceptions in Python that are raised when errors occur. These built-in exceptions can be viewed using the locals() built-in functions as follows :

list(dir(locals()['__builtins__']))</strong></em>



 |**Exceptions**|**Causes**|
 | :- | :- |
 |**AssertionError**|Raised when an assert statement fails.|
 |**AttributeError**|Raised when attribute assignment or reference fails.|
 |**EOFError**|Raised when the input() function hits end-of-file condition|
 |**FloatingPointError**|Raised when a floating point operation fails.|
 |**GeneratorExit**|Raise when a generator's close() method is called.|
 |**ImportError**|Raised when the imported module is not found.|
 |**IndexError**|Raised when the index of a sequence is out of range.|
 |**KeyError**|Raised when a key is not found in a dictionary.|
 |**KeyboardInterrupt**|Raised when the user hits the interrupt key (Ctrl+C or Delete).|
|**MemoryError**|Raised when an operation runs out of memory.|
|**NameError**|Raised when a variable is not found in local or global scope.|
|**NotImplementedError**|Raised by abstract methods.|
|**OSError**|Raised when system operation causes system related error.|
|**OverflowError**|Raised when the result of an arithmetic operation is too large to be represented.|
|**ReferenceError**|Raised when a weak reference proxy is used to access a garbage collected referent.|
|**RuntimeError**|Raised when an error does not fall under any other category.|
|**StopIteration**|Raised by next() function to indicate that there is no further item to be returned by iterator.|
|**SyntaxError**|Raised by parser when syntax error is encountered.|
|**IndentationError**|Raised when there is incorrect indentation.|
|**TabError**|Raised when indentation consists of inconsistent tabs and spaces.|
|**SystemError**|Raised when interpreter detects internal error.|
|**SystemExit**|Raised by sys.exit() function.|
|**TypeError**|Raised when a function or operation is applied to an object of incorrect type.|
|**UnboundLocalError**|Raised when a reference is made to a local variable in a function or method, but no value has been bound to that variable.|
|**UnicodeError**|Raised when a Unicode-related encoding or decoding error occurs.|
|**UnicodeEncodeError**|Raised when a Unicode-related error occurs during encoding.|
|**UnicodeDecodeError**|Raised when a Unicode-related error occurs during decoding.|
|**UnicodeTranslateError**|Raised when a Unicode-related error occurs during translating.|
|**ValueError**|Raised when a function gets an argument of correct type but improper value.|
|**ZeroDivisionError**|Raised when the second operand of division or modulo operation is zero.|





Example of built-In Exception <br>

<em><strong>

def division(a, b): <br>
&emsp;&emsp;return a / b <br>

</strong></em>

c = division(10, 0) <br>

Output: <br>
<em><strong>
ZeroDivisionError: division by zero

</strong></em>



## User-define Exceptions or Custom Exceptions

We can use raise to throw an exception if a condition occurs, as typical user/programmer defined exception . The statement is complemented with a custom exception.

![alt text](https://files.realpython.com/media/raise.3931e8819e08.png)

<em><strong>x=10 <br />
if x>5: <br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; raise Exception('x should not exceed 5. The value of x was: {}'.format(x))

Exception                                 Traceback (most recent call last)
~\AppData\Local\Temp\ipykernel_20732\3673638409.py in <cell line: 1>()
      1 if x>5:
----> 2     raise Exception('x should not exceed 5. The value of x was: {}'.format(x))

Exception: x should not exceed 5. The value of x was: 6</strong></em>

## Exception handling

In Python programming, exception handling allows a programmer to enable flow control. Using try-except is the most common and natural way of handling unexpected errors along with many more exception handling constructs. We’ll get to explore some of the best techniques to use try-except in Python.

Exception handling is very critical for creating robust and stable applications. And it encourages programmers to write clean, readable and error-free code.

You would agree that even the best of the code could behave unexpectedly at runtime. It could be due to a missing configuration, or a change in the execution environment or the user entered the wrong input.

Some of these errors may cause the program to terminate abruptly. With the help of Python exception handling, we can manage the above issues and avoid intermittent failures of our code.    

#### How to Handle Exceptions with Try-Except?
What is Try-Except Statement?
We use the try-except statement to enable exception handling in Python programs.

Inside the try block, you write the code which can raise an exception.

And the code that handles or catches the exception, we place in the except clause.

#### Python Exception Handling Syntax
Following is the syntax of a Python try-except-else block.  

<em><strong>try:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;You do your operations here; <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.................................................... <br/>
except ExceptionI: <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;If there is ExceptionI, then execute this block. <br/>
except ExceptionII: <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;If there is ExceptionII, then execute this block. <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.................................................... <br/>
else: <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;If there is no exception then execute this block. <br/></strong></em>

Here is a checklist for using the Python try statement effectively.<br/>

A single try statement can have multiple except statements depending on the requirement. In this case, a try block contains statements that can throw different types of exceptions.
We can also add a generic except clause which can handle all possible types of exceptions.
We can even include an else clause after the except clause. The instructions in the else block will execute if the code in the try block doesn’t raise an exception.

#### Python Exception Handling Examples
Let’s take a sample code to understand the use of Python try-except.<br/>

<em><strong>try:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; fob = open("test", "w") <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; fob.write("This is my test file for exception handling!!") <br/>
except IOError: <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; print "Error: can\'t find the file or read data" <br/>
else:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; print "Write operation is performed successfully on the file" <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; fob.close()</strong></em>

The above code produces the following output:
>Write operation is performed successfully on the file.


Let’s take another example in which we are trying to open a file in the READ mode.

We’ll perform a WRITE operation on it. Upon execution, it’ll throw an exception.

<em><strong>try:<br>
&emsp; fob = open("test", "r") <br>
&emsp; fob.write("It's my test file to verify exception handling in Python!!") <br>
except IOError: <br/>
&emsp; print "Error: can\'t find the file or read data" <br/>
else: <br/>
&emsp;print "Write operation is performed successfully on the file"

The above code produces the following output.</strong></em>

>Error: can't find file or read data
Handling All Types of Exceptions with Except
If we use a bare “except” clause, then it would catch all types of exceptions.

However, neither it’s a good programming practice nor does anyone recommend it.

It is because that such a Python try-except block can handle all types of exceptions. But it will not help the programmer to find what exception caused the issue.

You can go through the below code to see how to catch all exceptions.

#### Example

<em><strong>try:<br>
&emsp;You do your operations here; <br>
&emsp;.................................... <br>

except: <br>
&emsp;If there is any exception, then execute this block. <br>
&emsp; ...................... <br>

else: <br>
&emsp; If there is no exception then execute this block. <br> </strong></em> <br/>


#### Handling Multiple Exceptions with Except

We can define multiple exceptions with the same except clause. It means that if the Python interpreter finds a matching exception, then it will execute the code written under the except clause.

In short, when we define except clause in this way, we expect the same piece of code to throw different exceptions. Also, we want to take the same action in each case.

Please refer to the below example.

Example

<em><strong>try:<br>
&emsp; You do your operations here; <br/>
&emsp; ...................... <br>

except(Exception1[, Exception2[,...ExceptionN]]]):<br/>
&emsp; If there is any exception from the given exception list,
then execute this block.<br>
&emsp; ...................... <br/>

else:<br/>
&emsp; If there is no exception then execute this block <br/>
</strong></em>

How to handle Exceptions with Try-Finally?
What is Try-Finally Statement?
We can also enable Python exception handling with the help of try-finally statement.

With try block, we also have the option to define the “finally” block. This clause allows defining statements that we want to execute, no matters whether the try block has raised an exception or not.

This feature usually comes in the picture while releasing external resources.

Here is the coding snippet for help.

<em><strong> try: <br/>
&emsp; You do your operations here; <br/>
&emsp; ...................... <br/>

&emsp; Due to any exception, this may be skipped. <br/>

finally: <br/>
&emsp; This would always be executed.<br/>
&emsp; ...................... <br/>
</strong></em>

Examples <br/>
One critical point is that we can either define an “except” or a “finally” clause with every try block. You can’t club these together. Also, you shouldn’t use the “else” clause along with a “finally” clause.

Let’s take an example to get more clarity. <br>

<em><strong>
try:<br/>
&emsp; fob = open('test', 'w') <br/>
&emsp; fob.write("It's my test file to verify try-finally in exception handling!!") <br/>
&emsp; print 'try block executed'<br>
finally: <br>
&emsp; fob.close() <br/>
&emsp; print 'finally block executed' <br/>
</strong></em>

If the exception doesn’t occur, then you’ll see the following output.

>try block executed <br/>
>finally block executed

Suppose we open the file in the READ mode and then try to perform a write operation on it. In such a situation, below code will help to handle the exception. <br>

<em><strong>
try: <br>
&emsp;&emsp; fob = open('test', 'r') <br>
&emsp;&emsp; try: <br>
&emsp;&emsp;&emsp;&emsp; fob.write("It's my test file to verify try-finally in exception handling!!") <br>
&emsp;&emsp;&emsp;&emsp; print 'try block executed' <br>
&emsp;&emsp;finally: <br>
&emsp;&emsp;&emsp;&emsp; fob.close() <br>
&emsp;&emsp;&emsp;&emsp; print 'finally block executed to close the file' <br>
except IOError: <br>
&emsp;&emsp; print "Error: can\'t find file or read data"
In this case, the interpreter will raise an exception, and the following output will get displayed. </strong></em>
<br/>


>finally block executed to close the file <br>
>Error: can\'t find file or read data


When some code causes an exception in a try block, the execution immediately passes to the “finally” block. After all the statements in the “finally” block gets executed, the exception resumes to the “except” block for execution. But there must present a next higher layer of the “try-except” statement.

### Raise Exception with Arguments
##### What is Raise?
We can forcefully raise an exception using the raise keyword.
We can also optionally pass values to the exception and specify why it has occurred.
##### Raise Syntax
Here is the syntax for calling the “raise” method.

raise [Exception [, args [, traceback]]]

Where,

Under the “Exception” – specify its name.<br>
The “args” is optional and represents the value of the exception argument. <br>
The final argument, “traceback,” is also optional and if present, is the traceback object used for the exception.<br>

Let’s take an example to clarify this.

##### Raise Example

<em><strong>
raise MemoryError <br>
Traceback (most recent call last): <br>
... <br>
MemoryError <br>

</strong></em>

>raise MemoryError("This is an argument") <br>
Traceback (most recent call last): <br>
... <br>

MemoryError: This is an argument

<em><strong>
try:<br/>
&emsp;&emsp;a = int(input("Enter a positive integer value: ")) <br>
&emsp;&emsp;if a <= 0: <br>
&emsp;&emsp;&emsp;&emsp;raise ValueError("This is not a positive number!!") <br>
except ValueError as ve: <br>
&emsp;&emsp; print(ve)

</strong></em>


Following Output is displayed if we enter a negative number:

>Enter a positive integer: –5 <br>
This is not a positive number!! <br>
Create Custom Exceptions in Python <br>



## References
https://www.javatpoint.com/python-exception-handling#:~:text=In%20Python%2C%20we%20catch%20exceptions,lines%20that%20handle%20the%20exception.
https://www.programiz.com/python-programming/exceptions
https://www.techopedia.com/definition/13391/syntax-error
https://runestone.academy/ns/books/published/fopp/Exceptions/intro-exceptions.html?highlight=error
https://www.codementor.io/@sheena/how-to-write-python-custom-exceptions-du107ufv9
https://www.programiz.com/python-programming/exceptions
https://realpython.com/python-exceptions/
https://www.techbeamers.com/use-try-except-python/
