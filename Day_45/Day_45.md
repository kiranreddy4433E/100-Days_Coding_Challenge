# Day 45 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 45** of my **100 Days of Code Challenge**! Today, I implemented a Java program to find the **smallest** and **largest elements** in an array. This task helped me practice array operations and sorting.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept an array of integers from the user.
  2. Sort the array in ascending order.
  3. Identify and print the smallest and largest elements.
- Practiced using the `Arrays.sort()` method and array traversal.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Sorting, Loops

## 📖 Problem Description
- The task is to:
  1. Input the size of an array and its elements.
  2. Sort the array.
  3. Display the sorted array along with the smallest and largest elements.

For example:
  - Input: `Array: [3, 1, 4, 1, 5, 9]`
  - Output:
    ```
    Sorted array: [1, 1, 3, 4, 5, 9]
    Smallest element: 1
    Largest element: 9
    ```

---

### Input/Output Example:

- **Input**:
Enter the number of elements in the array: 6 Enter the elements: 3 1 4 1 5 9

markdown
Copy code
- **Output**:
Sorted array: 1 1 3 4 5 9 Smallest element: 1 Largest element: 9

csharp
Copy code

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;
import java.util.Arrays;

public class pro_64 {

  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      System.out.println("Enter the number of elements in the array: ");
      int num = input.nextInt();

      int[] arrays = new int[num];

      System.out.println("Enter the array elements: ");
      for (int i = 0; i < num; i++) {
          arrays[i] = input.nextInt();
      }

      // Sort the array
      Arrays.sort(arrays);

      System.out.println("Sorted array: ");
      for (int i = 0; i < num; i++) {
          System.out.println(arrays[i]);
      }

      // Print the smallest and largest elements
      System.out.println("Smallest element: " + arrays[0]);
      System.out.println("Largest element: " + arrays[num - 1]);

      input.close();
  }
}
🖥️ Program Output
Example 1:

Enter the number of elements in the array: 
6
Enter the array elements: 
3 1 4 1 5 9
Sorted array: 
1
1
3
4
5
9
Smallest element: 1
Largest element: 9
```
---
### 📚 Lessons Learned
Practiced sorting arrays using Arrays.sort().
Improved understanding of identifying specific elements (smallest and largest) after sorting.

---
### ⚡ Challenges
Ensuring the program works for arrays of varying sizes, including single-element arrays.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.


 
100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
