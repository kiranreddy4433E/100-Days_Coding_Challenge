# Day 67 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 67** of my **100 Days of Code Challenge**! Today, I implemented a Java program to help Arunima determine the minimum number of hits required to break a stack of bricks. The program considers Arunima's strength and allows the stack to be reversed for optimal breaking.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept multiple test cases.
  2. For each test case:
     - Input Arunima's strength (`S`) and the widths of three bricks (`W1`, `W2`, `W3`).
     - Calculate the minimum number of hits required to break all bricks, considering stack reversals.
  3. Output the number of hits for each test case.
- Practiced conditional logic and arithmetic operations to optimize stack breaking.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Conditional Statements, Arithmetic Operations, Optimization Logic

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - `S`: Strength of Arunima (maximum sum of widths she can break in one hit).
    - `W1`, `W2`, `W3`: Widths of the bricks (stacked from top to bottom).
- **Output**:
  - Print the minimum number of hits needed to break all bricks, considering stack reversals.

---

### Input/Output Example:

#### Example 1:
**Input**:
Enter a T number of test cases: 2 Enter a Test case: 1 4 2 2 2 Enter a Test case: 2 6 1 4 5



**Output**:
2 3



#### Example 2:
**Input**:
Enter a T number of test cases: 1 Enter a Test case: 1 10 3 3 3



**Output**:
1



---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_67 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Enter a T number of test cases: ");
        int T = input.nextInt();

        for (int i = 0; i < T; i++) {
            System.out.println("Enter a Test case " + (i + 1) + ": ");
            int S = input.nextInt(); // Strength of Arunima
            int W1 = input.nextInt(); // Width of brick 1
            int W2 = input.nextInt(); // Width of brick 2
            int W3 = input.nextInt(); // Width of brick 3

            // Total width of all bricks
            int totalWidth = W1 + W2 + W3;

            // Check the number of hits needed
            if (totalWidth <= S) {
                System.out.println("1"); // All bricks can be broken in one hit
            } else if (W1 + W2 <= S || W2 + W3 <= S) {
                System.out.println("2"); // Two hits needed
            } else {
                System.out.println("3"); // Three hits needed
            }
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Enter a T number of test cases: 
2
Enter a Test case 1: 
4 2 2 2
Enter a Test case 2: 
6 1 4 5
2
3
Example 2:

Enter a T number of test cases: 
1
Enter a Test case 1: 
10 3 3 3
1
```
---
## 📚 Lessons Learned
Practiced using conditional logic to evaluate multiple scenarios and edge cases.
Reinforced problem-solving strategies for optimizing operations with minimal steps.
Gained insight into handling arithmetic operations and summations efficiently.

---
## ⚡ Challenges
Managing edge cases where the bricks' arrangement affects the number of hits required.
Ensuring the program handles large values for strength and brick widths effectively.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

--- 
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
