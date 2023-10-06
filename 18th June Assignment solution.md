1. What is the role of the 'else' block in a try-except statement? Provide an example
scenario where it would be useful.

Ans:-The try block lets you test a block of code for errors. The except block lets you handle the error. The else block lets you execute code when there is no error. The finally block lets you execute code, regardless of the result of the try- and except blocks.

```python
#Ex:-
try:
    print(x)  
except :
    print("There is no x") 
else:
    print("No error")
```

    There is no x
    
2. Can a try-except block be nested inside another try-except block? Explain with an
example.

Ans:-We can have nested try-except blocks in Python. In this case, if an exception is raised in the nested try block, the nested except block is used to handle it.

```python
# Ex:-
try:

  with open('sample.txt', 'r') as reader:
     for line in reader.readlines():
        
        try:
            print(int(line))
        except:
            print('\nLine error')
            quit()             
        
except:
    print('\nError: cannot read from the file')
```

    
    Error: cannot read from the file
    
3. How can you create a custom exception class in Python? Provide an example that
demonstrates its usage.

Ans:-In Python, we can define custom exceptions by creating a new class that is derived from the built-in Exception class. Here's the syntax to define custom exceptions, class CustomError(Exception): ... pass try: ...

```python
# Ex:-
class CustomException(Exception):
    def __init__(self, message, error_code):
        self.message = message
        self.error_code = error_code

try:
    raise CustomException("Something went wrong.", 500)
except CustomException as e:
    print(f"Error: {e.message}")
    print(f"Error Code: {e.error_code}")
```

    Error: Something went wrong.
    Error Code: 500
    
4. What are some common exceptions that are built-in to Python?

Ans:-Built-in Exceptions in Python are  EOFError,FloatingPointError,IndexError,MemoryError,OverflowError,TabError,ValueError etc.

5. What is logging in Python, and why is it important in software development?

Ans:-Logging is a way to store information about your script and track events that occur.
 Logging is important for software developing, debugging, and running. If you don't have any logging record and your program crashes, there are very few chances that you detect the cause of the problem.

 6. Explain the purpose of log levels in Python logging and provide examples of when
each log level would be appropriate.

Ans:-There are six levels for logging in Python; each level is associated with an integer that indicates the log severity: NOTSET=0, DEBUG=10, INFO=20, WARN=30, ERROR=40, and CRITICAL=50. All the levels are rather straightforward (DEBUG < INFO < WARN ) except NOTSET, whose particularity will be addressed next.


```python
import logging
logging.basicConfig(level=logging.DEBUG)

def add(x,y):
    logging.debug('variables are %s and %s' , x, y)
    return x + y
    
add(2,3)
```

    DEBUG:root:variables are 2 and 3
    




    5




```python
import logging
logging.basicConfig(level=logging.INFO)

def login123(user):
    logging.info('user name is %s', user)
    
login123("Admin") 

```

    INFO:root:user name is Admin
    


```python
import logging
logging.basicConfig(level=logging.WARNING)

def myBalance(amount):
    if amount < 4000:
       logging.warning('Sorry you have low balance,your balance is %s',amount)
    
myBalance(1000)   
```

    WARNING:root:Sorry you have low balance,your balance is 1000
    


```python
import logging
logging.basicConfig(level=logging.ERROR)

def DivideByZero(n,d):
    try:
        results = n / d
    except ZeroDivisionError:
        logging.error("Division by Zero")
    else:
        print(results)
        
DivideByZero(5,0)        
```

    ERROR:root:Division by Zero
    


```python
import logging
logging.basicConfig(level=logging.CRITICAL)

def LetusCheckSystem(sys):
    if sys != 'ok':
        logging.critical('System failed to boot: %s',sys)
        
LetusCheckSystem("You need to handle this issue")       
        
```

    CRITICAL:root:System failed to boot: You need to handle this issue
    
7. What are log formatters in Python logging, and how can you customise the log
message format using formatters?

Ans:-A formatter is created and added to the handler to transform log messages into placeholder data. In this formatter, the time of the log request (as an epoch timestamp), the logging level, the logger's name, the module name, and the log message will all print.

I customise the log message format using formatters are
formatter = logging.Formatter(‘%(asctime)s – %(name)s – %(levelname)s:
%(message)s’, datefmt=’%d/%m/%Y %I:%M:%S %p’)

8. How can you set up logging to capture log messages from multiple modules or
classes in a Python application?

Ans:-The basics of using the logging module to record the events in a file are very simple.  For that, simply import the module from the library.  

1.Create and configure the logger. It can have several parameters. But importantly, pass the name of the file in which you want to record the events.

2.Here the format of the logger can also be set. By default, the file works in append mode but we can change that to write mode if required.

3.Also, the level of the logger can be set which acts as the threshold for tracking based on the numeric values assigned to each level.There are several attributes that can be passed as parameters.

4.The list of all those parameters is given in Python Library. The user can choose the required attribute according to the requirement.After that, create an object and use the various methods as shown in the example.

9. What is the difference between the logging and print statements in Python? When
should you use logging over print statements in a real-world application?

Ans:-
Logging in Python:-

Logging in Python is a technique to display useful messages and warnings to users. The logging module provides a flexible way to log different messages in various output destinations such as on the console, in files, and on networks. Logging is a best practice for production code. The logging module provides features such as log levels and filtering.


```python
# Ex:-
import logging
  
# creating the logger object
logger = logging.getLogger()
  
# setting logger to a warning message
logger.warning('This is a Warning message!')
  
# configuring the logger to info log levek
logging.basicConfig(level=logging.INFO)
  
# setting the logger to a informative message
logging.info("This is an Informative message.")

```

    WARNING:root:This is a Warning message!
    INFO:root:This is an Informative message.
    
Print in Python:-

The print statement is a built-in function in Python that prints the specified value or values to the console. It is mainly used for debugging and is not recommended for logging information in production code.


```python
# Ex:-
name = "Rojalin"
age = 24
print("My name is", name, "and I'm", age, "years old.")

```

    My name is Rojalin and I'm 24 years old.
    
With the use of Loggers, we can customize what information is to be printed along with the actual message. The information that we can print includes the package name, log level, line number, timestamp, method name, etc.


10. Write a Python program that logs a message to a file named "app.log" with the
following requirements:
● The log message should be "Hello, World!"
● The log level should be set to "INFO."
● The log file should append new log entries without overwriting previous ones.

```python
# app.py
import logging


def main():
    logging.basicConfig(filename='app.log', level=logging.INFO)
    logging.info('Started')
    
    logging.info('Finished')

if __name__ == '__main__':
    main()
```

    INFO:root:Started
    INFO:root:Finished
    


```python
import logging
 
logging.basicConfig(filename='app.log', filemode='w', format='%(name)s - %(levelname)s - %(message)s')
logging.warning('The log message should be "Hello, World!"')
```

    WARNING:root:The log message should be "Hello, World!"
    
