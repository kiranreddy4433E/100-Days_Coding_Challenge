# Day 20 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 20** of my **100 Days of Code Challenge**! Today, I implemented a Java program that checks if a number is **prime**. This exercise helped me practice efficient divisibility checks, including using the square root optimization for prime detection.

## ✅ What I did today
- Wrote a Java program to determine if a given number is a **prime number**.
- Practiced using loops and conditional statements to check divisibility.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Prime Numbers, Loops, Conditional Statements

## 📖 Problem Description
- A **prime number** is a positive integer greater than 1 that has no positive divisors other than 1 and itself. For example:
  - 2, 3, 5, and 7 are prime numbers.
  - 4, 6, 8, and 9 are not prime numbers.

### Input/Output Example:
  - **Input**: `5`
    - **Output**: `5 is a prime number.`
  
  - **Input**: `10`
    - **Output**: `10 is not a prime number.`

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_32 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int num = input.nextInt();
        
        boolean isPrime = true;
        if (num <= 1) {
            isPrime = false;  
        } else {
            for (int i = 2; i <= Math.sqrt(num); i++) {
                if (num % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }
        
        // Output result based on the isPrime flag
        if (isPrime) {
            System.out.println(num + " is a prime number.");
        } else {
            System.out.println(num + " is not a prime number.");
        }
        
        input.close();
    }
}
```
---

### 🖥️ Program Output


Enter a number: 5
5 is a prime number.

Enter a number: 10
10 is not a prime number.

---

### 📚 Lessons Learned
Learned how to check for prime numbers efficiently by only iterating up to the square root of the number.
Practiced using boolean flags and conditional statements for prime detection logic.

---
### ⚡ Challenges
Implementing the square root optimization correctly was key to ensuring the program's efficiency for larger numbers.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
