# Day 58 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 58** of my **100 Days of Code Challenge**! Today, I implemented a Java program to calculate how much extra water can be added to a bucket without overflowing. This problem helped me practice input handling, arithmetic operations, and logic implementation for multiple test cases.

## ✅ What I did today
- Wrote a Java program to:
  1. Input the number of test cases.
  2. For each test case, input the capacity of the bucket (`K`) and the current amount of water (`X`).
  3. Calculate the maximum extra water that can be added without exceeding the bucket's capacity.
- Practiced handling multiple test cases and arithmetic operations.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arithmetic Operations, Loops, Input Handling

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - `K`: Total capacity of the bucket in liters.
    - `X`: Current amount of water in liters.
- **Output**:
  - For each test case, print the maximum extra water in liters that can be added to the bucket without overflowing.

---

### Input/Output Example:

#### Example 1:
**Input**:
Number of test cases: 2 Enter K and X for test case 1: 10 4 Enter K and X for test case 2: 15 12



**Output**:
Remaining liters of water: 6 Remaining liters of water: 3



#### Example 2:
**Input**:
Number of test cases: 1 Enter K and X for test case 1: 20 8



**Output**:
Remaining liters of water: 12


---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_58 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Number of test cases (T): ");
        int num = input.nextInt();

        for (int i = 0; i < num; i++) {
            System.out.println("Enter K and X liters of water for test case " + (i + 1) + ": ");
            int K = input.nextInt();
            int X = input.nextInt();

            int remaining = K - X;
            System.out.println("Remaining liters of water: " + remaining);
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Number of test cases: 
2
Enter K and X liters of water for test case 1: 
10 4
Enter K and X liters of water for test case 2: 
15 12
Remaining liters of water: 6
Remaining liters of water: 3
Example 2:

Number of test cases: 
1
Enter K and X liters of water for test case 1: 
20 8
Remaining liters of water: 12
```
---
## 📚 Lessons Learned
Practiced logical operations for determining the difference between two values.
Improved input/output handling for multiple test cases in a single run.

---
## ⚡ Challenges
Ensuring accurate calculations when X is equal to or greater than K (resulting in 0 or negative values).

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

--- 
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
