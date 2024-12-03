# Day 51 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 51** of my **100 Days of Code Challenge**! Today, I implemented a Java program to **sort an integer array** in ascending order. This task helped me practice array input handling and sorting techniques using built-in methods.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept an integer array as input from the user.
  2. Sort the array in ascending order.
  3. Display the sorted array.
- Practiced using `Arrays.sort()` for efficient sorting.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Sorting, Loops

## 📖 Problem Description
- The task is to:
  1. Input the size of an integer array and its elements.
  2. Use a sorting algorithm or a built-in method to arrange the elements in ascending order.
  3. Display the sorted array.

For example:
  - Input: `Array: [5, 2, 9, 1, 6]`
  - Output:
    ```
    Sorted array: [1, 2, 5, 6, 9]
    ```

---

### Input/Output Example:

- **Input**:
Size of the array: 5 Enter the elements: 5 2 9 1 6


- **Output**:
Sorted array: 1 2 5 6 9

java
Copy code

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;
import java.util.Arrays;

public class pro_71 {

  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      System.out.println("Size of the array: ");
      int num = input.nextInt();

      int[] array = new int[num];

      System.out.println("Enter the array elements: ");
      for (int i = 0; i < num; i++) {
          array[i] = input.nextInt();
      }

      // Sort the array
      Arrays.sort(array);

      // Display the sorted array
      System.out.println("Sorted array: ");
      for (int i = 0; i < num; i++) {
          System.out.println(array[i]);
      }

      input.close();
  }
}
🖥️ Program Output
Example 1:

Size of the array: 
5
Enter the array elements: 
5 2 9 1 6
Sorted array: 
1
2
5
6
9
Example 2:

Size of the array: 
4
Enter the array elements: 
10 3 8 7
Sorted array: 
3
7
8
10
```
---
## 📚 Lessons Learned
Practiced array traversal and input handling.
Used the built-in Arrays.sort() method to simplify sorting tasks.

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
