# Day 79 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 79** of my **100 Days of Code Challenge**! Today, I worked on a problem involving a binary string where the goal was to determine the **minimum number of operations** required to convert all the characters of the string to `0`. The operations are performed by picking indices such that no two indices are adjacent and flipping the values at those indices.

---

## ✅ Problem Description
You are given a binary string \( S \) of length \( N \). You can perform the following operation:
1. Pick any set of indices such that no two picked indices are adjacent.
2. Flip the values at the picked indices (`0` to `1` and `1` to `0`).

### Example
#### Input:
T = 1 N = 7 S = "1101101"


#### Output:
2


#### Explanation:
- Pick the indices {1, 3, 6}.
- After the first operation, \( S \) becomes `0111111`.
- Pick the indices {2, 4, 7}.
- After the second operation, \( S \) becomes `0000000`.

---

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** String Manipulation, Loops

---

## 📖 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_79 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter the number of test cases (T): ");
        int T = input.nextInt();
        while (T-- > 0) {
            System.out.println("Enter the length of the binary string (N): ");
            int N = input.nextInt();
            System.out.println("Enter the binary string (S): ");
            String S = input.next();
            int operations = calculateOperations(S, N);
            System.out.println(operations);
        }
    }

    private static int calculateOperations(String S, int N) {
        int operations = 0;
        int i = 0;

        while (i < N) {
            if (S.charAt(i) == '1') {
                // Found a group of 1's, increment operation count
                operations++;
                // Skip all consecutive 1's in the current group
                while (i < N && S.charAt(i) == '1') {
                    i++;
                }
            } else {
                // Skip 0's
                i++;
            }
        }
        return operations;
    }
}
🖥️ Program Output
Input:

Enter the number of test cases (T): 
1
Enter the length of the binary string (N): 
7
Enter the binary string (S): 
1101101
Output:

2
```
---
## 📚 Lessons Learned
Learned how to efficiently parse binary strings and count operations required for transformations.
Improved skills in handling while loops and conditional logic for sequential operations on strings.
Gained experience in implementing solutions to minimize operations in constraints-based problems.

---
## ⚡ Challenges
Managing edge cases where the string contains no 1s or only isolated 1s.
Ensuring that the logic correctly skips over adjacent indices to avoid invalid operations.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
