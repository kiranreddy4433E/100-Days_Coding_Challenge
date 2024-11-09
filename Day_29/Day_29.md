# Day 29 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 29** of my **100 Days of Code Challenge**! Today, I implemented a Java program to concatenate two user-input strings. This exercise helped me work with string operations and user input handling in Java.

## ✅ What I did today
- Wrote a Java program to concatenate two strings.
- Practiced handling user input and performing basic string operations.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, Concatenation, User Input

## 📖 Problem Description
- The task is to take two strings from the user and concatenate them. For example:
  - Input 1: `"Hello"`
  - Input 2: `"World"`
  - Output: `"HelloWorld"`

### Input/Output Example:
  - **Input**:
    ```
    Enter string 1: Hello
    Enter string 2: World
    ```
  - **Output**:
    ```
    HelloWorld
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_41 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        System.out.print("Enter string 1: ");
        String str1 = input.nextLine();
        
        System.out.print("Enter string 2: ");
        String str2 = input.nextLine();
        
        // Concatenate and print the result
        System.out.println("Concatenated String: " + str1 + str2);

        input.close();
    }
}
🖥️ Program Output

Enter string 1: 
Hello
Enter string 2: 
World
Concatenated String: HelloWorld
```
---
### 📚 Lessons Learned
- Practiced using + for string concatenation in Java.
- Improved skills in handling and managing user input with Scanner.

---
### ⚡ Challenges
Ensuring both strings were entered correctly to avoid unexpected outputs.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
