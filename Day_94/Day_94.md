# Day 94: Joke Spread Simulation in Mybeard Social Network

## 📝 Problem Description

In the social network **Mybeard**, the gnomes spread jokes to their friends.  
- Each gnome can forward a joke to their friends exactly **1 minute** after receiving it.
- The **friendship relationships** between gnomes are represented as a **directed adjacency matrix**, where:
  - `g[i][j] = 1` indicates gnome `i` is friends with gnome `j`.
  - `g[i][j] = 0` means no direct friendship exists.
- You are given `M` queries where you need to determine which gnomes will receive a joke after exactly `K` minutes if the joke starts at gnome `x`.

---

## 🚀 Approach

1. **Input Representation**:
   - A **directed adjacency matrix** represents friendship relationships.
   - Queries specify the time `K` and the starting gnome `x`.

2. **Key Observations**:
   - The spread of jokes can be computed using **matrix exponentiation**:
     - If `g[i][j] = 1`, gnome `j` receives the joke from `i` in 1 minute.
     - For `K = 2`, we compute `g^2` (matrix multiplication).
     - For arbitrary `K`, we use **binary exponentiation** to compute `g^K` efficiently.
   - Use **bitwise operations** for efficient computation with large matrices.

3. **Algorithm**:
   - Precompute `g^t` for all powers of 2 (up to 2^30).
   - Use binary representation of `K` to compute `g^K` using precomputed powers.
   - Determine the set of gnomes who received the joke after `K` minutes.

4. **Complexity**:
   - Precomputation: `O(N^3 log(K))` for `N` gnomes.
   - Query Processing: `O(N^2 log(K))`.

---

## 💻 Code

```java
package coading_Challange;

import java.util.*;

public class Day_94 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Number of gnomes
        int n = input.nextInt();
        long[][][] g = new long[30][n][(n + 63) / 64]; // Compressed bitwise representation of adjacency matrix

        // Input adjacency matrix
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                if (input.nextInt() == 1) {
                    g[0][i][j / 64] |= 1L << (j % 64);
                }
            }
        }

        // Precompute reachability for powers of 2 using dynamic programming
        for (int t = 1; t < 30; t++) {
            for (int i = 0; i < n; i++) {
                for (int j = 0; j < n; j++) {
                    if ((g[t - 1][i][j / 64] & (1L << (j % 64))) != 0) {
                        for (int k = 0; k < (n + 63) / 64; k++) {
                            g[t][i][k] |= g[t - 1][j][k];
                        }
                    }
                }
            }
        }

        // Number of queries
        int m = input.nextInt();

        // Process each query
        while (m-- > 0) {
            int k = input.nextInt(); // Time in minutes
            int x = input.nextInt() - 1; // Starting gnome (0-based indexing)

            // Initialize mask with the starting gnome
            long[] mask = new long[(n + 63) / 64];
            mask[x / 64] = 1L << (x % 64);

            // Process k in binary form (using precomputed powers of 2)
            for (int t = 0; t < 30; t++) {
                if ((k & (1 << t)) != 0) {
                    long[] newMask = new long[(n + 63) / 64];
                    for (int i = 0; i < n; i++) {
                        if ((mask[i / 64] & (1L << (i % 64))) != 0) {
                            for (int j = 0; j < (n + 63) / 64; j++) {
                                newMask[j] |= g[t][i][j];
                            }
                        }
                    }
                    mask = newMask;
                }
            }

            // Collect all gnomes who received the joke
            List<Integer> result = new ArrayList<>();
            for (int i = 0; i < n; i++) {
                if ((mask[i / 64] & (1L << (i % 64))) != 0) {
                    result.add(i + 1); // Convert back to 1-based indexing
                }
            }

            // Output the results
            System.out.println(result.size());
            if (result.isEmpty()) {
                System.out.println("-1");
            } else {
                for (int i = 0; i < result.size(); i++) {
                    if (i > 0) System.out.print(" ");
                    System.out.print(result.get(i));
                }
                System.out.println();
            }
        }

        input.close();
    }
}
🔍 Input/Output Examples

4
1 1 0 0
0 1 1 0
0 0 1 1
1 0 0 1
3
1 1
2 2
3 3
Output:

2
1 2
1
1
0
-1
```
---
## 🧠 Key Learnings
Efficient graph traversal using bitwise operations for adjacency matrix representation.
Binary exponentiation to compute large powers of matrices.
Practical application of reachability in graphs for social network modeling.

---
## 📬 Connect with Me!
Feel free to reach out for questions or discussions. 😊

---
## #100DaysOfCode #Java #CodingChallenge #GraphTheory #MatrixExponentiation
