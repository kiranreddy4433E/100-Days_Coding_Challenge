# Day 37 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 37** of my **100 Days of Code Challenge**! Today, I implemented a Java program to calculate the **frequency of each character** in a given string. This exercise helped me learn how to use `HashMap` for counting and tracking occurrences.

## ✅ What I did today
- Wrote a Java program to compute the frequency of characters in a string.
- Practiced using `HashMap` for storing and retrieving character counts.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, HashMap, Loops

## 📖 Problem Description
- The task is to take a string input from the user and calculate the frequency of each character. For example:
  - Input: `"hello"`
  - Output:
    ```
    The frequency of h is 1
    The frequency of e is 1
    The frequency of l is 2
    The frequency of o is 1
    ```

### Input/Output Example:
  - **Input**:
    ```
    Enter a String: hello
    ```
  - **Output**:
    ```
    The frequency of h is 1
    The frequency of e is 1
    The frequency of l is 2
    The frequency of o is 1
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
        
        // Display frequencies
        System.out.println("Character frequencies:");
        for (Character key : frequencyMap.keySet()) {
            System.out.println("The frequency of " + key + " is " + frequencyMap.get(key));
        }
        
        input.close();
    }
}
🖥️ Program Output

Enter a String: 
hello
Character frequencies:
The frequency of h is 1
The frequency of e is 1
The frequency of l is 2
The frequency of o is 1
```
---
### 📚 Lessons Learned
Learned how to use HashMap for counting occurrences of elements.
Practiced string iteration and handling character frequencies efficiently.

---
### ⚡ Challenges
Ensuring case sensitivity was handled correctly (e.g., distinguishing between H and h if required).

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
