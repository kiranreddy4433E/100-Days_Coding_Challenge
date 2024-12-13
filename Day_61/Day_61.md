# Day 61 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 61** of my **100 Days of Code Challenge**! Today, I implemented a Java program to classify chess match formats based on their time controls. This problem enhanced my understanding of conditional statements and logical operations.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept multiple test cases.
  2. For each test case, input two integers `a` and `b`, representing the time control.
  3. Determine the chess format based on the sum `a + b`:
     - **Bullet**: If `a + b < 3`
     - **Blitz**: If `3 ≤ a + b ≤ 10`
     - **Rapid**: If `11 ≤ a + b ≤ 60`
     - **Classical**: If `a + b > 60`
  4. Print the category number for each test case.
- Practiced handling multiple test cases and conditional logic.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Conditional Statements, Arithmetic Operations, Loops

## 🔗 Links to Code
- [Day 61 Code Repository](#link-to-repository): This repository contains the code solution for classifying chess match formats.

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - Two integers `a` and `b` representing the time control of the chess match.
- **Output**:
  - Print the category number corresponding to the chess format:
    - **1**: Bullet (if `a + b < 3`)
    - **2**: Blitz (if `3 ≤ a + b ≤ 10`)
    - **3**: Rapid (if `11 ≤ a + b ≤ 60`)
    - **4**: Classical (if `a + b > 60`)

---

### Input/Output Example:

#### Example 1:
**Input**:
Number of test cases: 2 Enter two integers (a and b) for test case 1: 1 1 Enter two integers (a and b) for test case 2: 15 20

makefile
Copy code

**Output**:
1 3

graphql
Copy code

#### Example 2:
**Input**:
Number of test cases: 3 Enter two integers (a and b) for test case 1: 0 3 Enter two integers (a and b) for test case 2: 5 3 Enter two integers (a and b) for test case 3: 40 25

makefile
Copy code

**Output**:
2 2 4

csharp
Copy code

---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_61 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Number of test cases (T): ");
        int T = input.nextInt();

        for (int i = 0; i < T; i++) {
            System.out.println("Enter two integers (a and b) for test case " + (i + 1) + ":");
            int a = input.nextInt();
            int b = input.nextInt();
            int add = a + b;

            if (add < 3) {
                System.out.println("1"); // Bullet
            } else if (add >= 3 && add <= 10) {
                System.out.println("2"); // Blitz
            } else if (add >= 11 && add <= 60) {
                System.out.println("3"); // Rapid
            } else {
                System.out.println("4"); // Classical
            }
        }
        input.close();
    }
}
🖥️ Program Output
Example 1:
bash
Copy code
Number of test cases: 
2
Enter two integers (a and b) for test case 1: 
1 1
Enter two integers (a and b) for test case 2: 
15 20
1
3
Example 2:
bash
Copy code
Number of test cases: 
3
Enter two integers (a and b) for test case 1: 
0 3
Enter two integers (a and b) for test case 2: 
5 3
Enter two integers (a and b) for test case 3: 
40 25
2
2
4
📚 Lessons Learned
Practiced conditional statements to classify values into specific ranges.
Enhanced skills in handling multiple test cases and formatting outputs.
Reinforced arithmetic operations and comparisons in Java.
⚡ Challenges
Handling edge cases where a + b is at the boundary of two categories (e.g., 3, 10, 11, 60).
📬 Connect with me
Email: kiranreddy4746@gmail.com
LinkedIn: Chandra Kiran Reddy Reddycharla
Twitter: @kiran4746
100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.# Day 61 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 61** of my **100 Days of Code Challenge**! Today, I implemented a Java program to classify chess match formats based on their time controls. This problem enhanced my understanding of conditional statements and logical operations.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept multiple test cases.
  2. For each test case, input two integers `a` and `b`, representing the time control.
  3. Determine the chess format based on the sum `a + b`:
     - **Bullet**: If `a + b < 3`
     - **Blitz**: If `3 ≤ a + b ≤ 10`
     - **Rapid**: If `11 ≤ a + b ≤ 60`
     - **Classical**: If `a + b > 60`
  4. Print the category number for each test case.
- Practiced handling multiple test cases and conditional logic.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Conditional Statements, Arithmetic Operations, Loops

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - Two integers `a` and `b` representing the time control of the chess match.
- **Output**:
  - Print the category number corresponding to the chess format:
    - **1**: Bullet (if `a + b < 3`)
    - **2**: Blitz (if `3 ≤ a + b ≤ 10`)
    - **3**: Rapid (if `11 ≤ a + b ≤ 60`)
    - **4**: Classical (if `a + b > 60`)

---

### Input/Output Example:

#### Example 1:
**Input**:
Number of test cases: 2 Enter two integers (a and b) for test case 1: 1 1 Enter two integers (a and b) for test case 2: 15 20


**Output**:
1 3

graphql
Copy code

#### Example 2:
**Input**:
Number of test cases: 3 Enter two integers (a and b) for test case 1: 0 3 Enter two integers (a and b) for test case 2: 5 3 Enter two integers (a and b) for test case 3: 40 25


**Output**:
2 2 4


---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_61 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Number of test cases (T): ");
        int T = input.nextInt();

        for (int i = 0; i < T; i++) {
            System.out.println("Enter two integers (a and b) for test case " + (i + 1) + ":");
            int a = input.nextInt();
            int b = input.nextInt();
            int add = a + b;

            if (add < 3) {
                System.out.println("1"); // Bullet
            } else if (add >= 3 && add <= 10) {
                System.out.println("2"); // Blitz
            } else if (add >= 11 && add <= 60) {
                System.out.println("3"); // Rapid
            } else {
                System.out.println("4"); // Classical
            }
        }
        input.close();
    }
}
🖥️ Program Output
Example 1:

Number of test cases: 
2
Enter two integers (a and b) for test case 1: 
1 1
Enter two integers (a and b) for test case 2: 
15 20
1
3
Example 2:

Number of test cases: 
3
Enter two integers (a and b) for test case 1: 
0 3
Enter two integers (a and b) for test case 2: 
5 3
Enter two integers (a and b) for test case 3: 
40 25
2
2
4
```
---
## 📚 Lessons Learned
Practiced conditional statements to classify values into specific ranges.
Enhanced skills in handling multiple test cases and formatting outputs.
Reinforced arithmetic operations and comparisons in Java.

---
## ⚡ Challenges
Handling edge cases where a + b is at the boundary of two categories (e.g., 3, 10, 11, 60).

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
