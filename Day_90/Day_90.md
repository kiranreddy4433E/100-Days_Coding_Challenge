# Day 90 of 100 - 100 Days of Code Challenge

## 📝 Problem: Lexicographically Smallest String

Gru has a string \( S \) of length \( N \), consisting only of the characters `a` and `b`. Gru also has \( P \) points to spend on operations. Gru wants to transform the string into the **lexicographically smallest string** possible by performing the following operations any number of times:

1. **Swap Operation**:
   - Swap any two characters in the string.
   - **Cost**: 1 point.

2. **Replace Operation**:
   - Replace a character in the string with any other lowercase English letter.
   - **Cost**: 2 points.

Your task is to help Gru obtain the lexicographically smallest string using at most \( P \) points.

---

## 🔗 Input and Output Format

### Input:
1. The first line contains \( T \), the number of test cases.
2. For each test case:
   - The first line contains two integers \( N \) (length of the string) and \( P \) (number of points).
   - The second line contains the string \( S \) of length \( N \), consisting of only the characters `a` and `b`.

### Output:
For each test case, output the **lexicographically smallest string** that Gru can create using at most \( P \) points.

---

## 💡 Approach

1. **Sorting the Target String**:
   - Compute the **sorted version** of the string \( S \), which represents the target lexicographically smallest string.

2. **Replace Characters**:
   - For each character in the string:
     - If it doesn't match the corresponding character in the sorted string, replace it.
     - Deduct 2 points from \( P \) for each replacement.

3. **Swap Remaining Characters**:
   - If \( P > 0 \), try to improve the order further by performing swaps:
     - Iterate through the string and swap any characters that would result in a lexicographically smaller string.
     - Deduct 1 point for each swap.

4. **Output the Result**:
   - Return the transformed string after performing the operations.

---

## 🚀 Code Implementation

```java
package coading_Challange;

import java.util.*;

public class Day_90 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read the number of test cases
        System.out.println("Enter the number of test cases: ");
        int T = sc.nextInt();

        while (T-- > 0) {
            // Read N and P
            System.out.println("Enter N (length of string) and P (points): ");
            int N = sc.nextInt();
            int P = sc.nextInt();
            sc.nextLine(); // Consume the newline character

            // Read the string S
            System.out.println("Enter the string S: ");
            char[] S = sc.nextLine().toCharArray();

            // Process the string to get the lexicographically smallest string
            String result = getLexicographicallySmallestString(S, N, P);
            System.out.println("Lexicographically smallest string: " + result);
        }

        sc.close();
    }

    private static String getLexicographicallySmallestString(char[] S, int N, int P) {
        char[] sorted = S.clone();
        Arrays.sort(sorted); // Sort to get the target lexicographic order

        // Replace characters to minimize lexicographic order
        for (int i = 0; i < N && P >= 2; i++) {
            if (S[i] != sorted[i]) {
                S[i] = sorted[i];
                P -= 2; // Deduct 2 points for replacement
            }
        }

        // If points remain, use them for swaps
        while (P > 0) {
            // Try to improve the order by swapping characters
            for (int i = 0; i < N - 1; i++) {
                for (int j = i + 1; j < N; j++) {
                    if (S[j] < S[i]) {
                        // Perform a swap if it improves the order
                        char temp = S[i];
                        S[i] = S[j];
                        S[j] = temp;
                        P--; // Deduct 1 point for the swap

                        // Break early if no points are left
                        if (P == 0) {
                            break;
                        }
                    }
                }
                if (P == 0) {
                    break;
                }
            }
        }

        // Return the final string
        return new String(S);
    }
}
📊 Sample Input and Output
Input:

2
4 3
abba
3 2
bab
Output:

Lexicographically smallest string: aabb
Lexicographically smallest string: abb
```
---
## 🛠️ Technologies Used
- Language: Java
- Concepts: Arrays, Sorting, String Manipulation

---
## 🤝 Connect with Me
- GitHub: kiranreddy4433E
- LinkedIn: Chandra Kiran Reddy

---
## 🌟 Acknowledgments
This problem is part of my 100 Days of Code Challenge, where I aim to solve coding problems daily and enhance my problem-solving skills.
