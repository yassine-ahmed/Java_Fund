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

By hiding the internal state and only exposing necessary operations, we can control how data is accessed or modified, ensuring integrity.
1. **Example**:

   ```java
   class Person {
    private String name;
    private int age;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        if (age >= 0) {
            this.age = age;
        }
    }
   }

