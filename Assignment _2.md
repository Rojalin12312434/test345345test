 Assignment 2

1.What are the two values of the Boolean data type? How do you write them?

Ans: The Boolean data types has two values i.e True and False,Which are special versions of 1 and 0 
respectively and behave as such in arithmetic conyexts.It is written as True=1 and False=0 .

```python
#Eg:
    
a = True 
b = False
print(a)
print(b)
```
    True 
    False
    
2. What are the three different types of Boolean operators?

Ans: The three different types of Boolean operators are AND,OR,NOT.


3. Make a list of each Boolean operator's truth tables (i.e. every possible combination of Boolean values for the operator and what it evaluate ).

Ans: True and True is True.

True and False is False.
  
False and True is False.

False and False is False

True or True is True.

True or False is True.

False or True is True.

False or False is False.

not True is False.

not False is True.

True is 1 and False is 0

Truth Table for AND

A B Output

0 0 0 

0 1 0

1 0 0

1 1 1

Truth Table for OR

A B output

0 0 0

0 1 1

1 0 1

1 1 1

Truth Table for Not

A output

o 1

1 0


4. What are the values of the following expressions?

```python
print((5 > 4) and (3 == 5))
print(not (5 > 4))
print((5 > 4) or (3 == 5))
print(not ((5 > 4) or (3 == 5)))
print((True and True) and (True == False))
print((not False) or (not True))

```

    False
    False
    True
    False
    False
    True
    
5. What are the six comparison operators?

Ans: ==,!=,<,>,<=,and >=


6. How do you tell the difference between the equal to and assignment operators?Describe a condition and when you would use one.

Ans: == is the equal operator that compares two values and evaluates to a Boolean, while = is the assignment operator that stores a value in a variable.

```python
Eg:
    
# Equal To operator
if(10 == 20):
    print("True")
else:
    print("False")
    
 # Assignment operator
x=30
print("x=",x)
```

    False
    x= 30
    
7. Identify the three blocks in this code:

```python
spam = 0
if spam == 10:
    print('eggs')
if spam > 5:
    print('bacon')
else:
    print('ham')
    print('spam')
    print('spam')
```

    ham
    spam
    spam
    
8. Write code that prints Hello if 1 is stored in spam, prints Howdy if 2 is stored in spam, and prints Greetings! if anything else is stored in spam.

```python
if spam == 1:
    print("hello")
elif spam == 2:
    print('Howdy')
else:    
    print('Greeting!')
```

    Greeting!
    
9.If your programme is stuck in an endless loop, what keys you’ll press?

Ans: The key i will press ctrl+c.


10. How can you tell the difference between break and continue?

Ans:The statement will move the execution outside and just after a loop.The continue statement will
move the execution to the start of the loop.

```python
# Break statement
l = [1,2,3,4,5,6,7]
for i in l :
    if i == 4:
        break
    print(i) 
    
 # Continue statement
for i in l :
    if i == 4 :
        continue
    print(i)    
```

    1
    2
    3
    1
    2
    3
    5
    6
    7
    
11. In a for loop, what is the difference between range(10), range(0, 10), and range(0, 10, 1)?

Ans: They all do the some thing.The range(10) call ranges from 0 up to(but not including)10,
range(0,10) explicitly tells the loop to start at 0 ,and range(0,10,1) explicitly tells the loop to
increase the variable by 1 on each iteration.


12. Write a short program that prints the numbers 1 to 10 using a for loop. Then write an equivalent program that prints the numbers 1 to 10 using a while loop.


```python
print('-'*10,'Using For Loop','-'*10)
for i in range(1,11):
    print(i, end=" ")
print('\n')
print('-'*10,'Using While Loop','-'*10) 
i=1
while i<=10:
    print(i, end=" ")
    i+=1
```

    ---------- Using For Loop ----------
    1 2 3 4 5 6 7 8 9 10 
    
    ---------- Using While Loop ----------
    1 2 3 4 5 6 7 8 9 10 


13. If you had a function named bacon() inside a module named spam, how would you call it after importing spam?

Ans: This function can be called with spam.bacon() .