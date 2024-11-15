# Day 34 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 34** of my **100 Days of Code Challenge**! Today, I wrote a Java program to remove brackets from an algebraic expression. This task helped me practice using regular expressions and string manipulation.

## ✅ What I did today
- Wrote a Java program to remove all brackets (`()` brackets specifically) from a given algebraic expression.
- Practiced using `replaceAll()` with regex for pattern-based replacements.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, Regular Expressions, Character Replacement

## 🔗 Links to Code
- [Day 34 Code Repository](#link-to-repository): This repository contains the code solution for removing brackets from an algebraic expression.

## 📖 Problem Description
- The task is to remove all parentheses (`()`) from a given algebraic expression. For example:
  - Input: `"a + (b - c) * (d / e)"`
  - Output: `"a + b - c * d / e"`

### Input/Output Example:
  - **Input**:
    ```
    Enter an equation: (x + y) * (z - w)
    ```
  - **Output**:
    ```
    Equation without Brackets: x + y * z - w
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_51 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        System.out.print("Enter an equation: ");
        String equation = input.nextLine();
        
        // Remove brackets using regex
        String result = equation.replaceAll("[()]", "");
        
        System.out.println("Equation without Brackets: " + result);
        input.close();
    }
}
🖥️ Program Output

Enter an equation: 
(x + y) * (z - w)
Equation without Brackets: x + y * z - w
```
---
### 📚 Lessons Learned
Practiced using replaceAll() with regex to remove specific characters or patterns.
Reinforced understanding of string manipulation techniques in Java.

---
### ⚡ Challenges
Ensuring the regex correctly targeted only the brackets without altering other parts of the expression.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
