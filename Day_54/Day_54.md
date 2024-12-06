# Day 54 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 54** of my **100 Days of Code Challenge**! Today, I implemented a Java program to determine whether two arrays are **disjoint**. Arrays are considered disjoint if they have no common elements.

## ✅ What I did today
- Wrote a Java program to:
  1. Input two arrays from the user.
  2. Check if the arrays are disjoint or share common elements.
  3. Display the result along with any common elements if found.
- Practiced nested loops and array comparisons.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Nested Loops, Disjoint Sets

## 📖 Problem Description
- The task is to:
  1. Input the sizes and elements of two arrays.
  2. Check if the arrays share any common elements.
  3. Print the result: whether the arrays are disjoint or not.

For example:
  - Input:
    ```
    Array 1: [1, 2, 3]
    Array 2: [4, 5, 6]
    ```
  - Output:
    ```
    Arrays are disjoint.
    ```

  - Input:
    ```
    Array 1: [1, 2, 3]
    Array 2: [3, 4, 5]
    ```
  - Output:
    ```
    Arrays are not disjoint. Common element: 3
    ```

---

### Input/Output Example:

- **Input**:
Size of the arrays: 3 3 Enter the elements of Array 1: 1 2 3 Enter the elements of Array 2: 3 4 5


- **Output**:
Array 1: [1, 2, 3] Array 2: [3, 4, 5] Arrays are not disjoint. Common element: 3

java
Copy code

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;
import java.util.Arrays;

public class pro_79 {

  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      System.out.println("Size of the arrays: ");
      int num = input.nextInt();
      int num1 = input.nextInt();

      int[] array1 = new int[num];
      int[] array2 = new int[num1];

      System.out.println("Enter the elements of Array 1: ");
      for (int i = 0; i < num; i++) {
          array1[i] = input.nextInt();
      }

      System.out.println("Enter the elements of Array 2: ");
      for (int j = 0; j < num1; j++) {
          array2[j] = input.nextInt();
      }

      System.out.println("Array 1: " + Arrays.toString(array1));
      System.out.println("Array 2: " + Arrays.toString(array2));

      boolean disjoint = true;

      for (int i = 0; i < num; i++) {
          for (int j = 0; j < num1; j++) {
              if (array1[i] == array2[j]) {
                  System.out.println("Arrays are not disjoint. Common element: " + array1[i]);
                  disjoint = false;
                  break;
              }
          }
      }

      if (disjoint) {
          System.out.println("Arrays are disjoint.");
      }

      input.close();
  }
}
🖥️ Program Output
Example 1: Disjoint Arrays

Size of the arrays: 
3 3
Enter the elements of Array 1: 
1 2 3
Enter the elements of Array 2: 
4 5 6
Array 1: [1, 2, 3]
Array 2: [4, 5, 6]
Arrays are disjoint.
Example 2: Arrays with Common Elements

Size of the arrays: 
3 3
Enter the elements of Array 1: 
1 2 3
Enter the elements of Array 2: 
3 4 5
Array 1: [1, 2, 3]
Array 2: [3, 4, 5]
Arrays are not disjoint. Common element: 3
```
---
## 📚 Lessons Learned
Practiced checking array elements for intersections.
Improved understanding of nested loops and array comparison logic.

---
## ⚡ Challenges
Ensuring proper handling of edge cases such as empty arrays or arrays with duplicate values.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
