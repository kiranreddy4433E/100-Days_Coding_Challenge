# Day 31 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 31** of my **100 Days of Code Challenge**! Today, I created a Java program that toggles the case of each character in a given string, changing uppercase letters to lowercase and vice versa. This exercise provided valuable practice in character manipulation and conditionals.

## ✅ What I did today
- Wrote a Java program to toggle the case of each character in a string.
- Practiced using `Character` methods to identify and change the case of characters.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, Character Manipulation, Conditionals

## 📖 Problem Description
- The task is to take a string and toggle each character’s case:
  - Convert uppercase characters to lowercase.
  - Convert lowercase characters to uppercase.
  - Leave non-alphabetical characters unchanged.
  
  For example:
  - Input: `"Hello World"`
  - Output: `"hELLO wORLD"`

### Input/Output Example:
  - **Input**:
    ```
    Enter a string: Hello World
    ```
  - **Output**:
    ```
    Toggled String: hELLO wORLD
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_46 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String str = input.nextLine();
        
        StringBuilder toggledString = new StringBuilder();
        
        // Toggle the case of each character
        for (int i = 0; i < str.length(); i++) {
            char c = str.charAt(i);
            if (Character.isUpperCase(c)) {
                toggledString.append(Character.toLowerCase(c));
            } else if (Character.isLowerCase(c)) {
                toggledString.append(Character.toUpperCase(c));
            } else {
                toggledString.append(c);
            }
        }
        
        System.out.println("Toggled String: " + toggledString.toString());
        input.close();
    }
}
🖥️ Program Output

Enter a string: 
Hello World
Toggled String: hELLO wORLD
```
---
### 📚 Lessons Learned
- Practiced toggling characters using Character.isUpperCase() and Character.toLowerCase().
- Improved understanding of handling mixed character strings and non-alphabetic characters.

---
### ⚡ Challenges
Ensuring non-alphabet characters remained unchanged while toggling cases for alphabetic characters.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
