
# **Unit 3: Inheritance, Polymorphism, Abstract Classes, and Interfaces**

## **1. Inheritance**

Inheritance is a fundamental concept in object-oriented programming that allows a new class (subclass or child class) to acquire properties and behaviors from an existing class (superclass or parent class). This promotes code reusability and establishes a hierarchical relationship between classes.

### **Syntax:**

```java
class Superclass {
    // Superclass members
}

class Subclass extends Superclass {
    // Additional members of Subclass
}
```

### **Example:**

```java
// Superclass
class Vehicle {
    String brand = "Ford";

    void honk() {
        System.out.println("Beep! Beep!");
    }
}

// Subclass
class Car extends Vehicle {
    String model = "Mustang";

    void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car();
        myCar.display();
        myCar.honk(); // Inherited method
    }
}
```

**Output:**

```
Brand: Ford
Model: Mustang
Beep! Beep!
```

In this example, `Car` inherits properties and methods from `Vehicle`.

<!-- types of inheritance in java -->
## **Types of Inheritance in Java**

There are two main types of inheritance:

- **Single Inheritance:** A class can inherit properties and methods from a single parent class.
- **Multiple Inheritance using interfaces:** A class can inherit properties and methods from more than one parent class.
- **Multilevel Inheritance:** A class can inherit properties and methods from a parent class, which in turn inherits from another parent class.
- **Hierarchical Inheritance:** Several classes can inherit from a single parent class.
- **Interface Inheritance:** A class can inherit properties and methods from an interface.

**Example of Multiple Inheritance using Interfaces:**

```java
// Java program to illustrate the
// concept of Multiple inheritance
import java.io.*;
import java.lang.*;
import java.util.*;

interface One {
    public void print_geek();
}

interface Two {
    public void print_for();
}

interface Three extends One, Two {
    public void print_geek();
}
class Child implements Three {
    @Override public void print_geek()
    {
        System.out.println("Geeks");
    }

    public void print_for() { System.out.println("for"); }
}

// Drived class
public class Main {
    public static void main(String[] args)
    {
        Child c = new Child();
        c.print_geek();
        c.print_for();
        c.print_geek();
    }
}
```
**Example of Hierarchical Inheritance:**

```java
// Java program to illustrate the
// concept of Hierarchical  inheritance

class A {
    public void print_A() { System.out.println("Class A"); }
}

class B extends A {
    public void print_B() { System.out.println("Class B"); }
}

class C extends A {
    public void print_C() { System.out.println("Class C"); }
}

class D extends A {
    public void print_D() { System.out.println("Class D"); }
}

// Driver Class
public class Test {
    public static void main(String[] args)
    {
        B obj_B = new B();
        obj_B.print_A();
        obj_B.print_B();

        C obj_C = new C();
        obj_C.print_A();
        obj_C.print_C();

        D obj_D = new D();
        obj_D.print_A();
        obj_D.print_D();
    }
}

```
**Example of Multilevel Inheritance:**

```java
// Importing required libraries
import java.io.*;
import java.lang.*;
import java.util.*;

// Parent class One
class One {
    // Method to print "Geeks"
    public void print_geek() {
        System.out.println("Geeks");
    }
}

// Child class Two inherits from class One
class Two extends One {
    // Method to print "for"
    public void print_for() {
        System.out.println("for");
    }
}

// Child class Three inherits from class Two
class Three extends Two {
    // Method to print "Geeks"
    public void print_lastgeek() {
        System.out.println("Geeks");
    }
}

// Driver class
public class Main {
    public static void main(String[] args) {
        // Creating an object of class Three
        Three g = new Three();
        
        // Calling method from class One
        g.print_geek();
        
        // Calling method from class Two
        g.print_for();
        
        // Calling method from class Three
        g.print_lastgeek();
    }
}
```



## **2. Polymorphism**

Polymorphism allows methods or objects to take on multiple forms. In Java, it is primarily achieved through method overriding and interfaces.

### **Method Overriding:**

When a subclass provides a specific implementation for a method already defined in its superclass.

**Example:**

```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Dog();
        myAnimal.sound(); // Outputs: Dog barks
    }
}
```

Here, the `sound()` method is overridden in the `Dog` class. When called on an `Animal` reference pointing to a `Dog` object, the overridden method is executed.

## **3. Abstract Classes**

An abstract class cannot be instantiated and may contain abstract methods (methods without a body) that must be implemented by subclasses.

### **Syntax:**

```java
abstract class Animal {
    abstract void sound();

    void sleep() {
        System.out.println("Sleeping...");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.sound();
        myDog.sleep();
    }
}
```

**Output:**

```
Dog barks
Sleeping...
```

In this example, `Animal` is an abstract class with an abstract method `sound()`. The `Dog` class extends `Animal` and provides an implementation for `sound()`.

## **4. Interfaces**

An interface is a reference type in Java, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types. Interfaces cannot contain instance fields or constructors. A class can implement multiple interfaces, providing a way to achieve multiple inheritance in Java.

### **Syntax:**

```java
interface Animal {
    void sound();
}

class Dog implements Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.sound();
    }
}
```

**Output:**

```
Dog barks
```

In this example, `Animal` is an interface with a method `sound()`. The `Dog` class implements the `Animal` interface and provides an implementation for `sound()`.

### **Multiple Interfaces:**

```java
interface CanRun {
    void run();
}

interface CanBark {
    void bark();
}

class Dog implements CanRun, CanBark {
    @Override
    public void run() {
        System.out.println("Dog is running");
    }

    @Override
    public void bark() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.run();
        myDog.bark();
    }
}
```

**Output:**

```
Dog is running
Dog barks
```

Here, `Dog` implements two interfaces: `CanRun` and `CanBark`, demonstrating multiple inheritance through interfaces.

## **5. Differences Between Abstract Classes and Interfaces**

| Feature             | Abstract Class                                                                 | Interface                                                                 |
|---------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| **Instantiation**   | Cannot be instantiated                                                         | Cannot be instantiated                                                    |
| **Methods**         | Can have both abstract and concrete methods                                    | Can have abstract methods; from Java 8, can have default and static methods |
| **Fields**          | Can have instance variables                                                    | Can only have static final variables                                      |
| **Inheritance**     | A class can extend only one abstract class                                     | A class can implement multiple interfaces                                 |
| **Constructors**    | Can have constructors                                                          | Cannot have constructors                                                  |

**Reference:** [Difference between Abstract Class and Interface in Java](https://www.geeksforgeeks.org/difference-between-abstract-class-and-interface-in-java/)

## **Conclusion**

- **Inheritance** allows classes to inherit properties and methods from other classes, promoting code reusability.
- **Polymorphism** enables methods or objects to take on multiple forms, enhancing flexibility in code execution.
- **Abstract Classes** provide a base for other classes to build upon and can contain both abstract and concrete methods.
- **Interfaces** define a contract that implementing classes must fulfill, allowing for multiple inheritance and promoting loose coupling.
