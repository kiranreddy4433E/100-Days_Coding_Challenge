# Day 21 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 21** of my **100 Days of Code Challenge**! Today, I implemented a Java program that checks if a number is a **Palindrome**. This exercise helped me practice number manipulation by reversing digits and comparing values.

## ✅ What I did today
- Wrote a Java program to determine if a given number is a **Palindrome**.
- Practiced reversing numbers and using conditional statements for comparison.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Loops, Palindrome, Number Manipulation

## 📖 Problem Description
- A **Palindrome** number is a number that reads the same backward as forward. For example:
  - 121 is a palindrome because reversing it gives the same number (121).
  - 123 is not a palindrome because reversing it gives 321.

### Input/Output Example:
  - **Input**: `121`
    - **Output**: `121 is a palindrome.`
  
  - **Input**: `123`
    - **Output**: `123 is not a palindrome.`

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_33 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter a number: ");
        
        int num = input.nextInt();
        int originalNum = num;
        int reversedNum = 0;
        
        // Reverse the number
        while(num != 0) {
            int digit = num % 10;
            reversedNum = reversedNum * 10 + digit;
            num /= 10;
        }
        
        // Check if original and reversed numbers are the same
        if (originalNum == reversedNum) {
            System.out.println(originalNum + " is a palindrome.");
        } else {
            System.out.println(originalNum + " is not a palindrome.");
        }
        
        input.close();
    }
}
```
---
### 🖥️ Program Output

- Enter a number: 
- 121
- 121 is a palindrome.

- Enter a number: 
- 123
- 123 is not a palindrome.

---
### 📚 Lessons Learned
Learned how to reverse a number by extracting digits and reconstructing it in reverse order.
Practiced using loops and conditional statements to identify palindromic numbers.

---
### ⚡ Challenges
Ensuring the reversal of the number was accurate to allow for proper comparison with the original value.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
