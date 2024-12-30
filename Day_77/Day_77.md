# Day 77 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 77** of my **100 Days of Code Challenge**! Today, I tackled a challenging problem of calculating the maximum value among all possible ordered triplets in an array. The value of a triplet \((i, j, k)\) is defined as \((A[i] - A[j]) \cdot A[k]\), and the task was to determine the maximum such value efficiently.

## ✅ What I did today
- Designed a Java program to:
  1. Iterate through the array to compute the maximum and minimum values.
  2. Calculate the difference between the maximum and minimum values.
  3. Compute the maximum value of the triplet using the formula.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Nested Loops, Optimized Searching

## 📖 Problem Description
- **Input**:
  - \( T \): Number of test cases.
  - For each test case:
    - \( N \): Number of elements in the array.
    - Array \( A \) containing \( N \) integers.
- **Output**:
  - The maximum value among all possible ordered triplets.

---

### Input/Output Example:

#### Example 1:
**Input**:
Enter a T test case's: 2 Enter N and array for test case 1: 5 1 3 5 2 4 Enter N and array for test case 2: 3 7 1 9


**Output**:
Maximum Value for test case 1: 12 Maximum Value for test case 2: 56


#### Explanation:
1. **Test Case 1**: The array \([1, 3, 5, 2, 4]\) produces the maximum triplet value of \( (5 - 1) \cdot 4 = 12 \).
2. **Test Case 2**: The array \([7, 1, 9]\) produces the maximum triplet value of \( (9 - 1) \cdot 7 = 56 \).

---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_77 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter a T test case's:- ");
        int num = input.nextInt();
        for (int i = 0; i < num; i++) {
            int N = input.nextInt();
            int array[] = new int[N];
            for (int j = 0; j < N; j++) {
                array[j] = input.nextInt();
            }
            System.out.println("Maximum Value: " + MaximumTriplet(array, N));
        }
    }

    private static int MaximumTriplet(int array[], int N) {
        int MaxValue = Integer.MIN_VALUE;
        int MinValue = Integer.MAX_VALUE;
        int MaxDifference = Integer.MIN_VALUE;
        
        // Calculate maximum and minimum values
        for (int num : array) {
            MaxValue = Math.max(MaxValue, num);
            MinValue = Math.min(MinValue, num);
        }
        
        // Calculate maximum difference
        MaxDifference = MaxValue - MinValue;

        // Return the maximum triplet value
        return MaxDifference * MaxValue;
    }
}
🖥️ Program Output
Example:

Enter a T test case's: 
1
Enter N and array for test case 1:
5
1 3 5 2 4
Maximum Value: 12
```
---
## 📚 Lessons Learned
Learned how to optimize nested loop problems by precomputing minimum and maximum values in an array.
Enhanced understanding of array traversal and arithmetic operations to calculate desired results.
Strengthened skills in implementing efficient algorithms for competitive programming.

---
## ⚡ Challenges
Managing edge cases, such as when all elements in the array are equal, which results in a maximum value of 
0
0.
Ensuring that the algorithm efficiently handles larger arrays within the constraints.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
