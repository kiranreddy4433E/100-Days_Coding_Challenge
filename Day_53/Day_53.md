# Day 53 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 53** of my **100 Days of Code Challenge**! Today, I implemented a Java program to calculate the **maximum product subarray** in a given array. This task enhanced my understanding of array traversal and subarray operations.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept an integer array as input.
  2. Find the subarray with the maximum product of its elements.
  3. Display the maximum product.
- Practiced nested loops and optimized calculations for subarrays.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Nested Loops, Subarray Calculations

## 📖 Problem Description
- The task is to:
  1. Input the size and elements of an integer array.
  2. Find the subarray with the highest product.
  3. Display the maximum product.

For example:
  - Input: `Array: [2, 3, -2, 4]`
  - Output:
    ```
    Maximum product subarray: 6
    ```

---

### Input/Output Example:

- **Input**:
Size of the array: 4 Enter the elements: 2 3 -2 4

- **Output**:
Maximum product subarray: 6

java
Copy code

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_78 {

  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      System.out.println("Size of the array: ");
      int num = input.nextInt();

      int[] array = new int[num];

      System.out.println("Enter the array elements: ");
      for (int i = 0; i < num; i++) {
          array[i] = input.nextInt();
      }

      int max_array = array[0];
      int product = 1;

      // Calculate the maximum product subarray
      for (int i = 0; i < num; i++) {
          product = array[i];
          max_array = Math.max(max_array, product);

          for (int j = i + 1; j < num; j++) {
              product *= array[j];
              max_array = Math.max(max_array, product);
          }
      }

      System.out.println("Maximum product subarray: " + max_array);
      input.close();
  }
}
🖥️ Program Output
Example 1:

Size of the array: 
4
Enter the array elements: 
2 3 -2 4
Maximum product subarray: 6
Example 2:

Size of the array: 
5
Enter the array elements: 
-1 -3 -10 0 60
Maximum product subarray: 60
```
---
## 📚 Lessons Learned
Learned how to calculate products of subarrays using nested loops.
Understood how to maintain and update the maximum product during iteration.

---
## ⚡ Challenges
Optimizing the nested loop structure to handle larger arrays efficiently.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
