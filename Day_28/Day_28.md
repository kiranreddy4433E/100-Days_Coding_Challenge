# Day 28 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 28** of my **100 Days of Code Challenge**! Today, I implemented a Java program to reverse a given string. This exercise helped me practice working with string manipulation and loops in Java.

## ✅ What I did today
- Created a Java program to reverse a string based on user input.
- Practiced using loops to access characters in reverse order.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, Loops, Character Manipulation

## 📖 Problem Description
- The task is to take a string input from the user and print it in reverse order. For example:
  - Input: `"Hello"`
  - Output: `"olleH"`

### Input/Output Example:
  - **Input**: `"Hello"`
  - **Output**:
    ```
    olleH
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_40 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a string: ");
        
        String str = input.nextLine();
        
        // Loop to print characters in reverse order
        for (int i = str.length() - 1; i >= 0; i--) {
            System.out.print(str.charAt(i));
        }
        
        input.close();
    }
}


🖥️ Program Output

Enter a string: 
Hello
olleH
```
---
### 📚 Lessons Learned
- Practiced accessing and reversing characters in a string.
- Gained further understanding of string length calculation and character indexing.

---
### ⚡ Challenges
Managing character indices correctly to reverse the string accurately.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

--- 
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
