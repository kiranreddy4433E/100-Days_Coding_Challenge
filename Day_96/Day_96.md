# Day 96: Maximizing Hamming Distance with Ball Arrangements

## 📝 Problem Description

Akhil has two rows of balls arranged in strings `X` and `Y`, each consisting of `N` balls. Each ball is either white (`W`) or black (`B`). Akhil wants to create a third row of `N` balls, `Z`, such that:

1. The **sum of the Hamming distances** between:
   - `X` and `Z`
   - `Y` and `Z`
   is maximized.

2. If multiple such rows `Z` exist, the **lexicographically smallest arrangement** should be chosen.

### Definitions
- **Hamming Distance**:
  The number of positions where corresponding characters in two strings differ.
  - Example: Hamming distance between `"WBB"` and `"BWB"` is `2`.

---

## 🚀 Approach

1. **Key Observations**:
   - To maximize the sum of Hamming distances:
     - For positions where `X[i] ≠ Y[i]`, pick the lexicographically smallest character (`B` is smaller than `W`).
     - For positions where `X[i] == Y[i]`, choose the opposite character of `X[i]`.

2. **Steps**:
   - Iterate through all positions in strings `X` and `Y`.
   - Based on the characters at each position:
     - If `X[i] != Y[i]`, append `'B'`.
     - If `X[i] == Y[i]`, append the opposite of `X[i]` to maximize the Hamming distance.
   - Construct the string `Z` following the above rules.

3. **Time Complexity**:
   - **O(T * N)** for `T` test cases, each processing strings of length `N`.

---

## 💻 Code

```java
package coading_Challange;

import java.util.Scanner;

public class Day_96 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Number of test cases
        int T = input.nextInt();
        input.nextLine(); // Consume the newline

        while (T-- > 0) {
            // Input strings X and Y
            String X = input.nextLine();
            String Y = input.nextLine();

            int N = X.length();
            StringBuilder Z = new StringBuilder();

            // Construct the string Z
            for (int i = 0; i < N; i++) {
                if (X.charAt(i) != Y.charAt(i)) {
                    Z.append('B'); // Pick the lexicographically smaller character
                } else {
                    // X[i] == Y[i], pick the opposite of X[i]
                    Z.append(X.charAt(i) == 'W' ? 'B' : 'W');
                }
            }

            // Output the result for the current test case
            System.out.println(Z.toString());
        }

        input.close();
    }
}
🔍 Input/Output Examples
Example 1:
Input:

2
WWB
BBW
WB
WB

Output:

BBB
BB
```
---
## Explanation:

- For X = "WWB" and Y = "BBW":
- At position 1: X[0] != Y[0], choose 'B'.
- At position 2: X[1] != Y[1], choose 'B'.
- At position 3: X[2] == Y[2] = 'B', choose the opposite of 'B' (i.e., 'W').
- Final Z = "BBB".
- For X = "WB" and Y = "WB":
- Both strings are identical; choose the opposite for all positions.
- Final Z = "BB".

--- 
## 🧠 Key Learnings
- Hamming Distance:
- This problem highlights the use of Hamming distance in optimization problems.
- Lexicographic Optimization:
- Understand how to balance multiple constraints (maximize distance while maintaining lexicographic order).
- String Manipulation:
- Efficiently process strings using character comparisons and StringBuilder.

---
## 💡 Next Steps
Explore more problems involving Hamming distance and lexicographical order.
Dive deeper into string manipulation problems with multi-constraint optimizations.

---
## 🤝 Let's Connect!
Feel free to reach out for questions or discussions! 😊

## #100DaysOfCode #Java #StringManipulation #HammingDistance #CodingChallenge
