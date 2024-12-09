# Day 57 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 57** of my **100 Days of Code Challenge**! Today, I implemented a Java program to determine whether a student passes or fails a test based on the scoring system of correct and incorrect answers. This problem was engaging and helped me practice handling multiple test cases and arithmetic operations.

## ✅ What I did today
- Wrote a Java program to:
  1. Input the total number of test cases.
  2. For each test case, calculate the total score based on correct and incorrect answers.
  3. Determine if the student passes or fails based on the minimum passing marks.
- Practiced logical conditions, loops, and input handling.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Conditional Statements, Loops, Arithmetic Operations

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - `N`: Total number of questions.
    - `X`: Number of correctly answered questions.
    - `P`: Minimum marks required to pass.
- **Scoring System**:
  - Correct answer: `+3` marks.
  - Incorrect answer: `−1` mark.
- **Output**:
  - Print `"PASS"` if the total marks are at least `P`, otherwise print `"FAIL"`.

---

### Input/Output Example:

#### Example 1:
**Input**:
Number of test cases: 2 Enter N, X, and P for test case 1: 5 3 7 Enter N, X, and P for test case 2: 4 2 5



**Output**:
PASS FAIL



#### Example 2:
**Input**:
Number of test cases: 1 Enter N, X, and P for test case 1: 6 4 10


**Output**:
PASS

java


---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_57 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Number of test cases: ");
        int T = input.nextInt();

        for (int i = 0; i < T; i++) {
            System.out.println("Enter N, X, and P for test case " + (i + 1) + ":");
            int N = input.nextInt();
            int X = input.nextInt();
            int P = input.nextInt();

            int marks_CQuestions = 3 * X; // Marks for correct answers
            int marks_Wanswers = -(N - X); // Marks for incorrect answers
            int total_Marks = marks_CQuestions + marks_Wanswers;

            if (total_Marks >= P) {
                System.out.println("PASS");
            } else {
                System.out.println("FAIL");
            }
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Number of test cases: 
2
Enter N, X, and P for test case 1: 
5 3 7
Enter N, X, and P for test case 2: 
4 2 5
PASS
FAIL
Example 2:

Number of test cases: 
1
Enter N, X, and P for test case 1: 
6 4 10
PASS
```
---
## 📚 Lessons Learned
Reinforced the use of loops to handle multiple test cases.
Practiced basic arithmetic operations and conditional logic.
Enhanced skills in designing user-friendly input/output prompts for competitive programming.

---
## ⚡ Challenges
Ensuring accurate calculation of scores for negative marks due to incorrect answers.
Handling edge cases where the number of correct answers is very low or very high.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
