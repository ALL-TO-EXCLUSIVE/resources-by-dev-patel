# **Unit 4: Java Collections Framework**

## **1. Introduction to Collections Framework**

The Java Collections Framework is a unified architecture for representing and manipulating collections. It allows developers to store, retrieve, and manipulate data efficiently. The framework includes interfaces, implementations (classes), and algorithms to handle various data structures like lists, sets, queues, and maps.

**Key Benefits:**

- **Reduces Programming Effort:** Provides ready-to-use data structures and algorithms.
- **Increases Performance:** Offers high-performance implementations of data structures.
- **Enhances Interoperability:** Standardizes the way collections are handled across different APIs.

## **2. Core Interfaces of the Collections Framework**

The framework is built around several core interfaces:

- **Collection:** The root interface for all collection classes.
- **List:** An ordered collection that allows duplicate elements.
- **Set:** A collection that does not allow duplicate elements.
- **Queue:** A collection used to hold multiple elements prior to processing.
- **Map:** An object that maps keys to values; cannot contain duplicate keys.

## **3. List Interface**

The `List` interface extends the `Collection` interface and represents an ordered collection. Elements can be inserted or accessed by their position (index). Common implementations include `ArrayList` and `LinkedList`.

**Example:**

```java
import java.util.ArrayList;
import java.util.List;

public class ListExample {
    public static void main(String[] args) {
        List<String> fruits = new ArrayList<>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");

        // Accessing elements
        System.out.println(fruits.get(1)); // Output: Banana

        // Iterating over the list
        for (String fruit : fruits) {
            System.out.println(fruit);
        }
    }
}
```

**Output:**

```
Banana
Apple
Banana
Cherry
```

## **4. Set Interface**

The `Set` interface extends the `Collection` interface and represents a collection that does not allow duplicate elements. Common implementations include `HashSet` and `TreeSet`.

**Example:**

```java
import java.util.HashSet;
import java.util.Set;

public class SetExample {
    public static void main(String[] args) {
        Set<String> colors = new HashSet<>();
        colors.add("Red");
        colors.add("Blue");
        colors.add("Green");
        colors.add("Red"); // Duplicate element

        // Iterating over the set
        for (String color : colors) {
            System.out.println(color);
        }
    }
}
```

**Output:**

```
Red
Blue
Green
```

*Note: The output order may vary as `HashSet` does not guarantee order.*

## **5. Queue Interface**

The `Queue` interface extends the `Collection` interface and represents a collection used to hold multiple elements prior to processing. Common implementations include `LinkedList` and `PriorityQueue`.

**Example:**

```java
import java.util.LinkedList;
import java.util.Queue;

public class QueueExample {
    public static void main(String[] args) {
        Queue<String> queue = new LinkedList<>();
        queue.add("John");
        queue.add("Jane");
        queue.add("Jack");

        // Processing elements
        while (!queue.isEmpty()) {
            System.out.println(queue.poll());
        }
    }
}
```

**Output:**

```
John
Jane
Jack
```

## **6. Map Interface**

The `Map` interface is not a subtype of `Collection`. It represents a collection that maps keys to values, with no duplicate keys allowed. Common implementations include `HashMap` and `TreeMap`.

**Example:**

```java
import java.util.HashMap;
import java.util.Map;

public class MapExample {
    public static void main(String[] args) {
        Map<String, Integer> ages = new HashMap<>();
        ages.put("Alice", 30);
        ages.put("Bob", 25);
        ages.put("Charlie", 28);

        // Accessing values
        System.out.println("Alice's age: " + ages.get("Alice"));

        // Iterating over the map
        for (Map.Entry<String, Integer> entry : ages.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
```

**Output:**

```
Alice's age: 30
Alice: 30
Bob: 25
Charlie: 28
```

## **7. Algorithms and Utilities**

The `Collections` class provides static methods for various operations on collections, such as sorting and searching.

**Example:**

```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class CollectionsExample {
    public static void main(String[] args) {
        List<Integer> numbers = new ArrayList<>();
        numbers.add(5);
        numbers.add(3);
        numbers.add(8);
        numbers.add(1);

        // Sorting the list
        Collections.sort(numbers);
        System.out.println("Sorted List: " + numbers);

        // Searching for an element
        int index = Collections.binarySearch(numbers, 3);
        System.out.println("Index of 3: " + index);
    }
}
```

**Output:**

```
Sorted List: [1, 3, 5, 8]
Index of 3: 1
```

## **8. Generics in Collections**

Generics provide type safety by allowing you to specify the type of objects a collection can contain.

**Example:**

```java
import java.util.ArrayList;
import java.util.List;

public class GenericsExample {
    public static void main(String[] args) {
        List<String> names = new ArrayList<>();
        names.add("Emma");
        names.add("Liam");

        // Compile-time error if you try to add an integer
        // names.add(123);

        for (String name : names) {
            System.out.println(name);
        }
    }
}
```

**Output:**

```
Emma
Liam
```

*Note: Attempting to add an integer to the `names` list will result in a compile-time error.*

## **Conclusion**

The Java Collections Framework provides a comprehensive set of interfaces and classes to handle various data structures efficiently. Understanding these components is crucial for effective Java programming.
