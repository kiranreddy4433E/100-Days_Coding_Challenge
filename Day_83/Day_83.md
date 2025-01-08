# Day 83 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 83** of my **100 Days of Code Challenge**! Today, I solved a problem that calculates the **P1 value** for a **complete binary tree**, using a defined recursive formula involving the maximum product of values from child nodes. This exercise involved **modular arithmetic**, **tree traversal**, and **dynamic programming**.

---

## ✅ Problem Description
You are given a complete binary tree with height \( H \), where nodes are indexed top-down and left-right starting from 1. Each node \( i \) stores a positive integer \( V_i \). The value of \( P_i \) is defined as:
- \( P_i = V_i \) if \( i \) is a leaf node.
- \( P_i = \max(V_i \cdot P_L, V_i \cdot P_R) \mod 10^9+7 \), where \( L \) and \( R \) are the indices of the left and right children of \( i \), respectively.

The task is to calculate the value of \( P_1 \), which represents the value at the root of the tree.

---

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Modular Arithmetic, Dynamic Programming, Tree Traversal

---

## 📖 Code Example

```java
package coading_Challange;

import java.util.*;

public class Day_83 {

    static final int MOD = 1_000_000_007;

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (true) {
            // Read height of the tree
            int H = sc.nextInt();
            if (H == 0) break;

            // Read values for the complete binary tree
            int totalNodes = (1 << H) - 1; // Total nodes in a complete binary tree of height H
            int[] V = new int[totalNodes + 1]; // Node values, 1-based indexing
            for (int i = 1; i <= totalNodes; i++) {
                V[i] = sc.nextInt();
            }

            // Array to store P values
            int[] P = new int[totalNodes + 1];

            // Calculate P values from bottom to top
            for (int i = totalNodes; i >= 1; i--) {
                if (2 * i > totalNodes) { // Leaf node condition
                    P[i] = V[i];
                } else { // Internal node condition
                    int left = 2 * i;
                    int right = 2 * i + 1;
                    P[i] = (int) Math.max(
                            (long) V[i] * P[left] % MOD,
                            (long) V[i] * P[right] % MOD
                    );
                }
            }

            // Output the value of P1
            System.out.println(P[1]);
        }
        sc.close();
    }
}
🖥️ Program Output
Input:

3
3 2 1 1 2 3 4
2
2 3 4
0
Output:

24
8
```
---
## 📚 Lessons Learned
Gained experience working with complete binary trees and calculating values bottom-up.
Understood how to handle modular arithmetic in a recursive formula to avoid integer overflow.
Learned how to calculate values efficiently for large inputs using dynamic programming.

---
## ⚡ Challenges
Correctly implementing the bottom-up traversal for calculating 
𝑃
P values while ensuring modular constraints.
Handling large inputs while maintaining optimal performance.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

--- 
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
