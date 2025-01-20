# Day 89 of 100 - 100 Days of Code Challenge

## 📝 Problem: Maximum Steps with Group Deletion

You are given \( N \) integers. In each step, you can choose \( K \) of the remaining numbers and delete them if the following condition holds:

- Let the \( K \) numbers you've chosen be \( a_1, a_2, a_3, \ldots, a_K \) in sorted order. Then, for each \( i \leq K - 1 \):
  \[
  a_{i+1} \geq a_i \times C
  \]

You need to calculate the **maximum number of steps** you can perform under the above condition.

---

## 🔗 Input and Output Format

### Input:
1. The first line contains \( T \), the number of test cases.
2. For each test case:
   - The first line contains three integers \( N \) (size of the array), \( K \) (group size), and \( C \) (condition factor).
   - The second line contains \( N \) integers representing the array.

### Output:
For each test case, output the **maximum number of steps** that can be performed.

---

## 💡 Approach

1. **Sorting the Array**:
   - First, sort the array in **non-decreasing order**.

2. **Binary Search for Steps**:
   - Perform a **binary search** to find the maximum number of steps.
   - Check if it is possible to form \( steps \) groups of size \( K \) that satisfy the condition.

3. **Validate Groups**:
   - Iterate through the array to form \( K \) groups of \( steps \) size each.
   - Ensure that the condition \( a_{i+1} \geq a_i \times C \) holds for all groups.

4. **Output the Result**:
   - Print the maximum steps that can be performed for each test case.

---

## 🚀 Code Implementation

```java
package coading_Challange;

import java.util.*;

public class Day_89 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter number of test cases (T): ");
        int T = sc.nextInt();

        while (T-- > 0) {
            System.out.println("Enter N (size), K (group size), C (condition factor): ");
            int N = sc.nextInt();
            int K = sc.nextInt();
            long C = sc.nextLong();

            System.out.println("Enter the array: ");
            long[] array = new long[N];
            for (int i = 0; i < N; i++) {
                array[i] = sc.nextLong();
            }

            int maxSteps = calculateMaxSteps(array, N, K, C);
            System.out.println("Maximum number of steps: " + maxSteps);
        }

        sc.close();
    }

    private static int calculateMaxSteps(long[] array, int N, int K, long C) {
        Arrays.sort(array); // Sort the array in non-decreasing order
        int left = 0;
        int right = N / K; // Max possible steps
        int result = 0;

        // Perform binary search for maximum steps
        while (left <= right) {
            int mid = left + (right - left) / 2;

            if (canFormGroups(array, mid, K, C)) {
                result = mid;
                left = mid + 1;
            } else {
                right = mid - 1;
            }
        }

        return result;
    }

    private static boolean canFormGroups(long[] array, int steps, int K, long C) {
        if (steps * K > array.length) return false; // Not enough elements for 'steps' groups

        long[][] groups = new long[K][steps];
        int index = 0;

        // Fill the first group
        for (int i = 0; i < steps; i++) {
            groups[0][i] = array[index++];
        }

        // Fill the remaining groups
        for (int group = 1; group < K; group++) {
            for (int i = 0; i < steps; i++) {
                boolean found = false;

                while (index < array.length) {
                    if (array[index] >= groups[group - 1][i] * C) {
                        groups[group][i] = array[index++];
                        found = true;
                        break;
                    }
                    index++;
                }

                if (!found) return false;
            }
        }

        return true;
    }
}
📊 Sample Input and Output
Input:

2
6 2 2
1 2 4 8 16 32
7 3 3
3 9 27 2 6 18 1
Output:

3
2
```
---
## 🛠️ Technologies Used
- Language: Java
- Concepts: Binary Search, Arrays, Sorting, Modular Arithmetic

---
## 🤝 Connect with Me
- GitHub: kiranreddy4433E
- LinkedIn: Chandra Kiran Reddy

---
## 🌟 Acknowledgments
This problem is part of my 100 Days of Code Challenge, where I aim to solve coding problems daily and enhance my problem-solving skills.
