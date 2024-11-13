# Day 32 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 32** of my **100 Days of Code Challenge**! Today, I implemented a Java program to remove all vowels from a given string. This task helped me practice using regular expressions and string manipulation techniques in Java.

## ✅ What I did today
- Wrote a Java program to remove vowels (both uppercase and lowercase) from a string.
- Practiced using `replaceAll()` with regular expressions to filter out specific characters.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, Regular Expressions, Character Manipulation

## 📖 Problem Description
- The task is to remove all vowels from a given string, leaving only consonants and other characters intact. For example:
  - Input: `"Hello World"`
  - Output: `"Hll Wrld"`

### Input/Output Example:
  - **Input**:
    ```
    Enter a String: Hello World
    ```
  - **Output**:
    ```
    Hll Wrld
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_49 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a String: ");
        
        String str = input.nextLine();
        
        // Remove all vowels using regex
        String noVowels = str.replaceAll("[aeiouAEIOU]", "");
        
        System.out.println("String without vowels: " + noVowels);
        input.close();
    }
}
🖥️ Program Output

Enter a String: 
Hello World
String without vowels: Hll Wrld
```
---
### 📚 Lessons Learned
Learned how to use replaceAll() with regex to target specific characters in a string.
Practiced string manipulation for filtering out specific patterns.

---
### ⚡ Challenges
Ensuring both uppercase and lowercase vowels were removed correctly.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
