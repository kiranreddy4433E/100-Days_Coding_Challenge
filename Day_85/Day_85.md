# Day 85 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 85** of my **100 Days of Code Challenge**! Today, I tackled a problem involving **graphs**, **dynamic programming**, and **pathfinding**. The task was to determine the number of "beautiful paths" in an undirected graph where nodes are labeled, and the path must match a given string's character sequence.

---

## ✅ Problem Description
You are given:
1. An **undirected graph** with \( N \) nodes and \( M \) edges.
2. A **target string** \( S \) of length \( L \).
3. Each node has a lowercase English letter written on it.

### A **beautiful path**:
- Consists of \( L - 1 \) edges connecting a sequence of \( L \) nodes.
- Matches the characters in \( S \) sequentially: the \( i \)-th node in the path must have the \( i \)-th character of \( S \).
- Paths can revisit nodes or edges any number of times.

### Objective:
Count the number of beautiful paths in the graph. Return the result modulo \( 10^9+7 \).

---

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Dynamic Programming (DP), Graph Traversal, Adjacency List

---

## 📖 Code Example

```java
package coading_Challange;

import java.util.*;

public class Day_85 {

    static final int MOD = 1000000007;

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int T = sc.nextInt(); // Number of test cases

        while (T-- > 0) {
            int N = sc.nextInt(); // Number of nodes
            int M = sc.nextInt(); // Number of edges
            int L = sc.nextInt(); // Length of string S

            String S = sc.next(); // Target string
            String nodeLabels = sc.next(); // Node labels

            int[] u = new int[M]; // Edge start nodes
            int[] v = new int[M]; // Edge end nodes

            for (int i = 0; i < M; i++) {
                u[i] = sc.nextInt() - 1; // Convert to 0-based
            }
            for (int i = 0; i < M; i++) {
                v[i] = sc.nextInt() - 1; // Convert to 0-based
            }

            // Build adjacency list
            List<Integer>[] graph = new ArrayList[N];
            for (int i = 0; i < N; i++) {
                graph[i] = new ArrayList<>();
            }
            for (int i = 0; i < M; i++) {
                graph[u[i]].add(v[i]);
                graph[v[i]].add(u[i]);
            }

            // DP array: dp[node][i] = ways to match S[0..i] ending at node
            int[][] dp = new int[N][L];
            for (int i = 0; i < N; i++) {
                if (nodeLabels.charAt(i) == S.charAt(0)) {
                    dp[i][0] = 1; // Initialize with nodes matching first character
                }
            }

            // Fill DP table
            for (int i = 0; i < L - 1; i++) {
                for (int node = 0; node < N; node++) {
                    if (dp[node][i] > 0) {
                        for (int neighbor : graph[node]) {
                            if (S.charAt(i + 1) == nodeLabels.charAt(neighbor)) {
                                dp[neighbor][i + 1] = (dp[neighbor][i + 1] + dp[node][i]) % MOD;
                            }
                        }
                    }
                }
            }

            // Compute final result
            int result = 0;
            for (int node = 0; node < N; node++) {
                result = (result + dp[node][L - 1]) % MOD;
            }

            System.out.println(result);
        }

        sc.close();
    }
}
🖥️ Program Output
Input:

1
4 5 3
abc
abac
1 2 2 3 3
2 3 3 4 4
Output:

2
```
---
## 📚 Lessons Learned
Gained experience working with graphs, adjacency lists, and dynamic programming.
Understood how to efficiently manage state transitions in a graph traversal problem.
Practiced handling modular arithmetic in complex DP-based problems.

---
## ⚡ Challenges
Efficiently implementing the DP transitions for large graphs and long strings.
Managing edge cases, such as disjoint graphs or mismatched character sequences.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

--- 
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
