# Day 60 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 60** of my **100 Days of Code Challenge**! Today, I implemented a Java program to determine if the weather in Magicland is **Good** or **Not Good** based on the number of sunny and rainy days in a week. A week is considered **Good** if the number of sunny days is strictly greater than the number of rainy days.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept multiple test cases of weekly weather data.
  2. Calculate the count of sunny days (`1`) and rainy days (`0`).
  3. Determine if the week qualifies as **Good** based on the condition.
- Practiced array operations and logical comparisons.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Loops, Conditional Statements

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - `7 integers` representing the weather for each day of the week:
      - `1` for a sunny day.
      - `0` for a rainy day.
- **Output**:
  - Print `"Yes"` if the week is Good (sunny days > rainy days).
  - Print `"No"` otherwise.

---

### Input/Output Example:

#### Example 1:
**Input**:
Number of test cases: 1 Enter 7 integers for test case 1: 1 1 1 1 1 0 0



**Output**:
5 Yes



#### Example 2:
**Input**:
Number of test cases: 2 Enter 7 integers for test case 1: 1 0 1 0 1 0 1 Enter 7 integers for test case 2: 0 0 0 0 0 0 1



**Output**:
4 Yes 1 No



---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_60 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Number of test cases (T): ");
        int T = input.nextInt();
        for (int t = 0; t < T; t++) {
            System.out.println("Enter 7 integers for test case " + (t + 1) + ":");
            int[] A = new int[7];
            int CountOne = 0;

            for (int i = 0; i < 7; i++) {
                A[i] = input.nextInt();
                CountOne += A[i];
            }

            int CountZero = 7 - CountOne;

            if (CountOne > CountZero) {
                System.out.println("Yes");
            } else {
                System.out.println("No");
            }
        }
        input.close();
    }
}
🖥️ Program Output
Example 1:

Number of test cases: 
1
Enter 7 integers for test case 1: 
1 1 1 1 1 0 0
5
Yes
Example 2:

Number of test cases: 
2
Enter 7 integers for test case 1: 
1 0 1 0 1 0 1
Enter 7 integers for test case 2: 
0 0 0 0 0 0 1
4
Yes
1
No
```
---
## 📚 Lessons Learned
Practiced counting occurrences in an array and calculating differences.
Enhanced understanding of logical comparisons and conditional statements.
Improved skills in handling multiple test cases efficiently.

---
## ⚡ Challenges
Handling edge cases, such as all days being sunny ([1, 1, 1, 1, 1, 1, 1]) or rainy ([0, 0, 0, 0, 0, 0, 0]).
Ensuring clear and concise output for each test case.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
