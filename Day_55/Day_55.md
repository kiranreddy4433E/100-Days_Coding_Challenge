# Day 55 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 55** of my **100 Days of Code Challenge**! Today, I implemented a Java program to calculate the **sum of the maximum scalar product (dot product)** of two integer arrays treated as vectors. This task helped me practice vector operations and array traversal.

## ✅ What I did today
- Wrote a Java program to:
  1. Input two integer arrays of the same size.
  2. Calculate the scalar product of the two arrays.
  3. Print the sum of the scalar product.
- Practiced element-wise array operations and mathematical computations.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Scalar Product, Loops

## 📖 Problem Description
- The task is to:
  1. Input two integer arrays of the same size.
  2. Treat the arrays as vectors and compute their scalar product:
     ```
     Scalar Product = Σ(X[i] * Y[i])
     ```
  3. Display the sum of the scalar product.

For example:
  - Input:
    ```
    Array X: [1, 2, 3]
    Array Y: [4, 5, 6]
    ```
  - Output:
    ```
    Scalar Product: 32
    ```

---

### Input/Output Example:

- **Input**:
Size of the arrays: 3 Enter the elements of Array X: 1 2 3 Enter the elements of Array Y: 4 5 6

markdown
Copy code
- **Output**:
Scalar Product: 32

csharp
Copy code

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_81 {

  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      System.out.println("Size of the arrays: ");
      int num = input.nextInt();

      int[] array = new int[num];
      int[] array1 = new int[num];
      int sum = 0;

      System.out.println("Enter the elements of Array X: ");
      for (int i = 0; i < num; i++) {
          array[i] = input.nextInt();
      }

      System.out.println("Enter the elements of Array Y: ");
      for (int i = 0; i < num; i++) {
          array1[i] = input.nextInt();
      }

      System.out.println("Scalar product of X and Y arrays: ");
      for (int i = 0; i < num; i++) {
          int prod = array[i] * array1[i];
          sum += prod;
      }

      System.out.println(sum);
      input.close();
  }
}
🖥️ Program Output
Example 1:

Size of the arrays: 
3
Enter the elements of Array X: 
1 2 3
Enter the elements of Array Y: 
4 5 6
Scalar Product: 32
Example 2:

Size of the arrays: 
4
Enter the elements of Array X: 
1 0 -1 2
Enter the elements of Array Y: 
2 -1 3 4
Scalar Product: 9
```
---
## 📚 Lessons Learned
Practiced calculating scalar products for vectors.
Enhanced understanding of element-wise array operations.

---
## ⚡ Challenges
Handling arrays of unequal sizes (ensured arrays are the same size as a prerequisite).
Ensuring accurate results for arrays with negative and zero values.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
