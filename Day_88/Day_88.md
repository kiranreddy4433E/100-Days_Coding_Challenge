# Day 88 of 100 - 100 Days of Code Challenge

## 📝 Problem: Lexicographically Smallest Permutation with Swaps

Blobo2 is participating in his practical exam, where the teacher has given him a permutation \( A \) of \( N \) integers. The goal is to find the **lexicographically smallest permutation** Blobo2 can generate after applying the following operations:

1. **Left Shift Operation**: Blobo2 can take the first element of the permutation and move it to the back of the permutation.
2. **At Most Two Swaps**: Blobo2 can swap any two elements in the permutation up to **two times**.

Blobo2 wants to impress his teacher by generating the **smallest permutation** possible after performing any number of left shifts and at most two swaps.

### Notes:
- A permutation of size \( N \) contains all integers from \( 1 \) to \( N \) exactly once.
- During a swap, Blobo2 can choose any two indices \( i \) and \( j \) (where \( 1 \leq i, j \leq N \)) and swap \( A[i] \) with \( A[j] \).

---

## 🔗 Input and Output Format

### Input:
1. The first line contains \( T \), the number of test cases.
2. For each test case:
   - The first line contains \( N \), the size of the permutation.
   - The second line contains \( N \) integers representing the permutation.

### Output:
For each test case, output the **lexicographically smallest permutation** Blobo2 can generate.

---

## 💡 Approach

1. **Generate All Rotations**:
   - Create all possible **rotations** of the given permutation using left shifts.

2. **Apply At Most Two Swaps**:
   - For each rotation, try all possible combinations of two swaps (including no swaps and one swap).

3. **Track the Smallest Permutation**:
   - Use lexicographical comparison to keep track of the smallest permutation across all rotations and swaps.

4. **Output the Result**:
   - Print the smallest permutation found for each test case.

---

## 🚀 Code Implementation

```java
package coading_Challange;

import java.util.*;

public class Day_88 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Number of test cases
        System.out.println("Enter number of test cases:");
        int T = input.nextInt();

        while (T-- > 0) {
            System.out.println("Enter size of the permutation:");
            int N = input.nextInt();

            System.out.println("Enter the permutation:");
            int[] A = new int[N];
            for (int i = 0; i < N; i++) {
                A[i] = input.nextInt();
            }

            System.out.println("Lexicographically smallest permutation: " + findSmallestPermutation(A));
        }
        input.close();
    }

    private static String findSmallestPermutation(int[] A) {
        int N = A.length;
        int[] smallest = Arrays.copyOf(A, N); // Track the smallest permutation

        // Generate all rotations (left shifts)
        for (int i = 0; i < N; i++) {
            int[] rotated = rotateLeft(A, i);

            // Generate all possible permutations with at most two swaps
            findSmallestWithTwoSwaps(rotated, smallest);
        }

        // Convert result to string for output
        StringBuilder result = new StringBuilder();
        for (int num : smallest) {
            result.append(num).append(" ");
        }
        return result.toString().trim();
    }

    private static void findSmallestWithTwoSwaps(int[] perm, int[] smallest) {
        int N = perm.length;

        // Try all combinations of two swaps (or no swaps)
        for (int i = 0; i < N; i++) {
            for (int j = i; j < N; j++) {
                for (int k = j; k < N; k++) {
                    for (int l = k; l < N; l++) {
                        // Create a copy of the array
                        int[] swapped = Arrays.copyOf(perm, N);

                        // Perform up to two swaps
                        swap(swapped, i, j);
                        if (k != i || l != j) {
                            swap(swapped, k, l);
                        }

                        // Update smallest permutation if needed
                        if (isLexicographicallySmaller(swapped, smallest)) {
                            System.arraycopy(swapped, 0, smallest, 0, N);
                        }
                    }
                }
            }
        }
    }

    private static boolean isLexicographicallySmaller(int[] A, int[] B) {
        for (int i = 0; i < A.length; i++) {
            if (A[i] < B[i]) {
                return true;
            } else if (A[i] > B[i]) {
                return false;
            }
        }
        return false; // Arrays are equal
    }

    private static void swap(int[] array, int i, int j) {
        int temp = array[i];
        array[i] = array[j];
        array[j] = temp;
    }

    private static int[] rotateLeft(int[] A, int shifts) {
        int N = A.length;
        int[] rotated = new int[N];
        for (int i = 0; i < N; i++) {
            rotated[i] = A[(i + shifts) % N];
        }
        return rotated;
    }
}
📊 Sample Input and Output
Input:

2
4
4 3 2 1
3
1 3 2
Output:

1 2 3 4
1 2 3
```
---
## 🛠️ Technologies Used
- Language: Java
- Concepts: Arrays, Rotations, Permutations, Lexicographical Comparison

---
## 🤝 Connect with Me
- GitHub: kiranreddy4433E
- LinkedIn: [Chandra Kiran Reddy](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/recent-activity/all/)

---
## 🌟 Acknowledgments
This problem is part of my 100 Days of Code Challenge, where I aim to solve coding problems daily and enhance my problem-solving skills.
