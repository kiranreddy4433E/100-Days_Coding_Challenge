# Day 95: Breaking N into Powers of 2

## 📝 Problem Description

Kulyash is given an integer `N` and needs to break it into some number of **powers of 2**. To achieve this, he can perform the following operation:

- Choose an integer `X` he already has and break it into two integers `Y` and `Z` such that `X = Y + Z`.

The goal is to determine the **minimum number of operations** required to break `N` into individual powers of 2.

---

## 🚀 Approach

1. **Binary Representation Insight**:
   - Any number `N` can be represented as a sum of powers of 2 based on its binary representation.
   - For example:
     - `13 (1101 in binary)` can be broken into `8 (2^3) + 4 (2^2) + 1 (2^0)`.

2. **Key Observations**:
   - The number of `1`s in the binary representation of `N` (`Integer.bitCount(N)`) indicates how many distinct powers of 2 are present.
   - To break `N` into these powers of 2:
     - We need to perform `count of 1s - 1` operations because the first power does not require splitting.

3. **Steps**:
   - Count the number of `1`s in the binary representation of `N`.
   - Subtract 1 to compute the **minimum number of operations**.

4. **Complexity**:
   - **Time Complexity**: `O(1)` per test case (using `Integer.bitCount`).
   - **Space Complexity**: `O(1)`.

---

## 💻 Code

```java
package coading_Challange;

import java.util.*;

public class Day_95 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Read the number of test cases
        int T = input.nextInt();
        while (T-- > 0) {
            // Read the integer N
            int N = input.nextInt();

            // Count the number of 1s in the binary representation of N
            int countOnes = Integer.bitCount(N);

            // Minimum number of operations
            int minOperations = countOnes - 1;

            // Output the result
            System.out.println(minOperations);
        }

        input.close();
    }
}
🔍 Input/Output Examples
Example 1:
Input:

3
13
4
7
Output:

2
0
2
```
---
## Explanation:

- For 13 (1101 in binary):
- Powers of 2: 8 + 4 + 1.
- Operations: 2 splits (13 -> 8 + 5 -> 8 + 4 + 1).
- For 4 (100 in binary):
- Powers of 2: 4.
- Operations: 0 splits (4 is already a power of 2).
- For 7 (111 in binary):
- Powers of 2: 4 + 2 + 1.
- Operations: 2 splits (7 -> 4 + 3 -> 4 + 2 + 1).

---
## 🧠 Key Learnings
- Binary Representation:
- The number of 1s in the binary representation of a number determines the number of distinct powers of 2.
- Efficient Calculation:
- Using Integer.bitCount(N) allows for quick computation of the number of 1s.

---
## 💡 Next Steps
- Dive deeper into binary operations and their applications in problem-solving.
- Explore more efficient algorithms for bitwise manipulation.

---
## 🤝 Let's Connect!
- Feel free to reach out for questions or discussions! 😊

#100DaysOfCode #Java #BitManipulation #CodingChallenge
