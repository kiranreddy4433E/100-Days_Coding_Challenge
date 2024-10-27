# Day 16 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 16** of my **100 Days of Code Challenge**! Today, I implemented a Java program that checks if a number is a **Perfect Number**. This exercise allowed me to practice working with divisors and applying basic arithmetic operations to determine if a number is perfect.

## ✅ What I did today
- Wrote a Java program to check if a given number is a **Perfect Number**.
- Practiced using loops and conditional logic to identify and sum divisors.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Loops, Conditional Statements, Divisors, Perfect Numbers

## 📖 Problem Description
- A **Perfect Number** is a positive integer that is equal to the sum of its proper divisors, excluding itself. For example:
  - \(6\) is a perfect number because \(1 + 2 + 3 = 6\).
  - \(28\) is also a perfect number because \(1 + 2 + 4 + 7 + 14 = 28\).

### Input/Output Example:
  - Input: `6`
    - Output: `6 is a perfect number.`
  
  - Input: `10`
    - Output: `10 is not a perfect number.`

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_27 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter a Number");
        int perfect = input.nextInt();
        int sum = 0;

        // Check for divisors and calculate the sum of divisors
        for (int i = 1; i <= perfect / 2; i++) {
            if (perfect % i == 0) { 
                sum += i; 
                System.out.println("Divisor found: " + i); 
            }
        }

        System.out.println("Sum of divisors: " + sum); 

        // Check if the sum of divisors equals the original number
        if (sum == perfect) {
            System.out.println(perfect + " is a perfect number.");
        } else {
            System.out.println(perfect + " is not a perfect number.");
        }

        input.close();
    }
}
```
---

### 🖥️ Program Output

Enter a Number
6
Divisor found: 1
Divisor found: 2
Divisor found: 3
Sum of divisors: 6
6 is a perfect number.

Enter a Number
10
Divisor found: 1
Divisor found: 2
Divisor found: 5
Sum of divisors: 8
10 is not a perfect number.

---

### 📚 Lessons Learned
Practiced calculating divisors of a number and summing them to check for perfection.
Reinforced the use of loops and conditional statements to control program flow.
Gained insights into the concept of Perfect Numbers and their unique properties.

---

### ⚡ Challenges
Ensuring the program correctly excludes the number itself from the sum of divisors was essential to get accurate results.

---

### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---

### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
