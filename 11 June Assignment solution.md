1. What is a lambda function in Python, and how does it differ from a regular function?

Ans:-Lambda functions are similar to user-defined functions but without a name. They're commonly referred to as anonymous functions. Lambda functions are efficient whenever you want to create a function that will only contain simple expressions – that is, expressions that are usually a single line of a statement.

A lambda function is an anonymous function (i.e., defined without a name) that can take any number of arguments but, unlike normal functions, evaluates and returns only one expression.

2. Can a lambda function in Python have multiple arguments? If yes, how can you define and use
them?

Ans:-Yes,lambda function in Python have multiple arguments.
The lambda function can take many arguments but can return only one expression. Here the expression is nothing but the result returned by the lambda function. Lambda functions are syntactically restricted to return a single expression. You can use them as an anonymous function inside other functions.


```python
# I have list
# as input I want to feed a list = [1, 2, 3, 4....]
#I want compute square of every itemin the list
my_list_cal = lambda x: [i ** 2 for i in x]
print(my_list_cal([1, 2, 3, 4, 5]))
```

    [1, 4, 9, 16, 25]

    
3. How are lambda functions typically used in Python? Provide an example use case.

Ans:-Lambda functions are frequently used with higher-order functions, which take one or more functions as arguments or return one or more functions. Python exposes higher-order functions as built-in functions or in the standard library. Examples include map() , filter() ,sorted() functools.

```python
products = [{'name': 'phone','price': 10000},
           {'name': 'printer','price': 20000},
           {'name': 'Laptop','price': 40000},
           {'name': 'Headphone','price': 50000},]

sorted_products = sorted(products,key = lambda x: x['price'])

for products in sorted_products:
    print(products)
```

    {'name': 'phone', 'price': 10000}
    {'name': 'printer', 'price': 20000}
    {'name': 'Laptop', 'price': 40000}
    {'name': 'Headphone', 'price': 50000}
    
4. What are the advantages and limitations of lambda functions compared to regular functions in
Python?

Ans:-The main advantage is their concise and readable syntax, which makes them ideal for simple operations. However, lambda functions can only contain a single expression and cannot include statements, making them less suitable for complex operations.

5. Are lambda functions in Python able to access variables defined outside of their own scope?
Explain with an example.

Ans:-Lambda functions have their own local namespace and cannot access variables other than those in their parameter list and those in the global namespace.

```python
#Local variable

def average (a,b,c):
    
    d = (a + b + c ) / 3
    return d


result = average (10,20,30)

print (d)



```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[6], line 9
          4     return d
          7 result = average (10,20,30)
    ----> 9 print (d)
    

    NameError: name 'd' is not defined



```python
#Global variable
a = 10

def average (b,c):

    print ("a is", a)

    d = ( a + b + c ) / 3

    return d


print (average (20, 30) )

```

    a is 10
    20.0
    
6. Write a lambda function to calculate the square of a given number.


```python
square = lambda a: a ** 2
print(square(6))
 
```

    36
    
7. Create a lambda function to find the maximum value in a list of integers.


```python
max_num = lambda x,y: x if x > y else y
print(max_num(20, 14))
```

    20
    
8. Implement a lambda function to filter out all the even numbers from a list of integers.


```python
nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print("Original list of integers:")
print(nums)
print("\nEven numbers from the said list:")
even_nums = list(filter(lambda x: x%2 == 0, nums))
print(even_nums)
print("\nOdd numbers from the said list:")
odd_nums = list(filter(lambda x: x%2 != 0, nums))
print(odd_nums)

```

    Original list of integers:
    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    
    Even numbers from the said list:
    [2, 4, 6, 8, 10]
    
    Odd numbers from the said list:
    [1, 3, 5, 7, 9]

    
9. Write a lambda function to sort a list of strings in ascending order based on the length of each
string.


```python
# Python code to sort a list by creating
# another list Use of sorted()
def Sorting(lst):
    lst2 = sorted(lst, key=len)
    return lst2
     
# Driver code
lst = ["rashmi", "rozz", "sapna", "swati",
       "suraj", "sonali", "madhu"]
print(Sorting(lst))
```

    ['rozz', 'sapna', 'swati', 'suraj', 'madhu', 'rashmi', 'sonali']

    
10. Create a lambda function that takes two lists as input and returns a new list containing the
common elements between the two lists.

```python
# Python program to find the common elements
# in two lists
def common_member(a, b):
    a_set = set(a)
    b_set = set(b)
 
    if (a_set & b_set):
        print(a_set & b_set)
    else:
        print("No common elements")
          
  
a = [1, 2, 3, 4, 5]
b = [5, 6, 7, 8, 9]
common_member(a, b)
  
a = [1, 2, 3, 4, 5]
b = [6, 7, 8, 9]
common_member(a, b)
```

    {5}
    No common elements
    
11. Write a recursive function to calculate the factorial of a given positive integer.


```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)


num = 5
print("Factorial of", num, "is", factorial(num))
```

    Factorial of 5 is 120
    
12. Implement a recursive function to compute the nth Fibonacci number.


```python
# Function for nth Fibonacci number
 
def Fibonacci(n):
    if n<= 0:
        print("Incorrect input")
    # First Fibonacci number is 0
    elif n == 1:
        return 0
    # Second Fibonacci number is 1
    elif n == 2:
        return 1
    else:
        return Fibonacci(n-1)+Fibonacci(n-2)
 
# Driver Program
 
print(Fibonacci(10))
```

    34
    
13. Create a recursive function to find the sum of all the elements in a given list.

```python
def findSum(list1): 
     if len(list1)== 1: 
        return list1[0] 
     else: 
        return list1[0]+findSum(list1[1:]) 
  
# driver code 
list1 =[] 
# input values to list 
list1 = [1, 2, 3, 4, 5] 
print(findSum(list1))
```

    15
    
14. Write a recursive function to determine whether a given string is a palindrome.

```python
def is_palindrome(s):
    if len(s) < 1:
        return True
    else:
        if s[0] == s[-1]:
            return is_palindrome(s[1:-1])
        else:
            return False
a=str(input("Enter string:"))
if(is_palindrome(a)==True):
    print("String is a palindrome!")
else:
    print("String isn't a palindrome!")
```

    Enter string:1
    String is a palindrome!
    
15. Implement a recursive function to find the greatest common divisor (GCD) of two positive integers.

```python

# Recursive function to return gcd of a and b
def gcd(a, b):
 
    # Everything divides 0
    if (a == 0):
        return b
    if (b == 0):
        return a
 
    # base case
    if (a == b):
        return a
 
    # a is greater
    if (a > b):
        return gcd(a-b, b)
    return gcd(a, b-a)
 
# Driver program to test above function
a = 98
b = 56
if(gcd(a, b)):
    print('GCD of', a, 'and', b, 'is', gcd(a, b))
else:
    print('not found')
```

    GCD of 98 and 56 is 14
    


```python

```
