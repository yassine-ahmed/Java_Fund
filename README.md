# Object-Oriented Programming (OOP) in Java

This document provides a comprehensive guide to **Object-Oriented Programming (OOP)** in Java. It covers all the essential OOP principles, concepts, and best practices you need to master to excel in Java and prepare for interviews.

## Table of Contents
- [Introduction to OOP](#introduction-to-oop)
- [Four Pillars of OOP](#four-pillars-of-oop)
  - [Encapsulation](#encapsulation)
  - [Inheritance](#inheritance)
  - [Polymorphism](#polymorphism)
  - [Abstraction](#abstraction)
- [Other Important Concepts](#other-important-concepts)
  - [Interfaces](#interfaces)
  - [Constructors](#constructors)
  - [`this` and `super`](#this-and-super)
- [Advanced Concepts](#advanced-concepts)
  - [Inner Classes](#inner-classes)
  - [Exception Handling](#exception-handling)
- [Design Patterns](#design-patterns)
- [Best Practices](#best-practices)
- [Practical Steps for Mastery](#practical-steps-for-mastery)

---

## Introduction to OOP

**Object-Oriented Programming (OOP)** is a programming paradigm based on the concept of "objects," which contain both **data (fields)** and **methods (functions)**. Java is a fully object-oriented programming language, meaning it uses OOP principles to model real-world entities.

In Java, OOP allows us to:
- Organize and structure code in a reusable and scalable way.
- Create objects that interact with each other to solve complex problems.
- Improve maintainability by adhering to principles like **encapsulation**, **inheritance**, and **abstraction**.

---

## Four Pillars of OOP

### Encapsulation

**Encapsulation** refers to the concept of bundling data (fields) and methods (behaviors) that operate on the data into a single unit or class. It also involves restricting access to the internal state of an object to ensure that the object's data is protected from unintended modifications.

In Java, encapsulation is achieved by:
- Using **private** access modifiers for fields.
- Providing **public getter and setter methods** to access and modify the fields.

#### Example:
```java
class Person {
    private String name; // Private field
    private int age;     // Private field

    // Getter method for name
    public String getName() {
        return name;
    }

    // Setter method for name
    public void setName(String name) {
        this.name = name;
    }

    // Getter method for age
    public int getAge() {
        return age;
    }

    // Setter method for age
    public void setAge(int age) {
        if (age >= 0) { // Adding validation logic
            this.age = age;
        }
    }
}

### Inheritance

**Inheritance** The ability for a new class to inherit properties and methods from an existing class.
- Supports code reuse and is key to the concept of a class hierarchy.

#### Example:
```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.sound();  // Outputs: Dog barks
    }
}

### Polymorphism

**Polymorphism** The ability to define multiple methods with the same name but with different implementations.
- Method Overloading (same method name, different parameters) and Method Overriding (same method signature in parent and child classes) are key aspects.

#### Example of Overloading:
```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
}

#### Example of Overriding:
```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

### Abstraction

**Abstraction** The concept of hiding the complex implementation details and showing only the essential features of an object.
- In Java, abstract classes and interfaces are used to achieve abstraction.

#### Abstract Class Example:
```java
abstract class Animal {
    abstract void sound();
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }
}


### Other Important Concepts

**Interfaces** An interface is a contract that a class must follow. It contains only abstract methods (before Java 8), but from Java 8 onwards, it can also contain default methods.
- Interfaces allow you to implement multiple behaviors in a class, since Java supports only single inheritance but allows multiple interfaces.

#### Example:
```java
interface Animal {
    void sound();
}

class Dog implements Animal {
    public void sound() {
        System.out.println("Dog barks");
    }
}

**Constructors** A constructor is a special method used to initialize objects. It has the same name as the class and no return type.
- A default constructor is provided if no constructor is defined, but you can create your own constructor.


#### Example:
```java
class Car {
    String model;
    int year;

    // Constructor
    public Car(String model, int year) {
        this.model = model;
        this.year = year;
    }
}





