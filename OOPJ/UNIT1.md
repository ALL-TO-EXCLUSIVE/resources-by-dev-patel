# **Unit 1: Introduction to Java**

## **1. Basics of Java Programming**
Java is a high-level, object-oriented programming language developed by **Sun Microsystems** (now owned by Oracle). It is widely used for building **desktop applications, web applications, and mobile applications**.

### **Features of Java**
- **Platform Independent:** Write once, run anywhere (WORA) due to JVM.
- **Object-Oriented:** Everything in Java revolves around objects and classes.
- **Robust and Secure:** Strong memory management and security features.
- **Multithreaded:** Supports concurrent execution of programs.
- **Automatic Garbage Collection:** Java handles memory management automatically.

---

## **2. Data Types in Java**
Java provides **primitive** and **non-primitive** data types:

### **Primitive Data Types:**
| Data Type | Size   | Default Value | Example |
|-----------|--------|---------------|---------|
| byte      | 1 byte | 0             | `byte b = 10;` |
| short     | 2 bytes | 0             | `short s = 5000;` |
| int       | 4 bytes | 0             | `int i = 100000;` |
| long      | 8 bytes | 0L            | `long l = 150000L;` |
| float     | 4 bytes | 0.0f          | `float f = 5.75f;` |
| double    | 8 bytes | 0.0d          | `double d = 19.99;` |
| char      | 2 bytes | '\u0000'      | `char c = 'A';` |
| boolean   | 1 bit  | false         | `boolean flag = true;` |

### **Example:**
```java
public class DataTypesExample {
    public static void main(String[] args) {
        int num = 10;
        double price = 99.99;
        char grade = 'A';
        boolean isJavaFun = true;
        
        System.out.println("Number: " + num);
        System.out.println("Price: " + price);
        System.out.println("Grade: " + grade);
        System.out.println("Is Java Fun? " + isJavaFun);
    }
}
```

---

## **3. Variables in Java**
A variable is a container that holds data values.

### **Types of Variables:**
1. **Local Variables** - Declared inside a method and used only within that method.
2. **Instance Variables** - Defined inside a class but outside methods; each object has its own copy.
3. **Static Variables** - Declared using `static`; shared across all objects of a class.

### **Example:**
```java
class Example {
    int instanceVar = 5; // Instance variable
    static int staticVar = 10; // Static variable
    
    public void display() {
        int localVar = 20; // Local variable
        System.out.println("Local: " + localVar);
        System.out.println("Instance: " + instanceVar);
        System.out.println("Static: " + staticVar);
    }
    
    public static void main(String[] args) {
        Example obj = new Example();
        obj.display();
    }
}
```

---

## **4. Operators in Java**
Java provides different types of operators:

### **Arithmetic Operators:**
`+ - * / %`

```java
int a = 10, b = 5;
System.out.println(a + b); // 15
System.out.println(a - b); // 5
```

### **Relational Operators:**
`== != > < >= <=`

```java
boolean result = (10 > 5); // true
```

### **Logical Operators:**
`&& || !`

```java
boolean andResult = (true && false); // false
```

### **Assignment Operators:**
`= += -= *= /= %=`

```java
int x = 10;
x += 5; // x = x + 5;
System.out.println(x); // 15
```

---

## **5. Control Structures in Java**
Control structures define the flow of execution in a program.

### **Selection Statements (if-else, switch-case)**
```java
if (num > 0) {
    System.out.println("Positive Number");
} else {
    System.out.println("Negative Number");
}
```

```java
switch (grade) {
    case 'A':
        System.out.println("Excellent");
        break;
    case 'B':
        System.out.println("Good");
        break;
    default:
        System.out.println("Needs Improvement");
}
```

### **Looping Statements (for, while, do-while)**
```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

```java
int count = 0;
while (count < 5) {
    System.out.println(count);
    count++;
}
```

---

## **6. Java Methods**
Methods are reusable blocks of code.

```java
class MethodsExample {
    public static int add(int a, int b) {
        return a + b;
    }
    public static void main(String[] args) {
        System.out.println(add(5, 10)); // 15
    }
}
```

### **Method Overloading:**
```java
class OverloadExample {
    void display(int a) {
        System.out.println("Integer: " + a);
    }
    void display(String b) {
        System.out.println("String: " + b);
    }
    public static void main(String[] args) {
        OverloadExample obj = new OverloadExample();
        obj.display(10);
        obj.display("Java");
    }
}
```

---

## **7. Math Class in Java**
The `Math` class provides mathematical functions.

```java
System.out.println(Math.sqrt(25)); // 5.0
System.out.println(Math.pow(2, 3)); // 8.0
System.out.println(Math.random()); // Random number between 0.0 and 1.0
System.out.println(Math.abs(-5)); // 5
System.out.println(Math.max(10, 20)); // 20
System.out.println(Math.min(10, 20)); // 10

```

---

## **8. Arrays in Java**
Arrays store multiple values of the same type.

```java
int[] numbers = {1, 2, 3, 4, 5};
for (int num : numbers) {
    System.out.println(num);
}
```

---

## **Conclusion**
- Java is a **powerful, object-oriented** language.
- Understanding **data types, variables, operators, and control structures** is fundamental.
- Java methods and arrays provide **structured programming** capabilities.

This completes **Unit 1: Introduction to Java** 🚀
