# Day 63 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 63** of my **100 Days of Code Challenge**! Today, I implemented a Java program to validate whether the weight recorded at the end of the lockdown is within a scientifically plausible range based on monthly weight gain limits.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept multiple test cases.
  2. For each test case, input the initial weight (`w1`), final weight (`w2`), number of months (`M`), and the minimum (`x1`) and maximum (`x2`) monthly weight gain.
  3. Determine if the recorded final weight (`w2`) is plausible based on the formula:
     \[
     \text{minWeight} = w1 + (x1 \times M), \quad \text{maxWeight} = w1 + (x2 \times M)
     \]
     and check if:
     \[
     \text{minWeight} \leq w2 \leq \text{maxWeight}
     \]
  4. Print `"1"` if the result is plausible, otherwise print `"0"`.
- Practiced using conditional statements, loops, and arithmetic operations.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Loops, Conditional Statements, Arithmetic Operations

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - `w1`: Initial weight in kg.
    - `w2`: Final weight in kg (measured at home scale).
    - `M`: Number of months of weight gain.
    - `x1`: Minimum weight gain per month in kg.
    - `x2`: Maximum weight gain per month in kg.
- **Output**:
  - Print `"1"` if the final weight is plausible based on the input parameters.
  - Print `"0"` otherwise.

---

### Input/Output Example:

#### Example 1:
**Input**:
Number of test cases: 2 Enter w1, w2, M, x1, and x2 for test case 1: 50 56 2 2 4 Enter w1, w2, M, x1, and x2 for test case 2: 45 50 3 1 2


**Output**:
1 1


#### Example 2:
**Input**:
Number of test cases: 1 Enter w1, w2, M, x1, and x2 for test case 1: 60 80 5 3 4


**Output**:
0


---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_63 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Number of test cases (T): ");
        int T = input.nextInt();

        for (int i = 0; i < T; i++) {
            System.out.println("Enter w1 (initial weight), w2 (final weight), M (months), x1 (min gain), and x2 (max gain) for test case " + (i + 1) + ":");
            int W1 = input.nextInt();
            int W2 = input.nextInt();
            int M = input.nextInt();
            int X1 = input.nextInt();
            int X2 = input.nextInt();

            int minWeight = W1 + (X1 * M);
            int maxWeight = W1 + (X2 * M);

            if (W2 >= minWeight && W2 <= maxWeight) {
                System.out.println("1"); // Weight is plausible
            } else {
                System.out.println("0"); // Weight is not plausible
            }
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Number of test cases: 
2
Enter w1, w2, M, x1, and x2 for test case 1: 
50 56 2 2 4
Enter w1, w2, M, x1, and x2 for test case 2: 
45 50 3 1 2
1
1
Example 2:

Number of test cases: 
1
Enter w1, w2, M, x1, and x2 for test case 1: 
60 80 5 3 4
0
```
---
## 📚 Lessons Learned
Learned to use mathematical formulas and logical checks to validate input data.
Practiced handling multiple test cases and using loops efficiently.
Reinforced the concept of range checking in conditional statements.

---
## ⚡ Challenges
Managing edge cases where:
x1 and x2 values are very close, resulting in a narrow range for w2.
M = 0, where the weight cannot change.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
