
# **Unit 2: Objects and Classes**

## **1. Introduction to Classes and Objects**

In Java, a **class** is a blueprint for creating objects. It defines a datatype by bundling data and methods that work on the data into one single unit. An **object** is an instance of a class. For example, consider a class `Car`:

```java
public class Car {
    // Fields
    String color;
    String model;
    int year;

    // Method
    void displayInfo() {
        System.out.println("Model: " + model);
        System.out.println("Color: " + color);
        System.out.println("Year: " + year);
    }
}
```

Here, `Car` is a class with fields `color`, `model`, and `year`, and a method `displayInfo()`.

To create an object of this class:

```java
public class Main {
    public static void main(String[] args) {
        Car myCar = new Car(); // Creating an object
        myCar.color = "Red";
        myCar.model = "Toyota";
        myCar.year = 2021;
        myCar.displayInfo();
    }
}
```

**Output:**

```
Model: Toyota
Color: Red
Year: 2021
```

In this example, `myCar` is an object of the `Car` class.

## **2. Constructors**

A **constructor** is a special method that is called when an object is instantiated. It initializes the object. Constructors have the same name as the class and do not have a return type.

### **Types of Constructors:**

1. **Default Constructor:** Provided by Java if no constructor is defined. It initializes fields to default values.

2. **Parameterized Constructor:** Accepts parameters to initialize fields with specific values.

**Example:**

```java
public class Car {
    String color;
    String model;
    int year;

    // Parameterized Constructor
    public Car(String c, String m, int y) {
        color = c;
        model = m;
        year = y;
    }

    void displayInfo() {
        System.out.println("Model: " + model);
        System.out.println("Color: " + color);
        System.out.println("Year: " + year);
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car("Blue", "Honda", 2022);
        myCar.displayInfo();
    }
}
```

**Output:**

```
Model: Honda
Color: Blue
Year: 2022
```

In this example, the `Car` class has a parameterized constructor that initializes the fields.

## **3. Access Modifiers**

Access modifiers in Java determine the visibility of classes, methods, and variables. The four types are:

1. **Private:** Accessible only within the same class.
2. **Default (no modifier):** Accessible within the same package.
3. **Protected:** Accessible within the same package and subclasses.
4. **Public:** Accessible from any other class.

**Example:**

```java
public class Person {
    private String name; // Private field
    int age; // Default access
    protected String address; // Protected field
    public String email; // Public field

    public void setName(String n) {
        name = n;
    }

    public String getName() {
        return name;
    }
}

public class Main {
    public static void main(String[] args) {
        Person p = new Person();
        p.setName("Alice");
        p.age = 30; // Accessible within the same package
        p.address = "123 Main St"; // Accessible within the same package
        p.email = "alice@example.com"; // Accessible from anywhere
        System.out.println("Name: " + p.getName());
        System.out.println("Age: " + p.age);
        System.out.println("Address: " + p.address);
        System.out.println("Email: " + p.email);
    }
}
```

**Output:**

```
Name: Alice
Age: 30
Address: 123 Main St
Email: alice@example.com
```

In this example, the `name` field is private and accessed via getter and setter methods, while other fields have different access levels.

## **4. Inbuilt Classes: String and File**

### **String Class**

The `String` class represents a sequence of characters. Strings are immutable in Java.

**Example:**

```java
public class Main {
    public static void main(String[] args) {
        String greeting = "Hello, World!";
        System.out.println("Length: " + greeting.length());
        System.out.println("Uppercase: " + greeting.toUpperCase());
        System.out.println("Substring: " + greeting.substring(7, 12));
    }
}
```

**Output:**

```
Length: 13
Uppercase: HELLO, WORLD!
Substring: World
```

### **File Class**

The `File` class is used to represent file and directory pathnames.

**Example:**

```java
import java.io.File;

public class Main {
    public static void main(String[] args) {
        File file = new File("example.txt");

        if (file.exists()) {
            System.out.println("File name: " + file.getName());
            System.out.println("Absolute path: " + file.getAbsolutePath());
            System.out.println("Writable: " + file.canWrite());
            System.out.println("Readable: " + file.canRead());
            System.out.println("File size in bytes: " + file.length());
        } else {
            System.out.println("The file does not exist.");
        }
    }
}
```

**Output:**

```
File name: example.txt
Absolute path: /path/to/example.txt
Writable: true
Readable: true
File size in bytes: 1024
```

In this example, the `File` class is used to obtain information about a file.

## **Conclusion**

- **Classes and Objects:** Fundamental concepts in Java, where classes define the blueprint and objects are instances of classes.
- **Constructors:** Special methods to initialize new objects.
- **Access Modifiers:** Control the visibility and accessibility of classes, methods, and variables.
- **Inbuilt Classes:** Java provides many built-in classes like `String` and `File` to handle common tasks.

This concludes **Unit 2: Objects and Classes**.
