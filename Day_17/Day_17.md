# Day 17 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 17** of my **100 Days of Code Challenge**! Today, I implemented a Java program that finds the **factors of a given number**. This challenge helped me reinforce the use of loops and conditional statements to check divisibility.

## ✅ What I did today
- Wrote a Java program to find all **factors** of a user-provided integer.
- Practiced using conditional statements to check divisibility.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Loops, Conditional Statements, Factors

## 📖 Problem Description
- The task is to take an integer input and find all of its **factors**. A factor of a number is any number that divides it without leaving a remainder. For example:
  - Factors of `12` are `1, 2, 3, 4, 6, and 12`.
  - Factors of `15` are `1, 3, 5, and 15`.

### Input/Output Example:
  - Input: `12`
    - Output: `1 2 3 4 6 12`
  
  - Input: `15`
    - Output: `1 3 5 15`

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_28 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter a number to find its factors:");
        int fraction = input.nextInt();
        
        System.out.print("Factors of " + fraction + " are: ");
        for (int i = 1; i <= fraction; i++) {
            if (fraction % i == 0) {          
                System.out.print(i + " "); 
            }
        }
        
        input.close();
    }
}
```
---

### 🖥️ Program Output

Enter a number to find its factors:
12
Factors of 12 are: 1 2 3 4 6 12

Enter a number to find its factors:
15
Factors of 15 are: 1 3 5 15

---

### 📚 Lessons Learned
Practiced using loops to iterate over a range of numbers.
Reinforced the use of the modulus operator (%) to check for divisibility.
Learned how to identify factors by checking for zero remainders.

---

### ⚡ Challenges
Optimizing the loop to check only up to the square root of the number could further improve efficiency.

---

### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
