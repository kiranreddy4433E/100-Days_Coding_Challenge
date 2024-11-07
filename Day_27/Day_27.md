
Here’s the README.md for Day 27 of your 100 Days of Code Challenge, where you wrote a program to find the double of a given number without using arithmetic operators.

markdown
Copy code
# Day 27 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 27** of my **100 Days of Code Challenge**! Today, I implemented a Java program that calculates the **double of a given number** without using traditional arithmetic operators. Instead, I used bitwise shift operations to achieve this.

## ✅ What I did today
- Wrote a Java program to double a number without using `+`, `-`, `*`, or `/`.
- Practiced using **bitwise shift operators** to manipulate integer values.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Bitwise Operations, Left Shift

## 📖 Problem Description
- The task is to double a given integer without using arithmetic operators. Using the left shift (`<<`) operator, we can double a number by shifting its bits to the left by one position. For example:
  - Input: `5`
  - Double: `10` (using `5 << 1`).

### Input/Output Example:
  - **Input**: `5`
  - **Output**:
    ```
    Double of the number is: 10
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_39 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a number: ");
        
        int num = input.nextInt();
        
        // Use bitwise shift to double the number
        int doubled = num << 1;
        
        // Print the result
        System.out.println("Double of the number is: " + doubled);
        
        input.close();
    }
}
```
---
### 🖥️ Program Output

- Enter a number: 
- 5
- Double of the number is: 10

---
### 📚 Lessons Learned
- Learned how to use bitwise shift operators for mathematical operations.
- Reinforced my understanding of binary representations and bit manipulation techniques.

---
### ⚡ Challenges
The main challenge was understanding the mechanics of bitwise operations and ensuring the left shift correctly doubled the value.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
