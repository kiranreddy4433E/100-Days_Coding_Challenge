# Day 39 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 39** of my **100 Days of Code Challenge**! Today, I implemented a Java program to check if two strings are **anagrams**. This task strengthened my skills in string manipulation, sorting, and comparison.

## ✅ What I did today
- Wrote a Java program to check if two strings are anagrams of each other.
- Practiced converting strings to character arrays and using `Arrays.sort()` for comparison.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, Character Arrays, Sorting, Loops

## 📖 Problem Description
- Two strings are considered anagrams if they can be rearranged to form the same word. The task is to determine if two input strings are anagrams of each other. For example:
  - Input: `"listen"` and `"silent"`
  - Output: `"It's an anagram"`

### Input/Output Example:
  - **Input**:
    ```
    Enter the first string: listen
    Enter the second string: silent
    ```
  - **Output**:
    ```
    It's an anagram
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;
import java.util.Arrays;

public class pro_58 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        System.out.print("Enter the first string: ");
        String str = input.nextLine();
        
        System.out.print("Enter the second string: ");
        String str1 = input.nextLine();
        
        // If lengths differ, they cannot be anagrams
        if (str.length() != str1.length()) {
            System.out.println("It's not an anagram");
            return;
        }
        
        // Convert strings to character arrays
        char[] ch = str.toCharArray();
        char[] ch1 = str1.toCharArray();
        
        // Sort both arrays
        Arrays.sort(ch);
        Arrays.sort(ch1);
        
        // Compare sorted arrays
        for (int i = 0; i < ch.length; i++) {
            if (ch[i] != ch1[i]) {
                System.out.println("It's not an anagram");
                return;
            }
        }
        
        System.out.println("It's an anagram");
        input.close();
    }
}
🖥️ Program Output

Enter the first string: listen
Enter the second string: silent
It's an anagram
```
---
### 📚 Lessons Learned
Practiced checking if two strings are anagrams by comparing sorted character arrays.
Reinforced understanding of Arrays.sort() and its role in simplifying comparison tasks.

---
### ⚡ Challenges
Ensuring proper handling of strings with varying lengths or special characters.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
