# Day 36 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 36** of my **100 Days of Code Challenge**! Today, I created a Java program to capitalize the **first and last letters** of each word in a string. This exercise helped me work with strings, character manipulation, and conditionals.

## ✅ What I did today
- Wrote a Java program to capitalize the first and last letters of a string or word.
- Practiced handling edge cases such as empty strings and single-character inputs.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, Character Manipulation, Conditionals

## 📖 Problem Description
- The task is to take a string and capitalize the first and last letters while keeping the rest of the string unchanged. If the string contains only one letter, it is fully capitalized. For example:
  - Input: `"hello"`
  - Output: `"HellO"`

### Input/Output Example:
  - **Input**:
    ```
    Enter a String: hello
    ```
  - **Output**:
    ```
    Modified String: HellO
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_53 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a String: ");
        
        String str = input.nextLine();

        if (str.isEmpty()) {
            System.out.println("The string is empty.");
        } else if (str.length() == 1) {
            System.out.println(str.toUpperCase());
        } else {
            char first = Character.toUpperCase(str.charAt(0));
            char last = Character.toUpperCase(str.charAt(str.length() - 1));
            
            String result = first + str.substring(1, str.length() - 1) + last;
            System.out.println("Modified String: " + result);
        }
        
        input.close();
    }
}
🖥️ Program Output

Enter a String: 
hello
Modified String: HellO
```
---
### 📚 Lessons Learned
Learned how to capitalize specific characters in a string using Character.toUpperCase().
Practiced handling edge cases such as empty strings and single-character strings.

---
### ⚡ Challenges
Ensuring correct handling of edge cases, such as strings with only one character or no characters.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
