# Day 49 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 49** of my **100 Days of Code Challenge**! Today, I implemented a Java program to calculate the **minimum scalar product** (dot product) of two vectors represented as arrays. This task helped me explore sorting techniques and efficient mathematical operations on arrays.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept two integer arrays of the same size as input.
  2. Sort the arrays and calculate their dot product to minimize the scalar product.
  3. Display the minimum scalar product.
- Practiced sorting arrays and applying mathematical operations on vectors.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Sorting, Mathematical Operations

## 📖 Problem Description
- The task is to:
  1. Input two integer arrays of the same size.
  2. Sort one array in ascending order and the other in descending order.
  3. Compute the scalar product using the formula:
     ```
     Scalar Product = Σ(X[i] * Y[i])
     ```
  4. Display the minimum scalar product.

For example:
  - Input:
    ```
    Array X: [1, 3, 5]
    Array Y: [2, 4, 6]
    ```
  - Output:
    ```
    The minimum scalar product is: 27
    ```

---

### Input/Output Example:

- **Input**:
Enter the size of the arrays: 3 Enter elements of array X: 1 3 5 Enter elements of array Y: 2 4 6

markdown
Copy code
- **Output**:
The minimum scalar product is: 27

java
Copy code

---

## 📝 Code Example

```java
package dsa;

import java.util.Arrays;
import java.util.Scanner;

public class pro_69 {

  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      System.out.println("Enter the size of the arrays:");
      int n = input.nextInt();

      int[] X = new int[n];
      System.out.println("Enter elements of array X:");
      for (int i = 0; i < n; i++) {
          X[i] = input.nextInt();
      }

      int[] Y = new int[n];
      System.out.println("Enter elements of array Y:");
      for (int i = 0; i < n; i++) {
          Y[i] = input.nextInt();
      }

      // Sort X in ascending order
      Arrays.sort(X);

      // Sort Y in descending order
      Arrays.sort(Y);
      for (int i = 0; i < n / 2; i++) {
          int temp = Y[i];
          Y[i] = Y[n - 1 - i];
          Y[n - 1 - i] = temp;
      }

      // Compute the minimum scalar product
      long minScalarProduct = 0;
      for (int i = 0; i < n; i++) {
          minScalarProduct += (long) X[i] * Y[i];
      }

      System.out.println("The minimum scalar product is: " + minScalarProduct);
  }
}
🖥️ Program Output
Example 1:

Enter the size of the arrays:
3
Enter elements of array X:
1 3 5
Enter elements of array Y:
2 4 6
The minimum scalar product is: 27
Example 2:

Enter the size of the arrays:
4
Enter elements of array X:
1 2 3 4
Enter elements of array Y:
5 6 7 8
The minimum scalar product is: 70
```
---
## 📚 Lessons Learned
Practiced sorting arrays in both ascending and descending order.
Learned how to compute scalar products and optimize the result for a specific condition.

---
## ⚡ Challenges
Handling large array sizes to ensure correct computation without integer overflow (used long for scalar product).

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
