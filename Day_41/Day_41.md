# Day 41 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 41** of my **100 Days of Code Challenge**! Today, I implemented a Java program to determine if a string matches a pattern that includes **wildcard characters**. This task strengthened my skills in string manipulation and pattern matching.

## ✅ What I did today
- Wrote a Java program to check if two strings match where one string contains wildcard characters (`*` and `?`).
  - `*`: Matches any sequence of characters, including an empty sequence.
  - `?`: Matches any single character.
- Practiced using two-pointer techniques to handle the matching logic efficiently.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Strings, Pattern Matching, Wildcard Characters

## 📖 Problem Description
- The task is to determine if a string matches a pattern with wildcard characters:
  - `*` matches any sequence of characters (or none).
  - `?` matches exactly one character.
- For example:
  - String: `"abcdef"`
  - Pattern: `"a*c?f"`
  - Result: `"The string matches the pattern."`

### Input/Output Example:
  - **Input**:
    ```
    Enter the string: abcdef
    Enter the pattern: a*c?f
    ```
  - **Output**:
    ```
    The string matches the pattern.
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class day_41 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter the string: ");
        String str = input.nextLine();

        System.out.print("Enter the pattern: ");
        String pattern = input.nextLine();

        int s = 0; 
        int p = 0; 
        int starIdx = -1; 
        int matchIdx = -1; 

        // Match the string with the pattern
        while (s < str.length()) {
            if (p < pattern.length() && (pattern.charAt(p) == '?' || str.charAt(s) == pattern.charAt(p))) {
                s++;
                p++;
            } 
            else if (p < pattern.length() && pattern.charAt(p) == '*') {
                starIdx = p;
                matchIdx = s;
                p++;
            } 
            else if (starIdx != -1) {
                p = starIdx + 1;
                matchIdx++;
                s = matchIdx;
            } 
            else {
                System.out.println("The string does not match the pattern.");
                input.close();
                return;
            }
        }

        while (p < pattern.length() && pattern.charAt(p) == '*') {
            p++;
        }

        if (p == pattern.length()) {
            System.out.println("The string matches the pattern.");
        } else {
            System.out.println("The string does not match the pattern.");
        }

        input.close();
    }
}
🖥️ Program Output

Enter the string: 
abcdef
Enter the pattern: 
a*c?f
The string matches the pattern.
```
---
### 📚 Lessons Learned
Learned how to handle pattern matching using wildcard characters (* and ?).
Improved my understanding of efficient string traversal techniques.

---
### ⚡ Challenges
Ensuring that * handled sequences of varying lengths correctly without skipping valid matches.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
