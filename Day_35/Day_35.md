# Day 35 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 35** of my **100 Days of Code Challenge**! Today, I wrote a Java program to calculate the sum of all numeric digits in a given string. This task helped me practice identifying digits in a string and performing arithmetic operations.

## ✅ What I did today
- Wrote a Java program to find the sum of all numeric digits in a string.
- Practiced using `Character.isDigit()` and converting characters to integers.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, Loops, Character Manipulation

## 📖 Problem Description
- The task is to identify all numeric digits in a string and compute their sum. Non-numeric characters are ignored. For example:
  - Input: `"abc123xyz"`
  - Output: `6` (sum of `1`, `2`, and `3`)

### Input/Output Example:
  - **Input**:
    ```
    Enter a string: abc123xyz
    ```
  - **Output**:
    ```
    Sum of numbers in the string: 6
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_52 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a string: ");
        
        String str = input.nextLine();
        int sum = 0;

        // Iterate through the string to identify digits
        for (int i = 0; i < str.length(); i++) {
            char ch = str.charAt(i);
            if (Character.isDigit(ch)) {
                int num = ch - '0'; // Convert char to int
                sum += num;        // Add to the sum
            }
        }
        
        System.out.println("Sum of numbers in the string: " + sum);
        input.close();
    }
}
🖥️ Program Output

Enter a string: 
abc123xyz
Sum of numbers in the string: 6
```
---
### 📚 Lessons Learned
Learned how to identify numeric characters in a string using Character.isDigit().
Practiced converting character digits to integers and performing arithmetic operations.

---
### ⚡ Challenges
Ensuring only numeric characters were included in the sum and ignoring non-numeric characters.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
