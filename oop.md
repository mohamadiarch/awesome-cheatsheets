* [Object Oriented Design Principles Cheat Sheet](https://senoritadeveloper.medium.com/object-oriented-design-principles-cheat-sheet-24e75a2289a1)
* [Object Oriented Design Principles Cheat Sheet - II](https://senoritadeveloper.medium.com/object-oriented-design-principles-cheat-sheet-ii-dfc2fdf6fb3e)
* [S O L I D Python](https://medium.com/nerd-for-tech/solid-principles-python-f09915698d85)

## OOP Concepts

* **Abstraction** (hide complexity — black box, show only essential details. interfaces, abstract classes)
* **Encapsulation** (private fields, public getter/setter. code update in one place)
* **Inheritance**
* **Polymorphism** (method overloading, method overriding)

### Cohesion & Coupling

* Cohesion = how related the functions within a single module are
* Coupling = interdependencies between modules

> High Cohesion, Low Coupling 👍🏻

### SOLID Principles

* **Single Responsibility**
* **Open-Closed Principle** (open for extension, closed for modification)
* **Liskov’s Substitution** (Rabbit extends Animal. classes should be substitutable)
* **Interface Segregation** (instead of a single interface, prefer multiple smaller interfaces)
* **Dependency Inversion** (Decoupling. depend on abstractions, interfaces)

> GOF ➤ interface > implementation, object decomposition > inheritance

### Design Patterns

Creational — Structural — Behavioral

*Creational*

* **Factory Method**
* **Abstract Factory** (factory of factories)
* **Builder** (complex objects using smaller objects)
* **Prototype** (cloning)
* **Singleton** (single instance)

*Structural*

* **Adapter** (incompatible interfaces)
* **Bridge** (decouple an abstraction from its implementation)
* **Composite** (a class that contains a group of its own objects)
* **Decorator** (wrapper / no modifications on an existing class, new functionality added)
* **Facade** (hides complexity)
* **Flyweight** (reduce the weight of object creation, create if needed or reuse)
* **Proxy** (a class represents the functionality of another class — create a proxy class having the original object)

*Behavioral*

* **Chain of Responsibility**
* **Command** (stock. buy returns Buy Stock, stock. sell returns Sell Stock — both using Stock class)
* **Interpreter** (language grammar, SQL parsing)
* **Iterator** (.next)
* **Mediator** (communication between different classes)
* **Memento** (restores to a previous state)
* **Observer** (register, notify)
* **State** (status, context)
* **Null Object** (for do-nothing relationship, instead of returning null value)
* **Strategy** (a class behavior or its algorithm can change at runtime)
* **Template** (abstract class, method flow)
* **Visitor** (execution algorithm of the element can vary as and when visitor varies)
* **MVC**

### KISS (Keep It Simple, Stupid)

Keep it simple, avoid complexities => clear to understand, easy to debug, easy to maintain

### DRY (Don’t Repeat Yourself) — DIE (Duplication is Evil)

Avoid duplication — Consider modularizing functionality that you use more than once

* If you have a repeated piece of code, move inside a new function
* If you have a function that you’ve defined in several places, then move it into a common module.
* If the same applies to your module, consider turning it into a common library.

### YAGNI (You Aren’t Gonna Need It)

Avoid over-engineering (code bloat) and implement only necessary requirements.

### Curly’s Law — Do One Thing

An entity (class, function, variable) should mean one thing, and one thing only.

### Law of Demeter — Don’t talk to strangers

Avoid coupling.

A method of an object may only call methods of:

* The object itself.
* An argument of the method.
* Any object created within the method.
* Any direct properties/fields of the object.

### Inversion of Control — Hollywood Principle, “Don’t call us, we’ll call you”

Can achieve by using:

* *Factory Pattern*
* *Service Locator Pattern:* Instead of instantiating the dependent class itself, it gets an implementation from the service locator.
Some argue that it is an anti-pattern that obscures dependencies and makes software harder to test.
* *Dependency Injection:* To understand Dependency Injection, firstly I should give some details about IoC (Inversion of Control):
Inversion of Control — is to provide any kind of callback, instead of acting ourselves directly. It enables the creation of dependent objects to be inverted. It helps design testable, maintainable, and extensible loosely coupled classes.
Using IoC, you are not sewing up your objects. IoC containers (DI frameworks) will do that and manage their lifetime of them.
Dependency Injection — is a more specific version of the IoC pattern, where implementations are passed into an object through constructors/setters/service lookups, which the object will ‘depend’ on in order to behave correctly.
* *Template Method Pattern* It is a kind of IoC without using DI.
* *Strategy Pattern*

### Boy-Scout Rule

Refactoring (Uncle Bob) — always leave the code behind in a better state than you found it to avoid technical debt

### Linus’s Law

*Given enough eyeballs, all bugs are shallow.* — recommends a software reviewing process where multiple developers inspect the piece of code before it’s accepted and merged.

### Brooks’s Law

Adding manpower to a late software project makes it later.

## OOP Questions

![class-object](https://i.ibb.co/FwFGHVy/image.png)

### What is OOP?

OOP refers to object-oriented programming. It is the programming paradigms that is defined using objects. Objects can be considered as real-world instances of entities like class, that have some characteristics and behaviors.

Developed in 1960's ==> Simula language + smaltalk

### What is the need of OOP?

There are many reasons why OOP is preferred, but the most important among them are:

* OOP helps the user to understand the Software easily, even they don’t know about implementation.
* With OOP the readability, maintainability & understandability of the code is increase multifold.
* Very large software can be easily written & managed by using OOP.


### What are some advantages of using OOP?

* OOP is very helpful in solving very complex level of problems.
* OOP promotes code reuse, thereby reducing redundancy.
* Highly complex programs can be created, maintained, and handled easily using OOP.
* It also helps to hide unnecessary details with the help of data abstraction.
* Polymorphism offers a lot of flexibility in OOP.
* OOP is based on a bottom-up approach, unlike the structured programming paradigms, which are based on a top-down approach.

### What are the four design principles in OOP?

OOP or Object-Oriented Programming mainly comprises of the below four principles & make sure you don’t miss any of these.

* Inheritance
* Encapsulation
* Polymorphism
* Data Abstraction

### Encapsulation

![Encapsulation](https://i.ibb.co/JB6HF7T/image.png)

Encapsulation is the mechanism of wrapping the instance variables and methods together as a single unit like a class & exposing the selected information to the outside world.Exp: diffrenet section of company: finance,sales and managemnet

Encapsulation can also be defined in two different ways:

* **Data hiding:** Encapsulation is the process of hiding unwanted information, such as restricting access to any member of an object.
* **Data binding:** Encapsulation is the process of binding the properties and the methods together as a single unit.

### Inheritance

The term “inheritance” means “receiving some quality or behavior from a parent to an offspring.” In object-oriented programming, inheritance is the mechanism by which a class (referred to as a child) is created using the definition of another class (referred to as a parent). Inheritance not only helps to keep the implementation simpler but also helps to facilitate code reuse.

![types-of-inheritance](https://i.ibb.co/SyJ0K2t/image.png)

The various types of inheritance include:

* Single inheritance
* Multiple inheritances ==> java does not have this
* Multi-level inheritance
* Hierarchical inheritance
* Hybrid inheritance

### Abstraction

If you are a user, and you have a problem statement, you don't want to know how the components of the software work(details), or how it's made. You only want to know how the software solves your problem. *Abstraction is a process of hiding the implementation details from the user and only providing functionality(essential information) to the user*. It is one of the main features of OOP.

For example, consider a car. You only need to know how to run a car, and not how the wires are connected inside it. This is obtained using Abstraction

### Polymorphism

Polymorphism is composed of two words - “poly” means “many”, and “morph” means “shapes”. Therefore Polymorphism refers to something that has many shapes. exp: Calculate Area, Same function but different in implementation.
In programming, polymorphism means the same function name (but different signatures)

```py
# Polymorphism in programming language

def add(x, y, z = 0): 
	return x + y+z

# Driver code 
print(add(2, 3))
print(add(2, 3, 4))
```

![polymorphism](https://i.ibb.co/PcSfTGd/Untitled.png)

In OOP, Polymorphism refers to the process by which some code, data, method, or object behaves differently under different circumstances. Compile-time polymorphism and Run time polymorphism are the two types of polymorphisms in OOP languages.


### Abstract class

An abstract class is a special class containing abstract methods. The significance of an abstract class is that the abstract methods inside it are not implemented and only declared. So as a result, when a subclass inherits the abstract class and needs to use its abstract methods, they only need to define and implement them.

```python
from abc import ABC, abstractmethod

class AbstractClass(ABC):
    def __init__(self):
        pass

    # Methods with '@abstractmethod' decorators
    # must be defined in the child class.
    @abstractmethod
    def run(self):
        pass

    def walk(self):
        pass

class SubClass(AbstractClass):
    def run(self):
        return 'They are running`
```

### Interface

Interface refers to a special type of class, which contains methods, but not their definition. Only the declaration of methods is allowed inside an interface. To use an interface, you cannot create objects. Instead, you need to implement that interface and define the methods for their implementation.

### Difference between abstract class and interface

Interface and abstract classes both are special types of classes that contain only the methods declaration and not their implementation. But the interface is entirely different from an abstract class. The main difference between the two is that, when an interface is implemented, the subclass must define all its methods and provide its implementation. Whereas when an abstract class is inherited, the subclass does not need to provide the definition of its abstract method, until and unless the subclass is using it.

Also, an abstract class can contain abstract methods as well as non-abstract methods.

* [Difference between abstract class and interface](https://www.javatpoint.com/difference-between-abstract-class-and-interface)

### What is runtime and compile time polymorphism

![polymorphism-types](https://i.ibb.co/0rRy5zz/image.png)

* **Compile Time Polymorphism:** Compile time polymorphism, also known as Static Polymorphism, refers to the type of Polymorphism that happens at compile time. What it means is that the compiler decides what shape or value has to be taken by the entity in the picture.
* **Runtime Polymorphism:** Runtime polymorphism, also known as Dynamic Polymorphism, refers to the type of Polymorphism that happens at the run time. What it means is it can't be decided by the compiler. Therefore what shape or value has to be taken depends upon the execution. Hence the name Runtime Polymorphism.

* [Difference between Compile-time and Run-time Polymorphism in Java](https://www.geeksforgeeks.org/difference-between-compile-time-and-run-time-polymorphism-in-java)

### What is a class?

A class can be understood as a template or blueprint. Which contains some values known as data and some set of rules, known as behaviors or functions. So when an object is created, it automatically takes the data and functions that are defined in class. 

### What is an object?

An object is an identifiable entity with some characteristics & behaviors. An object is an instance of a class. When a class is defined, no memory is allocated, but when it is instantiated (object is created) memory is allocated.

Class: design, blueprint
Object: instance


```python 
class Person:
    def __init__(self, name, id):
        self.name = name
        self.id = id

    def __repr__(self):
        return f'Name {} and Id {}'

p = Person() # p is holding object-reference
```

### What is a constructor?

The Constructor is a method that is called when an object is created. This method is defined in the class & can be used to initialize basic variables. If you create four objects, then the class constructor is called four times. Every class has constructor but its not required to explicitly define it.

### What is a destructor?

Contrary to constructors, which initialize objects and specify space for them, Destructors are also special methods. But destructors free up the resources and memory occupied by an object. Destructors are automatically called when an object is being destroyed.

### What is a subclass?

The subclass is a part of Inheritance. The subclass is an entity, which inherits from another class. It is also known as the child class.

### What is superclass?

Superclass is also a part of Inheritance. The superclass is an entity, which allows subclasses or child classes to inherit from itself.

### What is the difference between overloading and overriding?

Overloading is a compile-time polymorphism feature in which an entity has multiple implementations with the same name. For example, Method overloading and Operator overloading.

```python 
# Method Overloading
# Overloading refers to making a method perform
# different operations based on the nature of its arguments.

class Employee:
    def __init__(self):
        pass

    def run(self, person):
        pass

    def run(self, person, street):
        pass

E = Employee()
E.run('p', '221b')

# python doesn't support method overloading. If we
# define 2 methods with the same name, the most recent
# method will be considered rest of the methods are ignored.
```

![overloading-advantages](https://i.ibb.co/717WHqy/image.png)

Whereas Overriding is a runtime polymorphism feature in which an entity has the same name, but its implementation changes during execution. For example, Method overriding.

```python 
# Method Overriding
# Method overriding is the process of redefining a
# parent class’s method in a subclass.

class Shape:
    def __init__(self):
        self.shapes = 0

    # overridden method
    def get_area(self):
        pass

    class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.length = length

    # overriding method
    def get_area(self):
        return self.width * self.length
```

![overloading](https://i.ibb.co/gPRHFZy/image.png)

## Pythonic Object

> Attributes → (Properties and Methods)

### Variables/Properties can be defined into two parts

* **Class Variables**
    * The Class variables are shared by all instances or objects of the classes. A change in the class variable will change the value of that property in *all the objects* of the class.
* **Instance Variables**
    * The instance variables are unique to each instance or object of the class. A change in the instance variable will change the value of that property in that *specific object only*.

Class variables are defined *outside* the initializer and instance variables are defined *inside* the initializer.

### 3 types of methods are available in python

A *method* is a group of statements that perform some operations and may or may not return a result.

* **Instance methods**
    - usuall methods
* **Class methods**
    - Class methods work with class variables and are accessible using the class name rather than its object. Since all class objects share the class variables, class methods are used to access and modify class variables.
    - Class methods are accessed using the class name and can be accessed without creating a class object.
    - Class methods can be alternative construcotr .
    - python doesn’t support method overloading like C++ or Java so we use class methods to create factory methods.
* **Static methods**
    - Static methods are methods that are usually limited to class only and not their objects. They have no direct relation to class variables or instance variables. They are used as utility functions inside the class or when we do not want the inherited classes to modify a method definition.
    - Static methods can be accessed using the class name or the object name.

### Access Modifiers

* **Public attributes** are those that can be accessed inside the class and outside the class.
    - Methods & properties are public by default
* **Private attributes** cannot be accessed directly from outside the class but can be accessed from inside the class.
    - We can make members private using the double underscore `__` prefix
    - Access private attributes/methods in main code `objectName._ClassName__property/method`
* **Protected attributes** are those members of the class that cannot be accessed outside the class but can be accessed from within the class and its subclasses.
    - We can make members protected by using single underscore `-` prefix.


### Static Variables 

* **Advantages**:
    - **Memory efficiency**: Since static variables are shared among all instances of a class, they can save memory by avoiding the need to create multiple copies of the same data.
    - **Shared state**: Static variables can provide a way to maintain shared state across all instances of a class, allowing all instances to access and modify the same data.
    - **Easy to access**: Static variables can be accessed using the class name itself, without needing an instance of the class. This can make it more convenient to access and modify the data stored in a static variable.
    - **Initialization**: Static variables can be initialized when the class is defined, making it easy to ensure that the variable has a valid starting value.
    - **Readability**: Static variables can improve the readability of the code, as they clearly indicate that the data stored in the variable is shared among all instances of the class.


* **Disadvantages**:
    - **Inflexibility**: Static variables can be inflexible, as their values are shared across all instances of the class, making it difficult to have different values for different instances.
    - **Hidden dependencies**: Static variables can create hidden dependencies between different parts of the code, making it difficult to understand and modify the code.
    - **Thread safety**: Static variables can be problematic in a multithreaded environment, as they can introduce race conditions and synchronization issues if not properly synchronized.
    - **Namespace pollution**: Static variables can add to the namespace of the class, potentially causing name conflicts and making it harder to maintain the code.
    - **Testing**: Static variables can make it more difficult to write effective unit tests, as the state of the static variable may affect the behavior of the class and its methods.

### Data hiding can be divided into two primary components:

* Encapsulation
* Abstraction

### Getters and Setters

* A *getter* method allows reading a property’s value.
* A *setter* method allows modifying a property’s value.

> Note: For encapsulating a class, all the properties should be private and any access to the properties should be through methods such as getters and setters.

### Inheritance

Wherever we come across an *IS A* relationship between objects, we can use inheritance.

* Square *IS A* shape
* Python *IS A* programming language
* Car *IS A* vehicle

In inheritance, in order to create a new class based on an existing class, we use the following terminology:

* **Parent Class (Super Class or Base Class):** This class allows the *reuse* of its *public* properties in another class.
* **Child Class (Sub Class or Derived Class):** This class *inherits* or *extends* the superclass.

The use of `super()` comes into play when we implement inheritance. It is used in a child class to **refer** to the parent class without explicitly naming it. It makes the code more manageable, and there is no need to know the name of the parent class to access its attributes.

**Use cases of the `super()` function**

* Accessing parent class properties → `super().classVariable`
* Calling the parent class methods → `super().walk()`
* Using initializers
    - Another essential use of the function `super()` is to call the initializer of the parent class from inside the initializer of the child class.

### Types of Inheritance

Based upon parent classes and child classes, there exists the following *five* types of inheritance:

* **Single Inheritance**
    - In single inheritance, there is only a single class extending from another class.
    - Examples
        - A Car *IS A* Vehicle.
    - ![single-inheritance](https://i.ibb.co/g31FMqJ/image.png)
* **Multi-level Inheritance**
    - When a class is derived from a class that itself is derived from another class, it is called multilevel inheritance. We can extend the classes to as many levels as we want to.
    - Examples
        - A Car *IS A* Vehicle.
        - A Hybrid *IS A* Car.
    - ![multi-level](https://i.ibb.co/kDmBdtn/Untitled.png)
* **Multiple Inheritance**
    - When a class is derived from more than one base class, i.e., when a class has more than one immediate parent class, it is called multiple inheritance.
    - Examples
        - HybridEngine *IS A* ElectricEngine.
        - HybridEngine *IS A* CombustionEngine as well.
    - ![multiple-inheritance](https://i.ibb.co/JnypyyY/image.png)
* **Hybrid Inheritance**
    * A type of inheritance that is a combination of *Multiple* and *Multi-level* inheritance is called hybrid inheritance.
    * Examples
        * CombustionEngine *IS A* Engine.
        * ElectricEngine *IS A* Engine.
        * HybridEngine *IS A* ElectricEngine and a CombustionEngine.
    * ![hybrid](https://i.ibb.co/P1YCFjN/image.png)
* **Hierarchical Inheritance**
    * In hierarchical inheritance, more than one class extends, as per the requirement of the design, from the same base class. The common attributes of these child classes are implemented inside the base class.
    * Examples
        - A Car *IS A* Vehicle
        - A Truck *IS A* Vehicle
    * ![Hierarchical](https://i.ibb.co/jDNTMnq/image.png)

### Polymorphism

The word *Polymorphism* is a combination of two Greek words, *Poly* meaning *many* and *Morph* meaning *forms*. In programming, *polymorphism* refers to the same object exhibiting different forms and behaviors.

**Method Overriding**

> Method overriding is the process of redefining a parent class’s method in a subclass.

In this case:

* The method in the parent class is called the **overridden method.**
* The methods in the child classes are called the **overriding methods.**

**Advantages and key features of method overriding**

* The derived classes can give their own specific implementations to inherited methods without modifying the parent class methods.
* For any method, a child class can use the implementation in the parent class or make its own implementation.
* Method overriding needs inheritance, and there should be at least one derived class to implement it.
* The methods in the derived classes usually have dissimilar implementations.

**Operator Overloading**

When a class is defined, its objects can interact with each other through the operators, *but* it is necessary to define the behavior of these operators through operator overloading.

**Implementing Polymorphism Using Duck Typing**

If an object *quacks* like a duck, *swims* like a duck, *eats* like a duck, or in short, *acts* like a duck, that object is a duck.

> Dynamic typing means that we can change the type of an object later in the code

```python 
# Example of dynamic typing
x = 5
print(type(x).__name__) # int

x = 'Imran'
print(type(x).__name__) # str
```

Implementing duck typing/Polymorphism without inheritance.

```python 
class Dog:
    def speak(self):
        return 'woof woof'

class Cat:
    def speak(self):
        return 'Meow Meow'

class AnimalSound:
    def sound(self, animal):
        return animal.speak()

d = Dog()
c = Cat()
a = AnimalSound()
print(a.sound(d)) # 'Woof Woof'
print(a.sound(c)) # 'Meow Meow'
```

### Abstract Base Class

**Abstract base classes** define a set of methods and properties that a class must implement in order to be considered a duck-type instance of that class.

### Relationships between classes

* **Part-of/Nested Class**
    * In this relationship, one class object is a **component** of another class object. Given two classes, *class A* and *class B*, they are in a **part-of** relation if a *class A* object is a *part of* *class B* object, or vice-versa.
    * ![example](https://i.ibb.co/K7rvWmL/image.png)
* **IS A/Inheritance**
* **Has-a**
    * This is a slightly less concrete relationship between two classes. *Class A* and *class B* have a **has-a** relationship if one or both need the other’s object to perform an operation, but both class objects can exist independently of each other.
    * This implies that a class **has a** reference to an object of the other class but does not decide the lifetime of the other class’s referenced object.
    * ![example](https://i.ibb.co/pK5GPtq/image.png)

### Aggregation

**Aggregation** follows the *Has-A* model. This creates a parent-child relationship between two classes, with one class owning the object of another.

So, what makes aggregation unique?

> In aggregation, the lifetime of the owned object does not depend on the lifetime of the owner.

In aggregation, the parent only contains a *reference* to the child, which removes the child’s dependency.

```python 
class Country:
    def __init__(self, name=None, population=0):
        self.name = name
        self.population = population

    def printDetails(self):
        print("Country Name:", self.name)
        print("Country Population", self.population)


class Person:
    def __init__(self, name, country):
        self.name = name
        self.country = country

    def printDetails(self):
        print("Person Name:", self.name)
        self.country.printDetails()


c = Country("Wales", 1500)
p = Person("Joe", c)
p.printDetails() # 

# deletes the object p
del p
print('')
c.printDetails() # Parent Class
```

### Composition

**Composition** is the practice of accessing other class objects in your class. In such a scenario, the class which creates the object of the other class is known as the *owner* and is responsible for the lifetime of that object.

Composition relationships are *Part-of* relationships where the *part* must constitute a segment of the whole object. We can achieve composition by adding smaller parts of other classes to make a complex unit.

But what makes composition so unique?

> In composition, the lifetime of the owned object depends on the lifetime of the owner.

```python 
class Engine:
    def __init__(self, capacity=0):
        self.capacity = capacity

    def printDetails(self):
        print("Engine Details:", self.capacity)


class Tires:
    def __init__(self, tires=0):
        self.tires = tires

    def printDetails(self):
        print("Number of tires:", self.tires)


class Doors:
    def __init__(self, doors=0):
        self.doors = doors

    def printDetails(self):
        print("Number of doors:", self.doors)


class Car:
    def __init__(self, eng, tr, dr, color):
        self.eObj = Engine(eng)
        self.tObj = Tires(tr)
        self.dObj = Doors(dr)
        self.color = color

    def printDetails(self):
        self.eObj.printDetails()
        self.tObj.printDetails()
        self.dObj.printDetails()
        print("Car color:", self.color)


car = Car(1600, 4, 2, "Grey")
car.printDetails()
```
ref =imrand-dev/oop-theory.md
ref =https://gist.github.com/imrand-dev/d62e3dbda1b3533a24b4de576cc7e5ef
