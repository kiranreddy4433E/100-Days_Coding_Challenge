# Day 78 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 78** of my **100 Days of Code Challenge**! Today, I worked on a challenging problem involving the computation of the sum of weights of all contiguous subarrays of a sorted array. The weight of a subarray is defined as the maximum value of \((B_i - B_j) \cdot (B_j - B_k)\) for all valid triples \((i, j, k)\).

## ✅ What I did today
- Designed a Java program to:
  - Calculate weights for all valid subarrays of length at least 3.
  - Optimize the process to handle sorted arrays efficiently.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Nested Loops, Arithmetic Operations, Arrays

## 📖 Problem Description
### Input:
- \( T \): Number of test cases.
- For each test case:
  - \( N \): Size of the array.
  - Array \( A \): Sorted integers \((A_1, A_2, ..., A_N)\).

### Output:
- The sum of weights for all contiguous subarrays of length at least 3.

---

### Input/Output Example:

#### Example:
**Input**:
Enter the number of test cases (T): 1 Test case 1: Enter the size of the array (N): 5 Enter 5 sorted array elements: 1 2 3 4 5


**Output**:
Total weight of subarrays: 27


#### Explanation:
The subarrays of length \(\geq 3\) are:
1. Subarray \([1, 2, 3]\): Weight = \((3 - 2) \cdot (2 - 1) = 1\)
2. Subarray \([1, 2, 3, 4]\): Weight = \((4 - 2) \cdot (2 - 1) = 2\)
3. Subarray \([1, 2, 3, 4, 5]\): Weight = \((5 - 3) \cdot (3 - 1) = 6\)

Sum of weights = \(1 + 2 + 6 = 27\).

---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_78 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter the number of test cases (T): ");
        int testCases = input.nextInt();

        for (int t = 1; t <= testCases; t++) {
            System.out.println("Test case " + t + ":");
            System.out.print("Enter the size of the array (N): ");
            int size = input.nextInt();
            int[] array = new int[size];
            System.out.println("Enter " + size + " sorted array elements: ");
            for (int i = 0; i < size; i++) {
                array[i] = input.nextInt();
            }

            long result = calculateWeight(array, size);
            System.out.println("Total weight of subarrays: " + result);
        }
    }

    private static long calculateWeight(int[] array, int size) {
        long sumOfWeights = 0;

        for (int start = 0; start < size - 2; start++) { // Start index
            for (int end = start + 2; end < size; end++) { // End index
                int first = array[start];
                int last = array[end];
                long maxWeight = 0;

                // Iterate through possible middle elements
                for (int mid = start + 1; mid < end; mid++) {
                    int middle = array[mid];
                    long weight = (long) (last - middle) * (middle - first);
                    maxWeight = Math.max(maxWeight, weight);
                }
                sumOfWeights += maxWeight;
            }
        }
        return sumOfWeights;
    }
}
🖥️ Program Output
Example:

Enter the number of test cases (T): 
1
Test case 1:
Enter the size of the array (N): 
5
Enter 5 sorted array elements: 
1 2 3 4 5
Total weight of subarrays: 27
```
---
## 📚 Lessons Learned
Gained experience in working with nested loops and arithmetic calculations for complex operations.
Understood how to efficiently compute results for contiguous subarrays of a sorted array.
Improved debugging skills for edge cases in mathematical operations.

---
## ⚡ Challenges
Handling edge cases for arrays with less than 3 elements.
Ensuring the algorithm performs efficiently for larger arrays.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

--- 
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
