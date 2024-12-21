# Day 69 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 69** of my **100 Days of Code Challenge**! Today, I implemented a program to demonstrate the concept of **multi-level inheritance** in Java. This involves creating a class hierarchy where a derived class inherits from another derived class.

## ✅ What I did today
- Created a class hierarchy to illustrate multi-level inheritance:
  - `A`: Base class representing an equilateral triangle.
  - `B`: Derived class representing an isosceles triangle, inheriting from `A`.
  - `C`: Derived class representing a general triangle, inheriting from `B`.
- Accessed properties of all classes through an object of the most derived class (`C`).

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Multi-level Inheritance, Object-Oriented Programming (OOP)

## 📖 Problem Description
- Create a class hierarchy:
  1. Class `A` should represent an equilateral triangle with a property `"I am an equilateral triangle"`.
  2. Class `B` should inherit from `A` and add a property `"I am an isosceles triangle"`.
  3. Class `C` should inherit from `B` and add a property `"I am a triangle"`.
- Instantiate an object of class `C` and access all properties from `A`, `B`, and `C`.

---

### Input/Output Example:

#### Example:
**Input**:
(No user input is required; the program is hardcoded to demonstrate inheritance.)

**Output**:
I am an equilateral triangle I am an isosceles triangle I am a triangle

---

## 📝 Code Example

```java
package coading_Challange;

// Base class A
class A {
    String triangle = "I am an equilateral triangle";
}

// Derived class B inherits from A
class B extends A {
    String triangle1 = "I am an isosceles triangle";
}

// Derived class C inherits from B
class C extends B {
    String triangle2 = "I am a triangle";
}

public class Day_69 {

    public static void main(String[] args) {
        // Create an object of class C
        C str = new C();
        
        // Access properties from all classes in the hierarchy
        System.out.println(str.triangle);
        System.out.println(str.triangle1);
        System.out.println(str.triangle2);
    }
}
🖥️ Program Output

I am an equilateral triangle
I am an isosceles triangle
I am a triangle
```
---
## 📚 Lessons Learned
Gained practical experience with multi-level inheritance in Java.
Reinforced the concept of class hierarchy and how derived classes can inherit properties from base classes.
Understood how objects of the most derived class can access properties from all levels of the hierarchy.

---
## ⚡ Challenges
Ensuring that all properties are correctly inherited by the most derived class (C).
Managing class relationships to avoid redundancy or unnecessary dependencies.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
