# Day 30 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 30** of my **100 Days of Code Challenge**! Today, I implemented a Java program to calculate the **length of a string** without using built-in string length functions. This exercise was a great way to practice working with loops and character arrays.

## ✅ What I did today
- Wrote a Java program to find the length of a string by manually counting characters.
- Practiced iterating through strings with character arrays.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Loops, Strings, Character Arrays

## 📖 Problem Description
- The task is to find the length of a given string without using built-in functions such as `strlen()` or `length()`. For example:
  - Input: `"Hello"`
  - Output: `5`

### Input/Output Example:
  - **Input**:
    ```
    Enter a Word: Hello
    ```
  - **Output**:
    ```
    Length of the word is: 5
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_45 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        System.out.print("Enter a Word: ");
        String str = input.nextLine();
        
        // Manually calculate the length by counting characters
        int length = 0;
        for (char c : str.toCharArray()) {
            length++;
        }
        
        System.out.println("Length of the word is: " + length);
        input.close();
    }
}
🖥️ Program Output

Enter a Word: 
Hello
Length of the word is: 5
```
---
### 📚 Lessons Learned
- Reinforced understanding of string manipulation by manually counting characters.
- Improved skills in handling string inputs and using character arrays for iteration.

---
### ⚡ Challenges
Ensuring all characters were counted correctly, especially when iterating through strings without built-in functions.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
