1. What is the role of try and exception block?

Ans:-The try block lets you test a block of code for errors. The except block lets you handle the error.The else block lets you execute code  when there is no error.

2. What is the syntax for a basic try-except block?

Ans:-Example: Exception Handling Using try...except
try: numerator = 10 denominator = 0 result = numerator/denominator print(result) except: print("Error: Denominator cannot be 0.") # Output: Error: Denominator cannot be 0. In the example, we are trying to divide a number by 0. Here, this code generates an exception.

3. What happens if an exception occurs inside a try block and there is no matching
except block?

Ans:-If any exception occurs, the try clause will be skipped and except clause will run. If any exception occurs, but the except clause within the code doesn't handle it, it is passed on to the outer try statements. If the exception is left unhandled, then the execution stops.

4. What is the difference between using a bare except block and specifying a specific
exception type?

Ans:-A bare except: clause will catch SystemExit and KeyboardInterrupt exceptions, making it harder to interrupt a program with Control-C, and can disguise other problems.

For each try block, there can be zero or more except blocks. Multiple except blocks allow us to handle each exception differently. The argument type of each except block indicates the type of exception that can be handled by it.

5. Can you have nested try-except blocks in Python? If yes, then give an example.

Ans:-We can have nested try-except blocks in Python. In this case, if an exception is raised in the nested try block, the nested except block is used to handle it. In case the nested except is not able to handle it, the outer except blocks are used to handle the exception.


```python
try:
   print("outer try block")
   try:
       print("Inner try block")
   except ZeroDivisionError:
       print("Inner except block")
   finally:
       print("Inner finally block")
except:
   print("outer except block")
finally:
   print("outer finally block")
```

    outer try block
    Inner try block
    Inner finally block
    outer finally block
    
6. Can we use multiple exception blocks, if yes then give an example.

Ans:-Using a list of exception types you can catch multiple exceptions in a single except block in Python. This method is similar to using a tuple of exception types, but it allows you to easily add or remove exception types as needed.


```python

try:
    n = int(input("Enter num1: "))
    d = int(input("Enter num2: "))

    result = n / d
    print("Results",result)
    
except ZeroDivisionError:
    print("You have divided the number by zero")
```

    Enter num1: 6
    Enter num2: 0
    You have divided the number by zero
    
7. Write the reason due to which following errors are raised:
a. EOFError
b. FloatingPointError
c. IndexError
d. MemoryError
e. OverflowError
f. TabError
g. ValueError

Ans:- a.EOFError- Raised when the input() method hits an "end of file" condition (EOF)
b. FloatingPointError- Raised when a floating point calculation fails
c. IndexError-	Raised when an index of a sequence does not exist
d. MemoryError- Raised when a program runs out of memory
e. OverflowError- Raised when the result of an arithmetic operation is too large to be represented
f. TabError- Raised when indentation consists of tabs or spaces
g. ValueError-	Raised when there is a wrong value in a specified data type

8. Write code for the following given scenario and add try-exception block to it.
a. Program to divide two numbers
b. Program to convert a string to an integer
c. Program to access an element in a list
d. Program to handle a specific exception
e. Program to handle any exception

```python
# a. Program to divide two numbers
try:
    n = int(input("Enter num1: "))
    d = int(input("Enter num2: "))

    result = n / d
    print("Results",result)
    
except ZeroDivisionError:
    print("You have divided the number by zero")

```

    Enter num1: 8
    Enter num2: 0
    You have divided the number by zero
    


```python
# b. Program to convert a string to an integer
a_string = "14"

try:
    an_integer = int(a_string)
    print(an_integer)
except valueError:
    print("Catch Error")
```

    14
    


```python
# c. Program to access an element in a list
try:
    list1 = [11 , 12 , 13 , 14]
    print(list1[4])
    
except IndexError:
    print("Wrong Index")
```

    Wrong Index
    


```python
# d. Program to handle a specific exception
try:
    numerator = 10
    denominator = 0
    
    result = numerator/denominator
    
    print(result)
    
except:
    print("Error: Denominator cannot be 0.")
    
```

    Error: Denominator cannot be 0.
    


```python
# e. Program to handle any exception
try:
    print(x)  
except :
    print("There is no x") 
else:
    print("No error")
```

    There is no x
    
