# java-dsa-guide
Comprehensive guide to Java basics, data structures, and algorithms for quick revision and interview preparation. Perfect for mastering coding challenges and technical interviews.


## Table of Contents

1. [Python Basics](#python-basics)
   - [Syntax and Variables](#syntax-and-variables)
   - [Data Types](#data-types)
   - [Control Structures](#control-structures)
   - [Functions and Modules](#functions-and-modules)
2. [Basic Data Structures](#basic-data-structures)
   - [Lists](#lists)
   - [Tuples](#tuples)
   - [Sets](#sets)
   - [Dictionaries](#dictionaries)
3. [Advanced Data Structures](#advanced-data-structures)
   - [Arrays](#arrays)
   - [Linked Lists](#linked-lists)
   - [Stacks](#stacks)
   - [Queues](#queues)
   - [Trees](#trees)
   - [Graphs](#graphs)
   - [Heaps](#heaps)
   - [Hash Tables](#hash-tables)
4. [Common Algorithms](#common-algorithms)
   - [Sorting Algorithms](#sorting-algorithms)
   - [Searching Algorithms](#searching-algorithms)
   - [Dynamic Programming](#dynamic-programming)
   - [Graph Algorithms](#graph-algorithms)
5. [Interview Tips](#interview-tips)

# Java Basics

## Data Types

```java
int integer = 5;                    // int : primitive
double floatNumber = 5.0;            // double : floating-point number
String string = "Hello";             // String : immutable, non-primitive
int[] array = {1, 2, 3};             // Array : fixed size, mutable
List<Integer> listExample = new ArrayList<>(Arrays.asList(1, 2, 3));  // List : mutable, dynamic size
Set<Integer> setExample = new HashSet<>(Arrays.asList(1, 2, 3));      // Set : unordered, unique elements
Map<String, Integer> mapExample = new HashMap<>();                    // Map : key-value pairs
mapExample.put("a", 1);
mapExample.put("b", 2);
```

- **Time Complexity** (common operations):
  - **List (ArrayList)**: Add: O(1) (amortized), Access: O(1), Remove: O(n)
  - **Set (HashSet)**: Add/Remove/Contains: O(1)
  - **Map (HashMap)**: Put/Get: O(1), Remove: O(1)

## Control Structures

### If-Else Statements

```java
if (x > 0) {  
    // action if x is positive
} else if (x < 0) {  
    // action if x is negative
} else {  
    // action if x is zero
}
```

- **Ternary Operator**:

```java
String result = true ? "val1" : "val2"; 
```

### Loops

```java
// For Loop
for (int i = 0; i < 5; i++) {
    // action
}  // Time complexity: O(n)

for (int i = 4; i >= 0; i--) {
    // action
}  // Time complexity: O(n)
```

- **Enhanced For Loop (foreach)**:

```java
for (int num : arr) {
    // iterate over elements in array
}  // Time complexity: O(n)
```

- **Iterate with index**:

```java
for (int index = 0; index < arr.length; index++) {
    int num = arr[index];
    System.out.println(index + ": " + num);
}  // Time complexity: O(n)
```

- **Single line for loop (List initialization)**:

```java
List<Integer> squaredList = new ArrayList<>();
for (int i = 0; i < 5; i++) {
    squaredList.add(i * i);  // adds squares to the list
}  // Time complexity: O(n)
```

- **Using break and continue**:

```java
for (int i = 0; i < 10; i++) {
    if (i == 5) {
        break;  // exits loop when i is 5
    }
    System.out.println(i);
}  // Time complexity: O(n)

for (int i = 0; i < 10; i++) {
    if (i % 2 == 0) {
        continue;  // skips even numbers
    }
    System.out.println(i);  // prints odd numbers
}  // Time complexity: O(n)
```

- **While Loop**:

```java
int i = 0;
while (i < 5) {
    System.out.println(i);
    i++;
}  // Time complexity: O(n)
```

## Sorting with `Comparator` (Equivalent of attrgetter)

```java
import java.util.Comparator;
import java.util.Collections;

// Sorting objects using Comparator
Collections.sort(students, Comparator.comparing(Student::getGrade)
                                     .thenComparing(Student::getAge)
                                     .reversed());  
// Sort students by grade, then by age in descending order
```

- **Time Complexity**: O(n log n)





