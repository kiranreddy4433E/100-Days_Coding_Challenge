# Day 38 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 38** of my **100 Days of Code Challenge**! Today, I implemented a Java program to find and print all **non-repeating characters** in a given string. This exercise helped me understand how to use `HashMap` for character frequency analysis and filtering.

## ✅ What I did today
- Wrote a Java program to identify and print all non-repeating characters from a string.
- Practiced using `HashMap` to track and count character occurrences efficiently.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, HashMap, Loops

## 📖 Problem Description
- The task is to identify all characters in a string that appear only once (non-repeating). For example:
  - Input: `"swiss"`
  - Output:
    ```
    w
    i
    ```

### Input/Output Example:
  - **Input**:
    ```
    Enter a String: swiss
    ```
  - **Output**:
    ```
    w
    i
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;
import java.util.HashMap;

public class pro_57 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a String: ");
        
        String str = input.nextLine();
        HashMap<Character, Integer> frequencyMap = new HashMap<>();
        
        // Count character frequencies
        for (int i = 0; i < str.length(); i++) {
            char ch = str.charAt(i);
            frequencyMap.put(ch, frequencyMap.getOrDefault(ch, 0) + 1);
        }
        
        // Print non-repeating characters
        System.out.println("Non-repeating characters:");
        for (Character key : frequencyMap.keySet()) {
            if (frequencyMap.get(key) == 1) {
                System.out.println(key);
            }
        }
        
        input.close();
    }
}
🖥️ Program Output

Enter a String: 
swiss
Non-repeating characters:
w
i
```
---
### 📚 Lessons Learned
Practiced character frequency analysis using HashMap.
Learned to filter and identify elements in a collection based on specific conditions.

---
### ⚡ Challenges
Ensuring case sensitivity was handled correctly (e.g., distinguishing between S and s if required).

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
