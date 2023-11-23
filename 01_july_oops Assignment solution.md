1. What is the primary goal of Object-Oriented Programming (OOP)?

Ans:-It aims to implement real-world entities like inheritance, polymorphisms, encapsulation, etc. in the programming. The main concept of OOPs is to bind the data and the functions that work on that together as a single unit so that no other part of the code can access this data.

2. What is an object in Python?

Ans:-An Object is an instance of a Class. A class is like a blueprint while an instance is a copy of the class with actual values. Python is an object-oriented programming language that stresses objects i.e. it mainly emphasizes functions.

3. What is a class in Python?
Ans:-A class is a user-defined blueprint or prototype from which objects are created. Classes provide a means of bundling data and functionality together. Creating a new class creates a new type of object, allowing new instances of that type to be made.

4. What are attributes and methods in a class?

Ans:-Attributes are variables that belong to an object and contain information about its properties and characteristics. They can be used to represent details or facts related to the object. Methods are functions belonging to an object and are designed to perform actions or operations involving the object's attributes. Methods are defined as part of the class the object belongs to and are executed using instances of that particular class.


```python
# Ex of attributes and methods
class Cat:
 
    # Attributes
    name = 'Mittens'
    color = 'black'

    # Methods
    def meow(self):
        print('Meow!')

# Create an instance of the Cat class
my_cat = Cat()

# Access the attributes of the instance
print(my_cat.name)
print(my_cat.color)

# Call the meow() method
my_cat.meow()
```

    Mittens
    black
    Meow!
    
5. What is the difference between class variables and instance variables in Python?

Ans:-class variable-
Class variables are those variables that are defined within a class and before the class constructor i,e, __init__ method. Because class variables are shared by all instances of the class and owned by the class itself. Class variables are typically placed below the class name and outside of instance methods.

Instance variable:-
Instance variables are declared inside the constructor method of the class i.e the __init__ method. Every object has its own value in an instance variable


```python
# Eg of class variable:-
class Shark:
    animal_type = "fish"
    location = "ocean"
    followers = 5

new_shark = Shark()
print(new_shark.animal_type)
print(new_shark.location)
print(new_shark.followers)
```

    fish
    ocean
    5
    


```python
# Eg of Instance variable-
class Person:
    def __init__(self, name, age):
        self.name = name          #Instance Variable
        self.age = age            #Instance Variable
new_person = Person("Rojalin", 20)
print(new_person.name)
print(new_person.age)

```

    Rojalin
    20
    
6. What is the purpose of the self parameter in Python class methods?

Ans:-The self parameter is a reference to the current instance of the class, and is used to access variables that belongs to the class.

7. For a library management system, you have to design the "Book" class with OOP
principles in mind. The “Book” class will have following attributes:
a. title: Represents the title of the book.
b. author: Represents the author(s) of the book.
c. isbn: Represents the ISBN (International Standard Book Number) of the book.
d. publication_year: Represents the year of publication of the book.
e. available_copies: Represents the number of copies available for checkout.
The class will also include the following methods:
a. check_out(self): Decrements the available copies by one if there are copies
available for checkout.
b. return_book(self): Increments the available copies by one when a book is
returned.
c. display_book_info(self): Displays the information about the book, including its
attributes and the number of available copies.


```python
class Book:
    def __init__(self,author,isbn,publication_year,available_copies):
        self.author=author
        self.isbn=isbn
        self.publication_year=publication_year
        self.available_copies=available_copies
    def __str__(self):
        return f"Increments the available copies by one when a book is returned"
```


```python
book=Book("K.K Sharma",97893272,"2002",100)
print(book)
```

    Increments the available copies by one when a book is returned
    
8. For a ticket booking system, you have to design the "Ticket" class with OOP
principles in mind. The “Ticket” class should have the following attributes:
a. ticket_id: Represents the unique identifier for the ticket.
b. event_name: Represents the name of the event.
c. event_date: Represents the date of the event.
d. venue: Represents the venue of the event.
e. seat_number: Represents the seat number associated with the ticket.
f. price: Represents the price of the ticket.
g. is_reserved: Represents the reservation status of the ticket.
The class also includes the following methods:
a. reserve_ticket(self): Marks the ticket as reserved if it is not already reserved.
b. cancel_reservation(self): Cancels the reservation of the ticket if it is already
reserved.
c. display_ticket_info(self): Displays the information about the ticket, including its
attributes and reservation status.


```python
class Ticket:
    def __init__(self,ticket_id,event_name,event_date,venue,seat_number,price,):
        self.ticket_id=ticket_id
        self.event_name=event_name
        self.event_date=event_date
        self.venue=venue
        self.seat_number=seat_number
        self.price=price
    def __str__(self):
        return f"Displays the information about the ticket, including itsattributes and reservation status"
```


```python
ticket=Ticket("180","Glamour Party","06-12-2023","Palm Garden",10,250,)
print(ticket)
```

    Displays the information about the ticket, including itsattributes and reservation status
    
9. Imagine a school management system. You have to design the "Student" class using
OOP concepts.The “Student” class has the following attributes:
a. name: Represents the name of the student.
b. age: Represents the age of the student.
c. grade: Represents the grade or class of the student.
d. student_id: Represents the unique identifier for the student.
e. attendance: Represents the attendance record of the student.
The class should also include the following methods:
a. update_attendance(self, date, status): Updates the attendance record of the
student for a given date with the provided status (e.g., present or absent).
b. get_attendance(self): Returns the attendance record of the student.
c. get_average_attendance(self): Calculates and returns the average
attendance percentage of the student based on their attendance record.

```python
class Student:
    def __init__(self,name,age,grade,student_id,attendance):
        self.name=name
        self.age=age
        self.grade=grade
        self.student_id=student_id
        self.attendance=attendance
        
    def get_attendance(self):
        print(f"The {self.name} {self.age} {self.grade} {self.student_id} {self.attendance}")
       
```


```python
student1=Student("Rojalin",24,"A",108,45)
```


```python
student1.grade
```




    'A'


