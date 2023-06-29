Assignment 6

Q.1. What are keywords in python? Using the keyword library, print all the python keywords.

Ans:-Keywords in python are reserved words that cannot be used as ordinary identifiers.They are used to define the syntax and structure of the python language.As of python 3.9,there are 35 keywords.


```python
import keyword
print(keyword.kwlist)
```

    ['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
    
Q.2. What are the rules to create variables in python?

Ans:-Rules for python variables:-
-> A variable name must start with a letter or the underscore character.
-> A variable name cannot start with a number.
-> A variable name can only contain alpha-numeric characters underscores(A-z,0-9,and_).
-> Variable names are case-sensitive(age,Age,AGE are three different variables).

Q.3. What are the standards and conventions followed for the nomenclature of variables in
python to improve code readability and maintainability?

Ans:-The standard naming conventions used in modern software development are as follows:pascal case,
camel case,snake case.
use a lowercase single letter,word or words.seperate words with underscores to improve readability.
Start each word with a capital letter.Do not seperate words with underscores.

Q.4. What will happen if a keyword is used as a variable name?

Ans:-Keywords define the language's syntax rules and structure, and they cannot be used as variable
names.Programmers generally choose names for their variables that are meaningful to the human readers
of the program to remember what the variable is used for.


```python
True = 12
print(True)
```


      Cell In[1], line 1
        True = 12
        ^
    SyntaxError: cannot assign to True
    

Q.5. For what purpose def keyword is used? 

Ans:The def keyword is used to create(or define) a function.

Q.6. What is the operation of this special character ‘\’?

Ans:-In python strings,the backslash'\' is a special character, also called the "escape" character.
It is used in representing certain whitespace characters:"\t" is a tab,"\n" is a newline,and "\r" is 
a carriage return.

Q.7. Give an example of the following conditions:
(i) Homogeneous list
(ii) Heterogeneous set
(iii) Homogeneous tuple

```python
# Homogeneous list:-
fruits = ["Apples","Bananas","Grapes"]
print(fruits)
```

    ['Apples', 'Bananas', 'Grapes']
    


```python
# Homogeneous set:-
color = {"Red","Green","Blue"}
print(color)
```

    {'Blue', 'Red', 'Green'}
    


```python
# Homogeneous tuple
fruits = ("Bananas","Grapes","apples")
print(fruits)
```

    ('Bananas', 'Grapes', 'apples')
    
Q.8. Explain the mutable and immutable data types with proper explanation & examples. 

Ans:-Mutable objects are those that allow you to change their value or data in place without affecting
the object's identity.In contrast, immutable objects don't allow this kind of operation.you'll just have the option of creating new objects of the same type with different values.
List,set,Dictionary are mutable.Tuples,Integers,Floating-point numbers,Booleans,strings are immutable.



```python
# Mutable
colors= ["Red","Blue","Green"]
print(colors)
```

    ['Red', 'Blue', 'Green']
    


```python
# Immutable
my_tuple = (1,2,3,4)
print(my_tuple)
```

    (1, 2, 3, 4)
    
Q.9. Write a code to create the given structure using only for loop.
     *
    ***
   *****
  *******
 *********

```python
n = 5
for i in range(n):
    for j in range(n-i-1):
        print(' ',end = ' ')
    for k in range(2*i+1):
        print('*',end=' ')
    print()    
```

            * 
          * * * 
        * * * * * 
      * * * * * * * 
    * * * * * * * * * 
    
Q.10. Write a code to create the given structure using while loop.
    |||||||||
     |||||||
      |||||
       |||
        |

```python
rows = int(input("Enter number of rows: "))

for i in range(rows, 1, -1):
    for space in range(0, rows-i):
        print(" ", end="")
    for j in range(i, 2*i-1):
        print("|", end="")
    for j in range(1, i-1):
        print("|", end="")
    print()    
```

    Enter number of rows: 6
    |||||||||
     |||||||
      |||||
       |||
        |
    


```python

```


```python

```
