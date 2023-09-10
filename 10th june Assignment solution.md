1. In Python, what is the difference between a built-in function and a user-defined function? Provide an example of each.

Ans:-Built-in function are predefined functions which can be used anytime.
eg:len(),type(),etc.
User-defined function are functions that are defined by the programmer.
eg:def perimeter(b,l):p=2*(l+b)print(p)

2. How can you pass arguments to a function in Python? Explain the difference between positional
arguments and keyword arguments.

Ans:-Information can be passed into functions as arguments.Arguments are specified after the function name,inside the parentheses.You can add as many arguments as you want,just separate them with a comma.

Positional arguments:-
An Arguments are passed in the order of parameters. The order defined in the order function declaration.Order of values cannot be changed to avoid the unexpected output.
Syntax :-FunctionName(value1, value2, value3,....)

keyword arguments:-
Parameter Names are used to pass the argument during the function call.Order of parameter Names can be changed to pass the argument(or values) 
Syntax : – FunctionName(paramName = value, ...)


```python
## Positional arguments:-
complex(3,5)
```




    (3+5j)




```python
## keyword arguments:-
complex(real=3, imag=5)
```




    (3+5j)


3. What is the purpose of the return statement in a function? Can a function have multiple return
statements? Explain with an example.

Ans:-A return statement is used to end the execution of the function call and “returns” the result (value of the expression following the return keyword) to the caller. The statements after the return statements are not executed. If the return statement is without any expression, then the special value None is returned.

A function can have multiple return statements. When any of them is executed, the function terminates. A function can return multiple types of values. Python functions can return multiple values in a single return statement.


```python
## Example of Multiple return statement

def type_of_int(i):
    if i % 2 == 0:
        return 'even'
    else:
        return 'odd'
 
result = type_of_int(7)
 
print(result)

```

    odd
    
4. What are lambda functions in Python? How are they different from regular functions? Provide an
example where a lambda function can be useful.

Ans:-Lambda functions are similar to user-defined functions but without a name. They're commonly referred to as anonymous functions. Lambda functions are efficient whenever you want to create a function that will only contain simple expressions – that is, expressions that are usually a single line of a statement.

A lambda function is an anonymous function(i.e.,defined without a name) that can take any number of arguments but,unlike normal function,evaluates and returns only one expression.



```python
add = lambda x,y: x + y
print(add(6,4))
```

    10
    
5. How does the concept of "scope" apply to functions in Python? Explain the difference between local
scope and global scope.

Ans:-Local (or function) scope is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function.

Python Global variables are those which are not defined inside any function and have a global scope whereas Python local variables are those which are defined inside a function and their scope is limited to that function only.

6. How can you use the "return" statement in a Python function to return multiple values?

Ans:-In Python, we can return multiple values by simply separating them with commas in the return statement.In Python, comma-separated values are treated as tuples, even without parentheses, unless the syntax requires them. Therefore, the function in the example above returns a tuple.


```python
## Example

def add_num(num1, num2):
    sum = num1 + num2
    return sum
    
result = add_num(5, 3)
print("The sum of two number is:",result)
```

    The sum of two number is: 8
    
7.What is the difference between the "pass by value" and "pass by reference" concepts when it
comes to function arguments in Python?

Ans:-When you pass function arguments by reference, those arguments are only references to existing values. In contrast, when you pass arguments by value, those arguments become independent copies of the original values.

8. Create a function that can intake integer or decimal value and do following operations:
a. Logarithmic function (log x)
b. Exponential function (exp(x))
c. Power function with base 2 (2
x
)
d. Square root


```python
# Python code to demonstrate the working of
# exp() and log()
 
# importing "math" for mathematical operations
import math
 
# returning the exp of 4
print ("The e**4 value is : ", end="")
print (math.exp(4))
 
# returning the log of 2,3
print ("The value of log 2 with base 3 is : ", end="")
print (math.log(2,3))
```

    The e**4 value is : 54.598150033144236
    The value of log 2 with base 3 is : 0.6309297535714574
    
9. Create a function that takes a full name as an argument and returns first name and last name.

```python
import re
 
def name(s):
  # Use regular expression to extract the first letter of each word
  initials = re.findall(r'\b\w', s)
   
  # Use regular expression to extract the last word
  last_name = s.split()[-1]
  # Combine the initials and last name with dots
  result = '.'.join(initials[:-1]).upper() + '.' + last_name.title()
 
  return result
 
#Driver code
s = "Rojalin Rout"
print(name(s))
```

    R.Rout
    
