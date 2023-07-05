 Assignment 7

Q.1. Create two int type variables, apply addition, subtraction, division and multiplications
and store the results in variables. Then print the data in the following format by calling the
variables:

First variable is __ & second variable is __.
Addition: __ + __ = __
Subtraction: __ - __ = __
Multiplication: __ * __ = __
Division: __ / __ = __


```python
print("Enter first number: ")
num1 = int(input())
print("Enter second number: ")
num2 = int(input())
res = num1+num2
print("\nAddition Result = ", res)
res = num1-num2
print("Subtraction Result = ", res)
res = num1*num2
print("Multiplication Result = ",res)
res = num1/num2
print("Division Result = ", res)
```

    Enter first number: 
    7
    Enter second number: 
    4
    
    Addition Result =  11
    Subtraction Result =  3
    Multiplication Result =  28
    Division Result =  1.75
    
Q.2. What is the difference between the following operators:

(i) ‘/’ & ‘//’
(ii) ‘**’ & ‘^’

Ans:-In python,the single backslash(/) is the division operator that performs division between two numbers and returns the result mostly in float.
In python, the double-backslash(//) is a mathematical operator called the floor division operator. Floor division implies splitting and rounding down a number to its nearest whole integer-point value.



```python
# single slash
a = 10
b = 30
c = a/b
print(c)
```

    0.3333333333333333
    


```python
# Double slash

a = 4
b = 2
c = a//b
print(c)
```

    2
    
Q.3. List the logical operators.

Ans:-There are three logical operators:AND,OR,NOT.

Q.4. Explain right shift operator and left shift operator with examples.

Ans:-right shift:
Shifts the bits of the number to the right and fills 0 on voids left(fills 1 in the case of a negative number) as a result.Similar effect as of dividing the number with some power of two.

Example:
a = 10 = 0000 1010 (Binary)
a >> 1 = 0000 0101 = 5

left shift:
Shifts the bits of the number to the left and fills 0 on voids right as a result.Similar effect as of multiplying the number with some power of two.
Example:
a = 5 = 0000 0101 (Binary)
a <<1 = 0000 1010 = 10



```python
a = 10

# print bitwise right shift operator
print("a >> 1 =", a >> 1)
a = 5
#  print bitwise left shift operator
print("a << 1 =", a << 1)


```

    a >> 1 = 5
    a << 1 = 10
    
Q.5. Create a list containing int type data of length 15. Then write a code to check if 10 is
present in the list or not.


```python
len=[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15]
len[10]

```




    11




```python

```
