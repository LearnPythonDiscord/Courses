# 2020-21-2020 Class

## Classes

### What is a class

A class is a code template for creating objects. Objects have member variables and have behaviour associated with them. In python a class is created by the keyword class . An object is created using the constructor of the class (__init__ method). A class is pointless without things called methods and attributes which will be further discussed below.

### Attributes

The simplest way to say what an attribute is would be to show you it, so here it is:

```py
class Car:
    def __init__(self, wheels:int) -> None:
        self.wheels = wheels

mycar = Car(wheels=4)
print(mycar.wheels)
>>> 4
```

"Wheels" is now an attribute of the class "Car", an attribute is something you can reference throughout your code via your "self" usually defined on the __init__ (method called on object initialisation). There is a difference between instance attributes and class attributes. The simplest way to say this is that instance attributes are attributes assigned in the __init__ method whereas class attributes are defined outside of the constructor, it does get a bit more complex than this but for now that doesnt change anything for this.

### Methods

Methods are simply functions that belong to the class, so if you want to do something with the attributes of the class then you simply make a method so you can interact with the data, i will show an example of updating the amount of wheels a car has (a weird example im aware);

```py
class Car:
    def __init__(self, wheels:int) -> None:
        self.wheels = wheels # wheels is now an attribute of car
    def update_wheels(self, wheels) -> None:
        self.wheels = wheels # wheels is now updated with the new value

mycar = Car(wheels=4)
print(mycar.wheels)
>>> 4
mycar.update_wheels(5)
print(mycar.wheels)
>>> 5
```

tldr; a method allows you interact with attributes of a class

### Important notes

#### __init__

This is the feature you will see on pretty much every class in python, this is called the constructor. This is the first method called on the initialisation of the class, as the name suggests, it constructs the object.

### __repr__ and __str__

These methods are both called on the print() function, with __str__ being called first, __str__ is the informal representation of the object in string represenation and then __repr__ is the formal version

