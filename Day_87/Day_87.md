# Day 87 of 100 - 100 Days of Code Challenge

## 📝 Problem: Minimum Non-Negative Energy for Frog Jumps

There are **N stones** in a pond, each having a value \( A[i] \) written on it. A frog starts at **stone 1** and wants to reach **stone N**. The frog can jump from **stone i** to **stone j** (where \( j > i \)).

The energy required for a jump from \( i \) to \( j \) is calculated as:
\[
Energy = (d \cdot A[i]) - A[j]
\]
where:
- \( d = j - i + 1 \) (the distance between the stones),
- \( A[i] \) and \( A[j] \) are the values written on the stones.

The goal is to calculate the **minimum non-negative energy** required for the frog to jump from the first stone to the last stone.

### Notes:
- If the total energy required is negative, the result should be \( 0 \).
- Ensure the frog can jump optimally to minimize energy consumption.

---

## 🔗 Problem Input and Output Format

### Input:
1. The first line contains \( T \) — the number of test cases.
2. For each test case:
   - The first line contains \( N \) — the number of stones.
   - The second line contains \( N \) integers denoting the values written on the stones.

### Output:
For each test case, output a single integer — the minimum non-negative energy required.

### Example:

#### Input:
4 3 6 1 3 4 3 1 10 4 3 7 9 1 2 1 5


#### Output:
10 4 20 0


---

## 💻 Solution

### Approach:
1. Use **Dynamic Programming (DP)** to calculate the minimum energy required for the frog to reach each stone.
2. Initialize a DP array `dp` where `dp[i]` represents the minimum energy required to reach stone \( i \).
3. Start from the first stone (`dp[0] = 0`) and iterate through each stone.
4. For each possible jump, calculate the energy required using the formula:
   \[
   Energy = (d \cdot A[i]) - A[j]
   \]
5. Update the DP array to store the minimum energy for each stone.
6. Ensure the result is non-negative using `Math.max(dp[N-1], 0)`.

---

## 🚀 Code Implementation

```java
package coading_Challange;

import java.util.*;

public class Day_87 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Number of test cases
        System.out.println("Enter the number of test cases (T): ");
        int T = input.nextInt();

        // Process each test case
        for (int t = 0; t < T; t++) {
            System.out.println("Enter the number of stones (N) for test case " + (t + 1) + ": ");
            int N = input.nextInt(); // Number of stones

            System.out.println("Enter the values on the stones:");
            int[] stones = new int[N];
            for (int i = 0; i < N; i++) {
                stones[i] = input.nextInt(); // Values on the stones
            }

            // Call the function to compute the minimum energy
            int result = calculateMinimumEnergy(N, stones);

            // Print the result
            System.out.println("Minimum non-negative energy required: " + result);
        }

        input.close();
    }

    // Function to calculate the minimum non-negative energy
    private static int calculateMinimumEnergy(int N, int[] stones) {
        int[] dp = new int[N]; // dp[i] represents the minimum energy to reach stone i
        Arrays.fill(dp, Integer.MAX_VALUE); // Initialize dp array with maximum value
        dp[0] = 0; // Starting from stone 1 requires 0 energy

        for (int i = 0; i < N; i++) {
            for (int j = i + 1; j < N; j++) {
                int d = j - i + 1; // Length of the subarray (distance between stones)
                int energy = (d * stones[i]) - stones[j]; // Energy required for the jump
                dp[j] = Math.min(dp[j], dp[i] + energy); // Update minimum energy for stone j
            }
        }

        // Ensure non-negative energy
        return Math.max(dp[N - 1], 0);
    }
}
📊 Sample Input/Output Walkthrough:
Input:

4
3
6 1 3
4
3 1 10 4
3
7 9 1
2
1 5
Output:

10
4
20
0
```
---
## 🛠️ Technologies Used
- Language: Java
- Concepts: Dynamic Programming, Arrays

---
## 🤝 Connect with Me
- GitHub: [kiranreddy4433E](https://github.com/kiranreddy4433E)
- LinkedIn: [Chandra Kiran Reddy](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)

---
## 🌟 Acknowledgments
This problem is part of my 100 Days of Code Challenge, where I aim to solve coding problems daily and improve my problem-solving skills.
