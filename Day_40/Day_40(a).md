# Day 40(a) of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 40(a)** of my **100 Days of Code Challenge**! Today, I implemented a Java program to modify a string by replacing a specific substring with another. This task helped me practice working with string manipulation and the `replace()` method.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept a string from the user.
  2. Remove a specified substring from the string.
  3. Replace it with a new substring provided by the user.
- Practiced using the `replace()` method for string modifications.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, Substring Replacement, Input Handling

## 🔗 Links to Code
- [Day 40(a) Code Repository](#link-to-repository): This repository contains the code solution for substring replacement.

## 📖 Problem Description
- The task is to:
  1. Get a string as input from the user.
  2. Get another string (substring) to be removed.
  3. Get a third input (new substring) to replace the removed substring.
  4. Display the modified string with the changes applied.
  
For example:
  - Input: `"Hello World"`
  - Substring to remove: `"World"`
  - New substring: `"Java"`
  - Output: `"Hello Java"`

### Input/Output Example:
  - **Input**:
    ```
    Enter a string: Hello World
    Enter the substring to remove: World
    Enter the new substring to add: Java
    ```
  - **Output**:
    ```
    Modified string:
    Hello Java
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_60 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        System.out.println("Enter a string:");
        String str = input.nextLine();
        
        System.out.println("Enter the substring to remove:");
        String str1 = input.nextLine();
        
        System.out.println("Enter the new substring to add:");
        String str2 = input.nextLine();
        
        // Replace the specified substring
        String result = str.replace(str1, str2);
        
        System.out.println("Modified string:");
        System.out.println(result);
        input.close();
    }
}
🖥️ Program Output

Enter a string: 
Hello World
Enter the substring to remove: 
World
Enter the new substring to add: 
Java
Modified string:
Hello Java
```
---
### 📚 Lessons Learned
Learned how to replace substrings within a string using the replace() method.
Improved understanding of string manipulation and dynamic input handling.

---
### ⚡ Challenges
Ensuring that the substring to be replaced exists in the input string.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
