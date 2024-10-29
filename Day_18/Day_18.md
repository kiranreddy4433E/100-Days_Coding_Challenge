# Day 18 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 18** of my **100 Days of Code Challenge**! Today, I implemented a Java program that takes two fractions as input, calculates their sum, and outputs the result in simplified form. This exercise helped me practice working with fractions, applying the **GCD (Greatest Common Divisor)**, and simplifying fractions.

## ✅ What I did today
- Wrote a Java program to add two fractions and simplify the result using the **GCD** method.
- Practiced using recursive functions and conditional statements for fraction operations.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Fractions, Greatest Common Divisor (GCD), Recursion

## 🔗 Links to Code
- [Day 18 Code Repository](#link-to-repository): This repository contains the code solution for adding and simplifying fractions.

## 📖 Problem Description
- The task is to take two fractions as input, add them, and simplify the result. For example:
  - Input fractions: \( \frac{1}{2} \) and \( \frac{1}{3} \)
    - Result: \( \frac{5}{6} \)

### Input/Output Example:
  - **Input**:
    ```
    x1 = 1, y1 = 2
    x2 = 1, y2 = 3
    ```
  - **Output**:
    ```
    Result: 5/6
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_29 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        // Input fractions
        System.out.println("Enter x1 and y1: ");
        int x1 = input.nextInt();
        int y1 = input.nextInt();
        
        System.out.println("Enter x2 and y2: ");
        int x2 = input.nextInt();
        int y2 = input.nextInt();
        
        // Calculate the numerator and denominator of the result
        int x3 = (x1 * y2) + (x2 * y1);
        int y3 = (y1 * y2);
        
        // Simplify the fraction using GCD
        int gcd = gcd(x3, y3);
        x3 /= gcd;
        y3 /= gcd;
        
        // Print the result as a simplified fraction
        System.out.println("Result: " + x3 + "/" + y3);
        
        input.close();
    }

    // Method to calculate the Greatest Common Divisor (GCD) using recursion
    private static int gcd(int a, int b) {
        if (b == 0) return Math.abs(a);
        return gcd(b, a % b);
    }
}
```
---

### 🖥️ Program Output

- Enter x1 and y1: 
- 1 2
- Enter x2 and y2: 
- 1 3
- Result: 5/6

---

### 📚 Lessons Learned
Practiced calculating the GCD to simplify fractions.
Reinforced my understanding of fraction operations and recursive methods.
Learned the importance of handling both the numerator and denominator when performing addition on fractions.

---

### ⚡ Challenges
Ensuring the GCD calculation was accurate and that the result was simplified correctly was key to achieving the correct output.

---

### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
