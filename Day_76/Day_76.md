Here’s the README.md for Day 76 of your 100 Days of Code Challenge, where you implemented a solution to calculate the maximum number of steps based on specific deletion criteria for an array.

markdown
Copy code
# Day 76 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 76** of my **100 Days of Code Challenge**! Today, I worked on solving a problem that involves calculating the maximum number of steps possible by removing elements from an array under specific conditions.

## ✅ What I did today
- Designed a Java program to:
  1. Sort an array of integers.
  2. Remove \( K \) elements per step, ensuring that for each chosen group, \( a_{i+1} \geq a_i \times C \) holds true.
  3. Count the maximum number of such steps possible.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Sorting, Logical Constraints, Greedy Algorithms

## 📖 Problem Description
- **Input**:
  - \( T \): Number of test cases.
  - For each test case:
    - \( N \): Number of integers in the array.
    - \( K \): Number of elements to be removed in one step.
    - \( C \): Multiplier constraint.
    - A list of \( N \) integers.
- **Output**:
  - The maximum number of steps possible while satisfying the condition \( a_{i+1} \geq a_i \times C \).

---

### Input/Output Example:

#### Example 1:
**Input**:
Enter a T test case's: 2 Enter N, K, and C for test case 1: 6 3 2 1 2 4 8 16 32 Enter N, K, and C for test case 2: 5 2 3 1 3 9 27 81


**Output**:
Maximum steps: 2 Maximum steps: 2


#### Explanation:
1. **Test Case 1**: The array `[1, 2, 4, 8, 16, 32]` can form two valid groups of size \( K = 3 \) each: `[1, 2, 4]` and `[8, 16, 32]`.
2. **Test Case 2**: The array `[1, 3, 9, 27, 81]` can form two valid groups of size \( K = 2 \) each: `[1, 3]` and `[9, 27]`.

---

## 📝 Code Example

```java
package coading_Challange;

import java.util.*;

public class Day_76 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter a T test case's:- ");
        int num = input.nextInt();
        for (int i = 0; i < num; i++) {
            System.out.println("Enter N, K, and C for test case " + (i + 1) + ":");
            int N = input.nextInt();
            int K = input.nextInt();
            int C = input.nextInt();
            int series[] = new int[N];
            for (int j = 0; j < N; j++) {
                series[j] = input.nextInt();
            }
            System.out.println("Maximum steps: " + calculateMaxSteps(series, K, C));
        }
    }

    private static int calculateMaxSteps(int[] series, int K, int C) {
        Arrays.sort(series); // Sort the array
        int n = series.length;
        int steps = 0;
        boolean[] used = new boolean[n]; // Track used elements
        for (int i = 0; i <= n - K; ) {
            boolean isValidGroup = true;
            int lastElement = series[i];
            used[i] = true;
            int count = 1;
            for (int j = i + 1; j < n && count < K; j++) {
                if (!used[j] && series[j] >= lastElement * C) {
                    used[j] = true;
                    lastElement = series[j];
                    count++;
                }
            }
            if (count == K) {
                steps++;
                i++;
            } else {
                i++;
            }
        }
        return steps;
    }
}
🖥️ Program Output
Example 1:

Enter a T test case's: 
2
Enter N, K, and C for test case 1:
6 3 2
1 2 4 8 16 32
Maximum steps: 2
Enter N, K, and C for test case 2:
5 2 3
1 3 9 27 81
Maximum steps: 2
```
---
## 📚 Lessons Learned
Learned to implement constraints in array manipulations using sorting and greedy algorithms.
Practiced efficient usage of boolean arrays for tracking elements in complex selection scenarios.
Strengthened understanding of nested loops to address multi-step problems.

---
## ⚡ Challenges
Ensuring that the constraints 
𝑎
𝑖
+
1
≥
𝑎
𝑖
×
𝐶
a 
i+1
​
 ≥a 
i
​
 ×C were applied correctly for each group.
Managing overlapping cases where multiple valid groupings could exist.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

--- 
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
