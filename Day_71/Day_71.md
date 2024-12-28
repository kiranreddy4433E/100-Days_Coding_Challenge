# Day 71 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 71** of my **100 Days of Code Challenge**! Today, I implemented a program to determine the number of students in a class who will boast about their scores. This problem involves comparing the count of students scoring less than or equal to a given score against those scoring higher.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept multiple test cases.
  2. For each test case:
     - Input scores of students in a class.
     - Identify students who will boast if their score meets the boasting condition.
  3. Output the number of students who boast for each test case.
- Practiced sorting and counting techniques for problem-solving.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Sorting, Counting Elements, Conditional Logic

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - `N`: Number of students in the class.
    - An array of `N` integers, representing the scores of the students.
- **Output**:
  - Number of students who boast for each test case.

---

### Input/Output Example:

#### Example 1:
**Input**:
Enter the number of test cases: 1 Enter the number of students for test case 1: 5 Enter the scores of the students: 1 2 3 4 5



**Output**:
Number of students who will boast in test case 1: 3



#### Example 2:
**Input**:
Enter the number of test cases: 1 Enter the number of students for test case 1: 4 Enter the scores of the students: 10 20 10 20



**Output**:
Number of students who will boast in test case 1: 2



---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;
import java.util.Arrays;

public class Day_71 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter the number of test cases:");
        int T = input.nextInt();

        for (int t = 0; t < T; t++) {
            System.out.println("Enter the number of students for test case " + (t + 1) + ":");
            int numStudents = input.nextInt();
            int[] scores = new int[numStudents];
            System.out.println("Enter the scores of the students:");
            for (int i = 0; i < numStudents; i++) {
                scores[i] = input.nextInt();
            }

            // Sort the scores
            Arrays.sort(scores);

            int boastCount = 0;
            for (int i = 0; i < numStudents; ) {
                int currentScore = scores[i];
                int count = 0;
                while (i < numStudents && scores[i] == currentScore) {
                    count++;
                    i++;
                }

                int studentsWithLessOrEqual = i;
                int studentsWithMore = numStudents - studentsWithLessOrEqual;

                if (studentsWithLessOrEqual > studentsWithMore) {
                    boastCount += count;
                }
            }

            System.out.println("Number of students who will boast in test case " + (t + 1) + ": " + boastCount);
        }
        input.close();
    }
}
🖥️ Program Output
Example 1:

Enter the number of test cases:
1
Enter the number of students for test case 1:
5
Enter the scores of the students:
1 2 3 4 5
Number of students who will boast in test case 1: 3
Example 2:

Enter the number of test cases:
1
Enter the number of students for test case 1:
4
Enter the scores of the students:
10 20 10 20
Number of students who will boast in test case 1: 2
```
---
## 📚 Lessons Learned
Enhanced problem-solving skills by breaking down the boasting condition into smaller steps.
Practiced using sorting techniques to simplify comparisons in the dataset.
Reinforced counting and loop-based traversal for analyzing arrays.

---
## ⚡ Challenges
Ensuring that the counting mechanism correctly handles duplicate scores in the array.
Managing edge cases where all students have the same score or highly skewed distributions.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
