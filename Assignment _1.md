 Assignment 1


 1.In the below elements which of them are values or an expression?eg:-values can be integer or string and expressions will be mathematical operators .
*,'hellow',-87.8,-,/,+,6

Ans:-There are total 4 operators and Expression.They are:
operator: *,-,/,+
Expression: 'hello',-87.8,6

 2.What is the difference between string and variable?
 
 Ans:-A variable is used to store of information, and a string is a type of information you would store in a variable . A string is a group of single character usually enclosed in Double quotes" ",
or single quotes' ' . 

3.Describe three different Data types ?

Ans:-There are three different Data types:
1.integer: we can use int data types to represent whole numbers(integral value)
2.float : We can use float data types to represent floating point values(decimal values)
3.complex : complex numbers is represented by complex class.It is specified as (real part)+(imaginary part)



```python
#Example for integer data type
int_num=105
print(int_num, type(int_num))

#Example for float data type
flo_num=12.40
print(flo_num, type(flo_num))

#Example for Complex data type
com_com=5+7j
print(com_com, type(com_com))


```

    105 <class 'int'>
    12.4 <class 'float'>
    (5+7j) <class 'complex'>

    
 4.What is an expression made up of ? What do all expression do?
    
Ans:-An expression is an combination of values,variables,operators,and call to functions. Expression 
need to be evaluated. If we ask python to print an expression,the interpreter evaluates the expression
and displays the result.



```python
4*5+20-40 # Is an expression,The python interpreter evaluates it to 0
```




    0


5.This assinment statements,like spam=10.What is the difference between an expression and a statement?

Ans:-An expression is a combination of values,and operators.When we type an expression at the prompt,
the interpreter evaluates it,which means that it finds the value of the expression.
eg:4*5+20-40 is an example of the statement

A statement is a unit if code that has an effect,like creating a variable or displaying a value.When
type a statement,the interpreter executes it,which means that it does whatever the statement says.In
general,statement do not have values.
eg:Variable declaration and assignments because they do not return a value



```python
#example:
4*5+20-40  # Is an Expression
courseName = 'Ineuron Fullstack Datascience' # Is a sattement
print("Hello World !")  # Is a Expression statement

```

    Hello World !
    
6.After running the following code, what does the variable bacon contain?
bacon = 22
bacon + 1

Ans:-The variable bacon is set to 22.The expression bacon + 1 does not reassign the value is bacon
(that would the case if the expression is like bacon = bacon + 1 instead of bacon + 1)



```python
#Example
bacon=22
bacon+1
print(bacon)
```

    22
    
7.What should the values of the following two terms be?
'spam'+'spamspam'
'spam'*3

Ans:-Both expressions evaluate to the string 'Spamspamspam'Where as the first expression follows string concatentation and the second expression follows string multiplication.


```python
print('spam'+'spamspam') #String concatentation
print('spam'*3) # String multiplication
```

    spamspamspam
    spamspamspam
    
8.why is eggs a valid variable name while 100 is invalid?

Ans:-As per python , variable names cannot being with a number.


```python
egg='Ineuron'
100='hello'
print(egg)
print(100)
```


      Cell In[7], line 2
        100='hello'
        ^
    SyntaxError: cannot assign to literal here. Maybe you meant '==' instead of '='?
    

9.What three function can be used to get the integer,floating-point number,or string version of a value?

Ans:-The int(),float(),and str() fuctions will evaluate to the integer, floating point number,string version of the value passed to them .

10.Why does this expression cause an error?how can you fix it?
'I have eaten' + 99 +  'burritos'.


Ans:-This cause of error is 99.Because 99 is not a string.99 must be typecasted to a string to fix this error.The correct way is:

input: 'I have eaten' + str(99) + 'burritos'.
output: 'I have eaten 99 burritos' .


