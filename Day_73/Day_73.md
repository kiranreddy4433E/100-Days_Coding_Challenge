# Day 73 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 73** of my **100 Days of Code Challenge**! Today, I worked on solving a problem that involves identifying the **longest boring substring** in a given string. A substring is defined as boring if all the characters in it are the same and it occurs more than once in the string.

## ✅ What I did today
- Implemented a Java program to:
  1. Accept a string and determine its **longest boring substring** that occurs more than once.
  2. Calculate the length of such a substring.
- Practiced string manipulation and substring matching techniques.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** String Manipulation, Substring Matching, Nested Loops

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - `N`: Length of the string.
    - `S`: A string of length `N` consisting of lowercase English alphabets.
- **Output**:
  - The length of the longest boring substring of `S` that occurs more than once. If no such substring exists, return `0`.

---

### Input/Output Example:

#### Example 1:
**Input**:
Enter T test case: 2 5 aabbb 7 aaabbba


**Output**:
3 3


---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_73 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter T test case:- ");
        int num = input.nextInt();
        for (int i = 0; i < num; i++) {
            int N = input.nextInt();
            input.nextLine();
            String S = input.nextLine();
            int maxLength = findLongestBoringSubstring(S);
            System.out.println(maxLength);
        }
    }

    private static int findLongestBoringSubstring(String S) {
        int N = S.length();
        int maxLength = 0;
        for (int i = 0; i < N; i++) {
            int count = 1;
            while (i + 1 < N && S.charAt(i) == S.charAt(i + 1)) {
                count++;
                i++;
            }
            String boringSubstring = S.substring(i - count + 1, i + 1);
            if (S.indexOf(boringSubstring, i + 1) != -1) {
                maxLength = Math.max(maxLength, count);
            }
        }
        return maxLength;
    }
}
🖥️ Program Output
Example 1:

Enter T test case: 
2
Enter N and S for test case 1: 
5
aabbb
3
Enter N and S for test case 2: 
7
aaabbba
3
Example 2:

Enter T test case: 
1
Enter N and S for test case 1: 
8
abababab
0
```
---
## 📚 Lessons Learned
Practiced efficient substring matching using indexOf and substring extraction techniques.
Understood the importance of tracking substring occurrences for repetitive patterns.
Gained a better understanding of managing nested loops for character comparisons.

---
## ⚡ Challenges
Handling edge cases where there are no repetitive substrings in the input string.
Ensuring performance efficiency for strings with larger lengths.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
