# Day 33 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 33** of my **100 Days of Code Challenge**! Today, I implemented a Java program to check if a given string is a **palindrome**. This task helped me practice string manipulation and the use of pointers to compare characters.

## ✅ What I did today
- Wrote a Java program to check if a string reads the same forwards and backwards.
- Practiced using two-pointer technique to compare characters efficiently.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, Two-Pointer Technique, Conditionals

## 📖 Problem Description
- The task is to check if a string is a palindrome (a word or phrase that reads the same forwards and backwards). For example:
  - Input: `"madam"`
  - Output: `"It's a palindrome: madam"`
  
  - Input: `"hello"`
  - Output: `"It's not a palindrome: hello"`

### Input/Output Example:
  - **Input**:
    ```
    Enter a string: madam
    ```
  - **Output**:
    ```
    It's a palindrome: madam
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_50 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a string: ");
        
        String str = input.nextLine();
        boolean isPalindrome = true;
        int left = 0;
        int right = str.length() - 1;
        
        // Check characters from both ends
        while (left < right) {
            if (str.charAt(left) != str.charAt(right)) {
                isPalindrome = false;
                break;
            }
            left++;
            right--;
        }
        
        if (isPalindrome) {
            System.out.println("It's a palindrome: " + str);
        } else {
            System.out.println("It's not a palindrome: " + str);
        }
        
        input.close();
    }
}
🖥️ Program Output

Enter a string: 
madam
It's a palindrome: madam
```
---
### 📚 Lessons Learned
Practiced checking palindromes using the two-pointer technique for efficiency.
Reinforced understanding of character comparison and handling strings with loops.

---
### ⚡ Challenges
Ensuring correct handling of strings with different cases and characters was key for accurate comparison.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
